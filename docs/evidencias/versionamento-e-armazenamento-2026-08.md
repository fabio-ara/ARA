# Evidências e alternativas para versionamento e armazenamento

**Categoria:** evidência técnica e análise de alternativas  
**Recorte temporal:** 4 e 5 de agosto de 2026  
**Estado:** histórico, não normativo

Este documento preserva o raciocínio técnico que sustentou a investigação de versionamento e armazenamento do ARA. Ele não seleciona banco de dados, BaaS, armazenamento de objetos, esquema físico, mecanismo de versionamento, granularidade de artefatos nem política de retenção.

Os fatos comerciais e operacionais sobre provedores registrados abaixo são um retrato do recorte temporal. Preços, quotas, políticas de pausa, limites e capacidades precisam ser revalidados antes de qualquer decisão futura.

As decisões vigentes sobre o significado do histórico permanecem em [`DECISOES.md`](../../DECISOES.md). As questões ainda abertas estão no [`BACKLOG.yaml`](../../BACKLOG.yaml).

## 1. Limites entre semântica e armazenamento

A análise distingue a semântica do produto do mecanismo físico usado para armazená-la.

A semântica já registrada exige distinguir histórico materializado e histórico deliberativo. Uma revisão de curso representa um estado lógico completo do curso, mas isso não obriga que todos os componentes inalterados sejam copiados fisicamente a cada revisão.

Permanecem questões de investigação:

- fronteira entre diário local, checkpoint e revisão durável;
- granularidade física de cursos, microssequências, cards e recursos;
- representação de múltiplos pais, restauração e consolidação;
- retenção e eliminação física condicionadas por referências, auditoria e pesquisa;
- divisão de responsabilidades entre banco transacional, armazenamento de artefatos e armazenamento local;
- projeções de leitura para histórico, diferenças e grafo;
- custo, backup, restauração, portabilidade, funcionamento offline e escala institucional.

## 2. Motivadores e requisitos candidatos

A análise estruturada registrou vinte razões para investigar um sistema de histórico mais forte. As formulações abaixo preservam o conteúdo da investigação, mas não transformam suas consequências técnicas em requisitos aprovados.

| Tema | Motivação registrada | Consequência técnica investigada |
|---|---|---|
| Autoria com pouca burocracia | Edições ordinárias não deveriam exigir cerimônia de confirmação | diário local e checkpoints automáticos |
| Segurança de edição | Erros e mudanças de ideia devem ser reversíveis | revisões imutáveis duráveis e restauração sem destruição |
| Conhecimento provisório | Publicação não torna um artefato definitivamente final | referências correntes e snapshots fixados por contexto |
| Investigação vertical | Examinar uma linhagem ao longo do tempo | DAG de revisões, operações, diferenças e recuperação seletiva de contexto |
| Investigação horizontal | Comparar observações e derivações entre pessoas | índices entre linhagens, corpora congelados e recuperação condicionada por acesso |
| Ciclo vertical-horizontal | Padrões coletivos podem orientar diagnóstico longitudinal e acompanhamento posterior | relações entre achados, operações, revisões e observações |
| Reprodutibilidade de pesquisa | Experimentos precisam fixar conteúdo e configurações exatos | snapshots de pesquisa e retenção controlada |
| Derivação colaborativa | Variantes pessoais e de grupos precisam preservar origens | DAG, possíveis múltiplos pais e reutilização de artefatos |
| Evolução de agentes | Perfis, instruções, conhecimento, contratos e modelos podem mudar | artefatos de configuração versionados e registro da configuração efetiva |
| Trabalho offline | Edição precisa continuar sem disponibilidade do servidor | materialização local, diário e fila de saída idempotente como alternativas |
| Mudanças concorrentes | Edição baseada em revisão antiga não deve sobrescrever trabalho novo silenciosamente | revisão-base explícita e preservação de divergência |
| Acesso em derivações | Restrições de audiência podem depender das origens necessárias | grafo de acesso e projeções efetivas, tema destinado à investigação de colaboração e acesso |
| Revogação sem destruição | Bloqueio de acesso não deveria apagar a trajetória | separar estado de acesso de eliminação do artefato |
| Economia de armazenamento | Variantes podem reutilizar partes inalteradas | comparar manifests, endereçamento por conteúdo e deduplicação |
| Proteção da carga do banco | Payloads extensos não deveriam dominar a carga transacional sem necessidade | comparar separação entre metadados relacionais e artefatos |
| Inspeção do histórico | Pessoas precisam navegar revisões e diferenças | modelos de leitura paginados, prévias e resumos de diferenças |
| Portabilidade | O histórico não deveria depender semanticamente de um único provedor | formatos, digests, exportação e restauração independentes de fornecedor |
| Retenção seletiva | Nem todo autosave precisa ser preservado indefinidamente | classes distintas para diário, checkpoint, revisão durável e retenção de pesquisa |
| Auditoria sem replay integral | Intenção e proveniência são úteis, mas não devem obrigar reconstrução de todo o estado por eventos | comparar revisões materializadas com registro de operações append-only |
| Escolha econômica de provedor | Limites de plano gratuito não devem definir a semântica do produto | decisão futura baseada em workloads, custo, backup, restauração e operação medidos |

## 3. Alternativas físicas comparadas

Nenhuma alternativa desta tabela foi selecionada. Os rótulos de adequação registram somente a avaliação feita no recorte da investigação.

| Alternativa | Principal vantagem observada | Principal risco observado | Leitura no recorte |
|---|---|---|---|
| Estado atual mais log de operações | CRUD simples | histórico pode ser insuficiente para restauração | insuficiente como mecanismo principal |
| Snapshots completos no banco relacional | simplicidade transacional e consulta direta | duplicação, crescimento de linhas, índices, WAL, backup e CPU | uso limitado ou experimental |
| Snapshots completos em armazenamento de objetos | leitura e restauração simples, banco menor | duplicação de bytes, objetos e leituras para diferenças | baseline simples a comparar |
| Objetos endereçados por conteúdo com manifests | deduplicação e derivações sem cópia integral | integridade, canonicalização, garbage collection e depuração mais complexos | hipótese arquitetural relevante, não escolhida |
| Deltas ou cadeias de patches | economia potencial de bytes | reconstrução, compactação, migração e acesso aleatório mais difíceis | possível otimização posterior |
| Event sourcing integral | intenção e auditoria detalhadas | replay, evolução de eventos, projeções e consistência aumentam complexidade | não recomendado como pressuposto universal no recorte |
| Versionamento nativo do armazenamento | recuperação operacional simples | semântica dependente do provedor e sem significado pedagógico próprio | proteção secundária possível |
| Linhas temporais no banco | consultas temporais relacionais | ajuste fraco a DAG, múltiplos pais e artefatos grandes | possível uso restrito a metadados |
| Repositório Git verdadeiro | DAG, diferenças, refs e compactação maduros | incompatibilidade com autorização granular, sync móvel e consultas de produto | referência para exportação e artefatos técnicos |
| Camada semelhante a Git sobre armazenamento de objetos | derivações econômicas e histórico sobre objetos imutáveis | camada especializada e maior complexidade operacional | referência arquitetural a comparar |

A análise também considerou como hipótese uma combinação de metadados relacionais pequenos, artefatos imutáveis e materialização local, mas a revisão posterior ampliou a comparação e manteve essa combinação sem autoridade de decisão.

## 4. Evidência temporal de provedores

Os dados a seguir foram registrados em 4 de agosto de 2026 a partir das páginas públicas indicadas. São evidência histórica, não informação atual garantida.

| Provedor | Componente ou plano | Fatos registrados no recorte | Implicação considerada | Limitação registrada |
|---|---|---|---|---|
| Supabase | Free | 500 MB de banco; 1 GB de arquivos; 5 GB de egress e cached egress; dois projetos ativos; projetos de baixa atividade podiam pausar após uma semana | útil para protótipos, mas sem garantia de disponibilidade contínua ou retenção duradoura | quotas e política podem mudar; há acoplamento à plataforma |
| Supabase | Pro | a partir de USD 25/mês; primeiro projeto incluído; 8 GB de disco de banco; 100 GB de arquivos; 250 GB de egress; backups diários retidos por sete dias | poderia atender a uma primeira implantação conectada sem pausa por inatividade | crescimento de banco e armazenamento ainda precisaria ser medido |
| Supabase | Pausa no Free | projetos de baixa atividade podiam pausar após sete dias; restauração disponível por até um ano | plano gratuito não equivalia a garantia durável de serviço ativo | restauração dependia de intervenção e janela temporal |
| Supabase | Storage | 1 GB no Free; 100 GB no Pro; excedente pago registrado como USD 0,0213 por GB-mês | armazenamento de objetos parecia economicamente favorável a payloads em comparação com linhas relacionais | não fornece por si só semântica de artefatos independente de provedor |
| Cloudflare R2 | Free e pago | 10 GB-mês gratuitos; 1 milhão de operações Classe A e 10 milhões Classe B gratuitas por mês; armazenamento Standard a USD 0,015 por GB-mês; sem cobrança de egress do R2 | candidato para JSONs e assets imutáveis com API compatível com S3 | oferece armazenamento, não autenticação, metadados transacionais ou política de produto |
| Cloudflare R2 | Acesso | Workers API, APIs compatíveis com S3, CLI e painel | poderia sustentar um adaptador de repositório de artefatos | exige conta, configuração de cobrança e modelagem de número de operações |
| Cloudflare D1 | Free e pago | semântica SQLite; Free com 5 GB totais, 5 milhões de linhas lidas/dia e 100 mil escritas/dia | alternativa possível para implantações pequenas e com scale-to-zero | semântica SQLite e cobrança por linhas exigiriam validação de workload |
| Neon | PostgreSQL Free | 0,5 GB por projeto; 100 CU-hours mensais por projeto; scale-to-zero após inatividade; janela reduzida de restauração | reduz custo de compute quando inativo | não é BaaS completo nem armazenamento de objetos; capacidade gratuita de armazenamento é pequena |
| Neon | PostgreSQL Launch | uso registrado a USD 0,106 por CU-hour e USD 0,35 por GB-mês; restauração de até sete dias | alternativa de PostgreSQL gerenciado com componentes separados | custo mais variável e armazenamento relacional mais caro que armazenamento de objetos no recorte |
| Appwrite | Free | 2 GB de armazenamento; um banco, um bucket e duas funções por projeto; pausa após uma semana de inatividade | alternativa integrada com mais armazenamento gratuito que o Supabase no recorte | limitações e pausa permaneciam; modelo de banco precisava ser validado |
| Appwrite | Pro | a partir de USD 25/mês; 150 GB de armazenamento; bancos, buckets e funções ilimitados; backups diários de sete dias | alternativa integrada paga com armazenamento incluído | migração de semântica PostgreSQL/RLS e operação poderia ser substancial |

Fontes registradas no recorte:

- Supabase Pricing: https://supabase.com/pricing
- Supabase Free Project Pausing: https://supabase.com/docs/guides/platform/free-project-pausing
- Supabase Storage Pricing: https://supabase.com/docs/guides/storage/pricing
- Cloudflare R2 Pricing: https://developers.cloudflare.com/r2/pricing/
- Cloudflare R2 Get Started: https://developers.cloudflare.com/r2/get-started/
- Cloudflare D1 Pricing: https://developers.cloudflare.com/d1/platform/pricing/
- Neon Pricing: https://neon.com/pricing
- Appwrite Pricing: https://appwrite.io/pricing/

## 5. Critérios para investigação futura

Antes de qualquer decisão de infraestrutura, a análise recomenda medir ou estimar explicitamente:

- frequência, tamanho e distribuição das revisões;
- quantidade de objetos e taxa real de reutilização;
- leituras, escritas, listagens e travessias do grafo;
- impacto de índices, WAL, autorização e projeções;
- custo e latência de reconstrução e geração de diferenças;
- funcionamento offline, fila de saída e sincronização;
- backup, restauração e integridade;
- exportação completa e portabilidade;
- retenção e bloqueios de pesquisa;
- custo mensal em cenários pessoais, públicos e institucionais.

## 6. Limitações da evidência

No recorte preservado:

- nenhum gerador de workload havia sido executado;
- nenhum provedor ou mecanismo de armazenamento havia sido selecionado;
- nenhum esquema de produção havia sido definido;
- custo e desempenho permaneciam hipóteses até medição;
- os números de provedores eram temporais e sujeitos a mudança;
- nenhuma evidência deste documento autoriza compra, contratação ou implementação.
