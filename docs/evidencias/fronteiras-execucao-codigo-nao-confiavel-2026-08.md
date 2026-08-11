# Evidências sobre execução de código e fronteiras de confiança

**Categoria:** análise de sistema e restrição técnica  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação técnica sobre atividades educacionais em que o estudante produz código executável. O problema central não é apenas fazer o código rodar. É distinguir execução funcional, autoridade de validação, proteção de testes, isolamento do host, limites de recursos e evidência diagnóstica.

O material não aprova runtime, linguagem, biblioteca, sandbox, container, microVM, provedor, arquitetura de backend, schema ou política operacional. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Execução não equivale a segurança nem a avaliação

A investigação separou sete responsabilidades:

1. resposta de código produzida pelo estudante;
2. validação pública;
3. validação protegida;
4. serviço de execução;
5. garantia de isolamento;
6. política de recursos;
7. evidência diagnóstica.

Essa separação evita dois atalhos incorretos:

- um editor ou renderer de código não recebe autoridade implícita para executar;
- um runtime capaz de executar corretamente não recebe autoridade implícita para proteger o host nem para produzir avaliação completa.

A resposta do estudante deve permanecer conceitualmente independente do runtime concreto usado para executá-la.

## 2. Validação pública e validação protegida

A investigação tratou testes públicos e protegidos como capacidades distintas.

### Validação pública

Pode ser adequada para:

- retorno rápido durante o estudo;
- uso local ou offline após a disponibilidade do runtime;
- exemplos e testes conhecidos pelo estudante;
- verificação de baixo risco que não dependa de segredos.

Um resultado produzido apenas por esse caminho não deve ser apresentado como equivalente a uma avaliação protegida quando a atividade exigir material oculto ou uma fronteira de segurança mais forte.

### Validação protegida

Quando a atividade depender de testes não expostos ao estudante, a proposta histórica separou o conteúdo do curso da suíte protegida. O curso poderia referenciar uma suíte por identificador opaco, enquanto código, entradas e respostas esperadas permaneceriam fora do artefato distribuído ao estudante.

A evidência devolvida deveria oferecer critérios e diagnósticos úteis sem permitir a reconstrução indevida do material protegido.

Identificadores, formatos de referência e mecanismos de distribuição continuam em aberto.

## 3. Execução local e funcionamento offline

Runtimes locais ou de navegador foram considerados úteis para:

- retorno imediato;
- estudo offline após o download das capacidades necessárias;
- testes públicos;
- visualizações e experimentação;
- atividades de ciência computacional que possam operar integralmente no dispositivo.

Essa utilidade não demonstra automaticamente:

- isolamento contra código hostil;
- segredo de testes;
- limites uniformes de memória entre navegadores ou dispositivos;
- governança adequada de pacotes;
- resistência a abuso;
- equivalência com execução autoritativa em ambiente protegido.

A consequência metodológica é que disponibilidade local, segurança e autoridade avaliativa precisam ser analisadas separadamente.

## 4. Ambiente confiável como hipótese para validação protegida

A investigação registrou como hipótese que validação protegida, quando necessária, exige uma fronteira de execução mais forte do que um runtime funcional embutido no cliente.

Um ambiente candidato desse tipo deveria permitir avaliar, entre outros critérios:

- execução efêmera;
- isolamento revisado;
- imagem ou conjunto de pacotes versionado;
- rede desativada por padrão quando não necessária;
- base somente leitura quando aplicável;
- armazenamento temporário limitado;
- limites de CPU, tempo, memória e saída;
- cancelamento garantido;
- separação entre testes protegidos e conteúdo distribuído;
- redação de diagnósticos para evitar exposição indevida;
- coleta mínima e governada de logs.

Esses pontos são critérios de investigação. Eles não aprovam arquitetura centralizada, serviço gerenciado, container, microVM ou qualquer tecnologia de isolamento.

## 5. Perfis de implantação e degradação explícita

A análise histórica considerou que implantações diferentes podem oferecer capacidades diferentes.

### Perfil local ou pessoal

Pode oferecer apenas execução local e validação pública. A ausência de validação protegida precisa aparecer como capacidade indisponível, não como equivalência silenciosa.

### Perfil conectado

Pode acrescentar um serviço de execução protegido, desde que sua garantia de isolamento, limites, evidências e operação sejam verificáveis.

### Perfil autogerenciado

Pode implementar um serviço de execução que satisfaça critérios de conformidade ou desativar a validação protegida. A ausência da capacidade não deve ser mascarada por um mecanismo mais fraco apresentado como equivalente.

### Ferramenta local de autoria

Execução de código confiável pelo próprio autor pertence a uma fronteira de confiança diferente da execução de código produzido por estudantes. Credenciais, permissões e infraestrutura não devem ser compartilhadas automaticamente entre esses contextos.

Os perfis concretos de implantação permanecem questão do domínio de implantação e interoperabilidade.

## 6. Reprodutibilidade da execução autoritativa

A investigação propôs que uma execução usada como evidência autoritativa registre informações suficientes para reprodução e auditoria, como:

- linguagem e versão;
- imagem, pacote ou identificação do runtime;
- digest do ambiente quando aplicável;
- bibliotecas permitidas;
- limites efetivamente aplicados;
- localização da validação;
- versão da suíte de testes;
- política de evidência e diagnóstico.

Esses campos são candidatos. Não constituem schema aprovado nem política de retenção.

## 7. Resultados negativos e alternativas abertas

A investigação registrou dois resultados negativos específicos do recorte analisado:

- Web Worker não foi considerado fronteira produtiva suficiente contra código hostil;
- Node `vm` não foi considerado fronteira produtiva suficiente contra código hostil.

Essas conclusões devem ser lidas apenas como rejeição desses mecanismos para a função de sandbox produtiva naquele recorte. Elas não proíbem seu uso legítimo para isolamento funcional, responsividade, testes locais ou outros papéis que não façam alegação de segurança equivalente.

Container e microVM apareceram apenas como categorias de trabalho para isolamento mais forte. Nenhuma delas foi selecionada.

Runtimes de navegador, inclusive soluções voltadas a Python ou outras linguagens, permaneceram alternativas para retorno local e estudo offline, não garantias automáticas de segurança.

## 8. Critérios residuais dos planos de implementação superados

Planos de implementação posteriormente encerrados continham critérios técnicos que continuam úteis como perguntas de factibilidade, mas não como itens executáveis.

Entre eles estavam:

- separar domínio e serviços de aplicação dos adaptadores de infraestrutura;
- verificar builds e ambientes de forma reproduzível;
- manter diagnóstico explícito de versões e capacidades;
- ensaiar backup, restauração, migração e rollback;
- testar consistência entre metadados e inventários de artefatos sob falha;
- permitir implantações gerenciadas e autogerenciadas sem introduzir semântica específica de fornecedor no domínio;
- evitar IDs de fornecedor como identidade dos objetos do domínio;
- preservar um caminho pessoal sem conta conectada quando a capacidade remota não for necessária;
- impedir acesso direto do cliente a detalhes físicos de persistência quando isso violar as fronteiras da aplicação.

Esses critérios já estão cobertos pelas pendências vigentes de infraestrutura, acesso, versionamento, proveniência, dados e validação. Os antigos releases, dependências e critérios executáveis não permanecem ativos.

## 9. Relação com as pendências vigentes

Na orientação atual:

- `MODEL-003` mantém separadas representação, prática, resposta, validação e retorno pedagógico;
- `PED-004` mantém acessibilidade e equivalência de interação como questão transversal;
- `EXP-009` mantém a governança de capacidades instaladas e impede assumir código arbitrário fornecido pelo curso como capacidade automaticamente confiável;
- `VAL-002` mantém separadas validade da entrada, satisfação de critérios, disponibilidade de capacidade, autoridade e evidência;
- `INF-001` mantém abertas infraestrutura, desempenho, segurança, custo, armazenamento, backup, restauração e factibilidade;
- `ACCESS-002` mantém autenticação e autorização conectadas separadas da implementação física;
- `DATA-002` e `DATA-003` mantêm governança de logs, eventos e evidências separada da infraestrutura;
- `DEC-007` impede que os antigos itens de implementação ou esta investigação autorizem desenvolvimento.

Nenhum novo item de backlog é necessário para preservar esta frente no estágio atual. Uma decisão futura sobre execução protegida deve depender de threat model específico, critérios de conformidade, custos operacionais, requisitos pedagógicos e de avaliação, funcionamento offline, acessibilidade e comparação entre alternativas de isolamento.

## 10. Não autorizações

Este documento não seleciona:

- Web Worker ou Node `vm` como sandbox de produção;
- container ou microVM;
- Pyodide, Papyros ou outro runtime de navegador;
- linguagem ou versão de runtime;
- host gerenciado ou autogerenciado;
- formato de suíte protegida;
- schema de execução ou evidência;
- política de coleta ou retenção de logs;
- limites de CPU, memória, tempo, armazenamento ou saída;
- provedor, banco, object storage, OIDC, BaaS ou stack;
- fluxo de interface para avaliação protegida;
- implementação.

A contribuição preservada é a separação das fronteiras de confiança e dos tipos de evidência necessários para que execução de código educacional não seja confundida com segurança ou autoridade avaliativa.