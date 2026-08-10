# Evidências sobre arquitetura, infraestrutura e factibilidade

**Categoria:** análise de arquitetura, infraestrutura e factibilidade técnica  
**Recorte temporal:** 3 a 5 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação histórica sobre como estruturar a infraestrutura do ARA sem transformar restrições de um primeiro recorte, preferências tecnológicas ou características de um provedor em invariantes permanentes do produto.

O material não aprova linguagem de programação, framework, formato de cliente, banco de dados, armazenamento local, armazenamento de objetos, provedor de identidade, BaaS, topologia de sincronização, arquitetura de pacotes, runtime, schema físico ou stack. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

A investigação chegou a registrar uma arquitetura de referência e escolhas técnicas como aceitas naquele estágio histórico. Na orientação vigente, esses rótulos não possuem autoridade própria. `DEC-006` mantém a experiência anterior como referência funcional, não arquitetura obrigatória, e `DEC-007` mantém o projeto em pré-desenvolvimento.

## 1. Quatro categorias que não devem ser confundidas

Um resultado metodológico importante da investigação foi separar quatro categorias.

### 1.1 Requisitos duráveis do produto

A arquitetura histórica tratou como candidatos duráveis propriedades como:

- continuidade funcional reconhecível sem herança automática da implementação anterior;
- estudo orientado a dispositivos móveis e recuperação após interrupções;
- funcionamento offline para capacidades pertinentes ao perfil adotado;
- conteúdo e configuração portáveis e versionados;
- comportamento determinístico e testável quando a capacidade assim o permitir;
- pesquisa com condições reproduzíveis e governança explícita;
- acessibilidade, segurança, privacidade e proveniência;
- independência semântica em relação a provedores;
- backup, restauração, diagnóstico, migração e rollback verificáveis;
- extensibilidade governada, sem crescimento silencioso do núcleo.

A presença nesta lista histórica não transforma cada formulação em requisito aprovado. Quando existe uma orientação vigente equivalente, sua autoridade vem das decisões e itens atuais do projeto.

### 1.2 Restrições do primeiro recorte implementável

A investigação separou de propósito restrições que poderiam ser úteis apenas para uma primeira implementação, entre elas:

- avaliar desempenho em um dispositivo móvel modesto de referência;
- manter o estudo básico utilizável sem modelo de linguagem ou API conectada em tempo real;
- preferir contratos pequenos, fechados e validáveis localmente no primeiro recorte;
- priorizar práticas e retorno pedagógico determinísticos quando suficientes;
- evitar runtimes pesados no pacote inicial até existir necessidade demonstrada;
- preservar um caminho simples entre autoria assistida, estudo offline, observação, reparo e auditoria.

Essas formulações são hipóteses de recorte, não proibições permanentes nem requisitos de release aprovados.

### 1.3 Capacidades dependentes do contexto de implantação

A investigação também registrou que uso pessoal, pesquisa acadêmica, ensino formal, operação institucional confidencial e publicação aberta podem impor necessidades diferentes de infraestrutura, dados, disponibilidade, operação e governança.

O resultado residual é a necessidade de explicitar quais capacidades e obrigações dependem do contexto. A definição dos perfis concretos de implantação permanece uma questão própria de implantação e interoperabilidade, não uma decisão de infraestrutura estabelecida por este documento.

### 1.4 Hipóteses técnicas

Foram tratadas como hipóteses a comparar:

- topologia local-first, híbrida ou outra combinação de persistência local e conectada;
- divisão entre dados relacionais, artefatos imutáveis e projeções no dispositivo;
- Supabase ou outro serviço gerenciado como adaptador;
- IndexedDB ou outra persistência local;
- mecanismos de sincronização e resolução de conflitos;
- packages, registries ou outros mecanismos de extensão;
- formatos físicos de artefatos e schemas;
- provedores de identidade e autorização;
- transporte e armazenamento de eventos analíticos;
- cliente web estático, PWA, wrapper nativo ou outra forma de empacotamento;
- runtimes locais opcionais e gateways de serviços conectados;
- estratégias de cache e materialização offline.

A principal restrição é que nenhuma tecnologia seja selecionada apenas porque foi usada anteriormente ou porque um sistema externo a utiliza.

## 2. Alternativa histórica de cliente web instalável

Um registro arquitetural histórico escolheu, para o primeiro recorte, a seguinte combinação:

- monorepositório com TypeScript em modo estrito;
- cliente React com Vite;
- aplicação web progressiva instalável;
- service worker para shell e recursos offline;
- divisão do bundle por autoria, pesquisa e capacidades opcionais;
- separação entre objetos do framework e pacotes de domínio;
- HTML acessível e aprimoramento progressivo.

O racional registrado incluía ecossistema de testes e manutenção, suporte amplo a componentes e estado, acesso a recursos de navegador para funcionamento offline, uma base de código comum para diferentes contextos e possibilidade de troca futura do framework.

Também foram rejeitados naquele estágio JavaScript sem tipagem estrita, cliente exclusivamente nativo, acoplamento entre framework e domínio e um único bundle contendo todas as capacidades opcionais.

Na orientação atual, TypeScript, React, Vite, PWA, service worker, monorepositório e essas rejeições são **alternativas e argumentos históricos**, não stack aprovada.

## 3. Alternativa histórica de topologia híbrida de armazenamento

Outro registro arquitetural histórico propôs combinar:

- IndexedDB para projeção local estruturada, manifests, estado de estudo e fila de saída;
- Cache API para shell da aplicação e recursos versionados;
- OPFS apenas como adaptador opcional para arquivos grandes quando medições justificassem;
- PostgreSQL para metadados, relações, políticas e registros operacionais conectados;
- armazenamento compatível com S3 para versões imutáveis de conteúdo, snapshots de publicação e assets.

O racional era evitar dois extremos: colocar todo conteúdo em linhas relacionais ou colocar toda semântica e todos os metadados em objetos JSON isolados.

A proposta também registrou princípios que permanecem úteis como critérios de investigação:

- identificadores de domínio não devem depender de chaves físicas ou IDs de versão do provedor;
- integridade entre diferentes meios de armazenamento precisa ser verificável;
- manifests e digests podem relacionar artefatos e metadados;
- backup e restauração precisam conferir referências cruzadas;
- um provedor gerenciado pode implementar adaptadores sem definir a semântica do domínio.

IndexedDB, Cache API, OPFS, PostgreSQL, armazenamento S3-compatible e Supabase não estão selecionados pela orientação vigente.

## 4. Fronteiras arquiteturais investigadas

A arquitetura histórica organizou responsabilidades em fronteiras que continuam úteis para comparar alternativas, ainda que sua implementação concreta esteja aberta.

### Núcleo de domínio e aplicação

O núcleo deveria preservar identidades, versões, configuração, validação, estados e intenções de autorização sem importar diretamente detalhes de framework, banco, armazenamento ou fornecedor.

### Projeção local

Uma projeção local poderia materializar versões de curso, snapshots de configuração, manifests de capacidades e estado funcional para uso offline. A investigação considerou desejável que essa projeção fosse reconstruível a partir de artefatos portáveis e operações locais ainda não sincronizadas.

### Metadados e relações

Índices mutáveis, relações, referências, políticas e registros operacionais podem ter características diferentes das versões imutáveis de conteúdo. A fronteira física entre essas classes permanece aberta.

### Artefatos imutáveis

O estudo considerou armazenar objetos completos e assets de forma imutável, identificados por versão ou digest. O mecanismo físico de versionamento do provedor não deveria substituir a identidade semântica das versões do ARA.

### Pacotes portáveis

Pacotes portáveis foram tratados como dados canônicos transportáveis, e não como dumps de banco de dados. A investigação associou a esses pacotes manifests de versões, conteúdo, composição, configuração, capacidades, assets, proveniência, licenças e migrações.

A forma concreta, a granularidade, o formato e o mecanismo de empacotamento continuam em investigação.

## 5. Integridade, instalação e ciclo operacional

O pacote histórico registrou vários critérios operacionais independentes da escolha de uma tecnologia específica:

- materialização ou ativação deve ser verificável antes de substituir uma versão funcional;
- falha de capacidade não deve produzir fallback silencioso nem corromper fluxos não relacionados;
- migrações devem ser explícitas e, quando possível, reversíveis;
- backup deve cobrir todos os meios necessários à reconstrução lógica;
- restauração precisa ser ensaiada e verificar referências entre stores;
- diagnósticos devem tornar visíveis versões de aplicação, pacotes, armazenamento, sincronização e capacidades pertinentes;
- caminhos de compatibilidade e fallback precisam ser documentados;
- portabilidade deve ser verificada por comportamento e artefatos, não apenas por equivalência de fornecedor.

Esses pontos são critérios de investigação e qualidade. Não aprovam topologia, ferramentas operacionais, formato de backup ou mecanismo de migração.

## 6. Dezoito budgets históricos de qualidade e factibilidade

A investigação produziu dezoito valores e condições para orientar ensaios. Eles são preservados como **pontos históricos de benchmark**, não como requisitos aprovados, SLAs ou critérios de aceite atuais.

| Contexto histórico | Métrica ou propriedade | Valor ou condição investigada | Forma de verificação proposta |
|---|---|---|---|
| estudo pessoal | shell inicial compactado | até 1,5 MiB, excluindo capacidades opcionais carregadas sob demanda | relatório do artefato de build |
| estudo pessoal | interação a frio em dispositivo da classe Galaxy A07 | até 5 s sob perfil declarado de rede e dispositivo | benchmark em dispositivo físico |
| estudo pessoal | transição de card após materialização, p95 | até 100 ms | rastreamento de desempenho |
| estudo pessoal | memória de trabalho do estudo | até 180 MiB, excluindo overhead do navegador | amostragem em dispositivo físico |
| estudo pessoal | shell offline | todas as rotas e ações básicas utilizáveis após instalação | teste de jornada sem conexão |
| pacote de curso | aviso de tamanho | aviso acima de 50 MiB e divulgação antes do download | fixture de pacote |
| pacote de curso | ativação atômica | manter versão válida anterior até a nova verificação terminar | injeção de falha |
| sincronização | replay idempotente | requisição duplicada produz uma única operação aplicada | teste de contrato |
| sincronização | visibilidade de conflito | 100% dos conflitos de revisão detectados produzem estado explícito | fixture de conformidade |
| autoria assistida | limite de resposta de ferramenta | paginação e limites configurados de bytes e entidades | fixture ou teste de carga |
| pesquisa gerenciada | workload pequeno | 100 participantes por até 10 mil eventos autorizados cada | ensaio de capacidade |
| pesquisa gerenciada | workload médio | 1.000 participantes por até 50 mil eventos autorizados cada | modelo de capacidade antes de qualquer alegação |
| todos os contextos | acessibilidade | alvo histórico WCAG 2.2 AA para jornadas aprovadas | auditoria automatizada e manual |
| todos os contextos | expansão de idioma | fluxos críticos sem truncamento inacessível nas variantes então previstas | testes visuais e com tecnologia assistiva |
| autogerenciado | backup e restauração | RPO e RTO declarados por implantação e ensaio de restauração aprovado | ensaio operacional |
| todos os contextos | segurança | nenhuma vulnerabilidade crítica ou alta não aceita no gate de release | scans e revisão de ameaças |
| todos os contextos | portabilidade | conformidade equivalente entre contextos gerenciados e autogerenciados | suíte de conformidade |
| todos os contextos | falha de disponibilidade | ausência de fallback silencioso ou perda de dados quando capacidade ou serviço falhar | injeção de falha |

Alguns valores pertencem parcialmente a outros domínios, como sincronização, acessibilidade, pesquisa e implantação. Eles foram mantidos juntos porque formavam um único registro histórico de factibilidade. Qualquer reutilização futura deve reavaliar o recorte, a autoridade, o dispositivo, a carga, a forma de medição e o primeiro recorte realmente aprovado.

## 7. Auditoria histórica e limites

A auditoria interna do pacote registrou ausência de bloqueadores e marcou como `passed` a separação entre requisitos duráveis e primeiro recorte, a definição de perfis, o encaminhamento de hipóteses para registros arquiteturais, a rastreabilidade, as fronteiras offline, os limites da autoria conectada, a independência de provedor, os budgets, o dispositivo de referência, o ciclo operacional e o plano de conformidade.

Esse resultado significa somente coerência documental e arquitetural interna do pacote histórico. A própria auditoria registrou limitações:

- decisões de arquitetura ainda exigiriam benchmarks de implementação antes de qualquer alegação de escalabilidade;
- UX e terminologia permaneceriam por definir;
- warehouses especializados, CRDTs, uso de OPFS como primeira opção e runtimes pesados permaneceriam adiados.

Não houve implementação de produto capaz de validar os budgets, a escalabilidade, a segurança operacional, o comportamento offline completo ou a adequação da stack.

## 8. Relação com as pendências vigentes

Na orientação atual:

- `INF-001` mantém aberta a investigação de infraestrutura, armazenamento, banco de dados, portabilidade, custo, desempenho, backup, restauração e workloads;
- `SCOPE-002` mantém o projeto em pré-desenvolvimento e impede que este pacote autorize implementação;
- `SCOPE-005` mantém extensibilidade governada como questão de pesquisa;
- `EXP-005` mantém compatibilidade e migração com a experiência anterior sem solução aprovada;
- `EXP-009` mantém governança de capacidades instaladas e proíbe assumir código arbitrário fornecido pelo curso;
- `VER-002` mantém checkpoints, revisões duráveis e restauração como questões abertas;
- `PROV-004` mantém proveniência operacional e retenção sustentável abertas;
- `DATA-002` e `DATA-003` mantêm governança e instrumentação de pesquisa separadas da infraestrutura física;
- `ACCESS-002` mantém autenticação e autorização conectadas como investigação própria;
- `AGENT-001` mantém configuração e avaliação de agentes sem selecionar gateway, provedor ou modelo;
- `VAL-001` e `VAL-002` mantêm corpus, estados e evidências de validação abertos;
- `DEC-006` impede herança automática da arquitetura anterior;
- `DEC-007` impede interpretar qualquer baseline histórico como autorização para implementação.

A arquitetura histórica local-first híbrida permanece, portanto, uma alternativa tecnicamente articulada e documentada, não a arquitetura vigente do ARA.

## 9. Evolução da investigação de versionamento e armazenamento

Uma primeira formulação da frente de armazenamento organizou dez perguntas de investigação:

1. inventário de objetos versionados;
2. fronteira entre metadados relacionais, artefatos e estado local;
3. endereçamento por conteúdo e deduplicação;
4. manifests e materialização;
5. retenção e garbage collection condicionadas por referências, direitos e protocolos;
6. workloads e simulação de custo em ordens de 10 mil, 100 mil e 1 milhão de revisões;
7. comparação entre formas de implantação;
8. disponibilidade, pausa, degradação de serviço e continuidade offline;
9. backup, exportação e restauração independentes de fornecedor;
10. administração compreensível de espaço, crescimento, retenção, custo estimado, objetos órfãos e consequências de limpeza.

Uma revisão posterior ampliou o enquadramento. Versionamento deixou de ser tratado prioritariamente como problema de armazenamento e passou a ser analisado primeiro como suporte à autoria reversível, à preservação de erros e reparos, à investigação longitudinal e transversal, à fixação de condições de pesquisa, à derivação colaborativa e ao funcionamento offline. Somente depois dessas necessidades deveriam ser avaliadas granularidade física, mecanismos de persistência, retenção e custo.

A revisão posterior substitui a primeira como leitura conceitual mais completa, mas a preocupação inicial com **administração compreensível do armazenamento e consequências de limpeza** permanece um requisito de investigação útil que não deve ser perdido.

As famílias físicas de versionamento e armazenamento comparadas nessa evolução já estão preservadas em `versionamento-e-armazenamento-2026-08.md`. Nenhuma delas foi selecionada.

## 10. Mapa histórico de trinta alternativas tecnológicas

Uma etapa de idealização estruturou trinta alternativas em nove camadas. Os rótulos então usados, como `candidate`, `recommended`, `candidate-baseline`, `principal-hypothesis`, `defer` ou equivalentes, registravam a leitura daquela rodada. Eles não têm autoridade de decisão vigente.

| Camada | Alternativa histórica | Papel ou questão então considerada |
|---|---|---|
| backend | Supabase | continuidade operacional e possível primeiro adaptador conectado |
| backend | Firebase | alternativa móvel e gerenciada a comparar apenas se houvesse benefício específico |
| backend | Appwrite | BaaS integrado e autogerenciável para ensaio comparativo |
| backend | Nhost | alternativa baseada em PostgreSQL e GraphQL para ensaio de portabilidade |
| backend | PocketBase | opção simples para cenários pessoais ou autogerenciados pequenos |
| backend | PostgreSQL + S3-compatible + OIDC/API própria | referência de maior independência com maior custo operacional |
| perfil | somente local | hipótese para uso pessoal com custo remoto mínimo e colaboração posterior |
| armazenamento local | IndexedDB direto | alternativa nativa de navegador e continuidade com experiência anterior |
| armazenamento local | Dexie | camada sobre IndexedDB para reduzir complexidade de transações e consultas |
| armazenamento local | RxDB | banco local-first com replicação e maior complexidade de dependência |
| armazenamento local | SQLite com OPFS | alternativa relacional local que exige avaliar WASM, workers e compatibilidade |
| armazenamento local | PGlite | PostgreSQL no navegador, sujeito a medição de memória, inicialização e maturidade |
| sincronização | protocolo específico do ARA | alternativa com semântica de operações controlada pelo produto |
| sincronização | PowerSync | serviço de sincronização baseado em SQLite a comparar por custo, licença e adequação |
| sincronização | replicação RxDB | alternativa cliente-servidor com pull, push e checkpoints |
| sincronização | ausência de sync genérico no primeiro recorte | hipótese de reduzir risco inicial por packages e exportação/importação |
| hospedagem | GitHub Pages | hospedagem estática de demonstração, sem autoridade sobre o domínio |
| hospedagem | outro host HTTPS estático | alternativa institucional ou independente de provedor para o mesmo artefato |
| aplicação | PWA | hipótese de uma aplicação web instalável com base de código comum |
| aplicação | Trusted Web Activity ou empacotador equivalente | wrapper Android mínimo sobre experiência web hospedada |
| aplicação | Capacitor | contêiner web com acesso a capacidades nativas quando justificadas |
| interface | ESM/Web Components | alternativa de baixo overhead e maior orquestração manual |
| interface | React + TypeScript | alternativa de ecossistema de componentes, tipos e testes |
| interface | Vue ou Svelte | alternativas de framework a comparar por manutenção, tamanho e ecossistema |
| carregamento de capacidades | packages definidos no build | alternativa de maior previsibilidade e segurança, com rebuild para alterações |
| carregamento de capacidades | packages oficiais sob demanda | alternativa para reduzir bundle inicial com custo de cache e versionamento |
| carregamento de capacidades | packages assinados em runtime | hipótese de ecossistema instalável com riscos de supply chain e compatibilidade |
| artefatos | objetos imutáveis endereçados por conteúdo | hipótese de integridade e deduplicação com maior complexidade de lifecycle |
| artefatos | JSON integral de curso | alternativa simples, mas potencialmente grosseira e duplicadora |
| artefatos | manifesto de curso com revisões de unidades | hipótese de reutilização e atualização granular que exige resolução de referências |

Esse mapa não constitui ranking técnico nem recomendação atual. Ele demonstra a amplitude do espaço considerado e ajuda a evitar que uma escolha histórica de stack seja confundida com identidade do produto.

## 11. Evidência temporal de fornecedores e critérios de revalidação

A investigação registrou preços, quotas, políticas de pausa e capacidades de serviços gerenciados em agosto de 2026. Esses dados são evidência histórica e instável. O retrato detalhado de Supabase, Cloudflare R2/D1, Neon e Appwrite está preservado em `versionamento-e-armazenamento-2026-08.md`.

Qualquer decisão futura deve revalidar pelo menos:

- preços e unidades de cobrança;
- quotas de banco, arquivos, egress, operações e computação;
- política de pausa e retomada;
- backup, point-in-time recovery e janelas de restauração;
- limites de funções, mensagens, conexões e usuários quando pertinentes;
- condições de self-hosting e suporte operacional;
- mecanismos de exportação e saída do fornecedor;
- licenças e condições de bibliotecas ou serviços de sincronização;
- disponibilidade real das APIs e capacidades citadas no recorte histórico.

O plano gratuito de um serviço não deve definir a semântica do produto, e o plano pago de um serviço não resolve por si só retenção, portabilidade, deduplicação, recuperação, disponibilidade ou custo operacional humano.

## 12. Critérios consolidados para comparação futura

A evolução dessa frente reforça que uma decisão de infraestrutura deve ser precedida por comparação verificável de:

- comportamento observável e dependências do primeiro recorte realmente aprovado;
- cargas de 10 mil, 100 mil e 1 milhão de revisões ou ordens equivalentes justificadas por cenário;
- número e tamanho de objetos, relações, índices, leituras, escritas e listagens;
- CPU, memória, WAL ou mecanismo equivalente e custo de índices quando aplicável;
- latência, egress, requests e integridade de armazenamento de artefatos;
- funcionamento offline, materialização e recuperação de estado local;
- retenção por referências, bloqueios de pesquisa e garbage collection;
- backup, restauração e ensaio de migração para alternativa independente de fornecedor;
- custo mensal de infraestrutura e custo operacional humano;
- acessibilidade, privacidade, segurança, disponibilidade e comportamento de falha;
- complexidade da alternativa mais simples capaz de atender ao cenário.

A recomendação residual é metodológica: medir primeiro e selecionar depois. Nenhuma topologia, provider, plano, banco, armazenamento local, armazenamento de objetos, engine de sincronização, framework, cliente ou runtime está aprovado por esta evidência.
