# Evidências sobre perfis de implantação, capacidades e interoperabilidade

**Categoria:** análise de sistema e restrições técnicas  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação histórica sobre como o ARA poderia operar em contextos pessoais, conectados, acadêmicos, formais, institucionais e públicos sem alterar silenciosamente o significado do domínio nem transformar disponibilidade técnica em autoridade.

O material não aprova perfis de implantação, `CapabilityManifest`, registry, packages assinados, catálogo público, modelo de organização ou coorte, OIDC, PostgreSQL, armazenamento S3-compatible, Supabase, CDN, PWA, container, microVM, runtime, schema, política de providers, arquitetura ou implementação. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Problemas distintos

A investigação combinou três frentes que precisam permanecer separadas:

1. **perfil de implantação:** quais capacidades, responsabilidades operacionais e restrições existem em um determinado contexto;
2. **capacidade instalada:** como uma implantação declara, disponibiliza, atualiza, desativa ou deixa indisponível uma função opcional;
3. **interoperabilidade e conformidade:** quais significados e evidências precisam permanecer comparáveis entre implantações diferentes.

Uma implantação mais completa não deve ser tratada automaticamente como semanticamente superior. Da mesma forma, uma capacidade tecnicamente disponível não recebe, por isso, autorização para ser usada, coletar dados ou produzir uma conclusão consequencial.

## 2. Seis perfis históricos de implantação

O material de arquitetura organizou seis perfis históricos. Eles são úteis como casos de contraste, não como catálogo aprovado.

### 2.1 Uso pessoal móvel e offline

O perfil pessoal buscava preservar uso sem conta, sem sincronização obrigatória, sem event store e sem modelo de linguagem obrigatório. Bibliotecas e estado de estudo seriam locais, com exportação e importação opcionais sob controle do usuário.

A implementação histórica sugeria PWA e entrega estática. Essas escolhas não estão aprovadas. O conteúdo residual é a possibilidade de um perfil pessoal continuar funcional sem depender de serviços conectados que não sejam necessários à tarefa.

### 2.2 Uso pessoal ou autoria gerenciada

O perfil conectado acrescentava identidade, sincronização entre dispositivos, workspaces privados e assistência remota à autoria. O desenho histórico citava OIDC, PostgreSQL, armazenamento S3-compatible, Supabase e um gateway GPT+MCP.

Esses mecanismos permanecem alternativas. O problema residual é permitir capacidades conectadas sem tornar identificadores, semântica de domínio ou portabilidade dependentes de um provedor específico.

### 2.3 Pesquisa acadêmica gerenciada

O perfil acadêmico acrescentava governança de participantes, condições de pesquisa, retenção, exportação, auditoria e coleta vinculada ao protocolo.

Isso não aprova plano de dados segregado, banco, event store ou instrumentação de produção. A contribuição é reconhecer que pesquisa exige finalidade, autoridade, versões e evidências próprias e não pode herdar automaticamente dados operacionais ou pessoais.

### 2.4 Ensino formal e coortes

O perfil de ensino formal combinava organizações ou espaços institucionais, atribuições de cursos, papéis docentes, apoio autorizado, políticas de avaliação e acessibilidade.

Um plano de implementação posterior acrescentou como critérios históricos:

- espaços pessoais comuns não herdarem automaticamente bloqueios institucionais;
- avaliação, conclusão estrutural e domínio permanecerem conceitos distintos;
- visibilidade individual depender de finalidade e política;
- dados de acomodação e acessibilidade receberem tratamento protegido;
- perfis institucionais confidenciais restringirem integrações e exportações conforme autoridade aplicável.

A antiga ordem de precedência entre estudante, tutor e instituição não está aprovada. Organizações, coortes, papéis, locks e políticas concretas continuam questões abertas.

### 2.5 Implantação institucional autogerenciada e confidencial

O perfil institucional histórico atribuía à instituição responsabilidades por identidade, armazenamento, chaves, backup, restauração, monitoramento, atualização, rollback e restrição de integrações.

Containerização, PostgreSQL, armazenamento S3-compatible e OIDC controlado pela instituição eram escolhas do desenho histórico. O conteúdo residual é mais geral: uma implantação confidencial precisa tornar explícitas suas responsabilidades operacionais, fronteiras de confiança, restrições de exportação e capacidades ausentes, sem mudar o significado dos objetos do domínio.

### 2.6 Publicação aberta

O perfil público separava publicação e catálogo de autoria privada e dados de participantes. A proposta histórica previa snapshots imutáveis, manifests de licença e proveniência, entrega por CDN ou armazenamento de objetos e canais de retirada ou supersessão.

CDN, formato de snapshot, catálogo e infraestrutura não estão aprovados. Permanecem relevantes a separação entre índice público e dados privados, a apresentação explícita de licença e proveniência e o tratamento não silencioso de retirada e substituição.

## 3. Invariantes candidatos entre perfis

O desenho histórico propôs que perfis diferentes compartilhassem:

- identidades de domínio compatíveis;
- packages ou representações portáveis;
- resolução de configuração compreensível;
- semântica de conformidade comparável.

Também propôs que a ausência de uma capacidade necessária fosse explícita e que capacidades opcionais usassem somente comportamentos alternativos declarados.

Esses pontos são **hipóteses e requisitos de investigação**, não contratos aprovados. Eles precisam ser confrontados com `PARAM-002`, `EXP-009`, `INF-001`, `SYNC-001`, `SYNC-002`, `VAL-001` e `VAL-002` antes de qualquer arquitetura ou formato de interoperabilidade.

## 4. Capacidades instaladas e fronteira de confiança

Um ADR histórico rotulado como aceito propôs um registry confiável de definições versionadas de capacidades. Cursos conteriam dados e requisitos de capacidade, enquanto implementações entrariam na implantação por release revisado ou package instalado por administrador.

A autoridade atual não transforma esse desenho em decisão. O que permanece útil é o conjunto de perguntas que ele tornou explícito. Uma capacidade candidata pode precisar declarar:

- identidade e versão;
- compatibilidade com versões do domínio ou da taxonomia;
- formato de dados e validação;
- fronteira entre renderer, serviço e runtime;
- acessibilidade e alternativas;
- comportamento offline;
- efeitos de segurança, privacidade e custo;
- eventos que pode produzir, sem confundir emissão com autorização de coleta;
- comportamento quando indisponível;
- migração e evidências de conformidade.

Registry, assinatura, formato de package, schema, mecanismo de atualização e política administrativa continuam abertos.

## 5. Código fornecido pelo curso

O material histórico recomendava que cursos não carregassem código arbitrário de aplicação como parte do próprio conteúdo. Essa recomendação buscava reduzir risco de cadeia de fornecimento, expansão silenciosa de permissões e crescimento descontrolado do contexto técnico.

Na orientação atual, isso permanece uma **recomendação de investigação em `EXP-009`**, não decisão arquitetural. Uma análise futura precisa comparar pelo menos:

- catálogo fechado no núcleo;
- capacidades instaladas e aprovadas com versões e permissões explícitas;
- extensões fornecidas pelo conteúdo sob mecanismos adicionais de isolamento e governança.

A existência da recomendação histórica não elimina antecipadamente alternativas que consigam demonstrar segurança, governança, portabilidade, acessibilidade e manutenção adequadas.

## 6. Instalação, atualização, desativação e rollback

O plano histórico de publicação aberta e capacidades controladas tratava instalação, atualização, desativação e rollback como ações governadas. Também exigia que uma capacidade instalada não ampliasse silenciosamente as permissões do curso e que a ausência de uma capacidade opcional não quebrasse fluxos não relacionados.

Esses comportamentos permanecem candidatos. Ainda precisam ser definidos:

- quem possui autoridade para instalar ou habilitar uma capacidade;
- quais verificações antecedem ativação;
- como versões incompatíveis são tratadas;
- como uma capacidade é desativada ou revertida;
- como dependências e falhas ficam visíveis;
- como um curso se comporta quando uma capacidade obrigatória está ausente;
- quando um fallback é permitido e por qual autoridade.

`EXP-009`, `PARAM-002`, `SYNC-001`, `UX-003` e `VAL-002` mantêm essas questões abertas sem escolher mecanismo.

## 7. Catálogo público, autoria e dados de participantes

O plano R5 colocava como requisito histórico a separação entre índice público e dados de workspaces privados ou participantes. Também distinguia adicionar uma publicação à biblioteca de assumir propriedade ou criar cópia oculta.

Na orientação atual:

- `MODEL-005` mantém pendente a semântica de referências, cópias e derivações;
- `PUB-001` mantém pendentes publicação, retirada, supersessão e audiência;
- `PROV-002` mantém pendente o licenciamento explícito de cursos e recursos;
- `DATA-002` mantém governança e direitos de participantes separados da publicação;
- `ACCESS-001` e `ACCESS-002` mantêm visibilidade, autenticação e autorização em investigação.

O lote não aprova catálogo público, índice, marketplace, ranking, modelo editorial ou política de licença.

## 8. Quatro perfis candidatos de execução de programação

Uma matriz técnica separou quatro contextos para execução de código produzido ou utilizado em atividades educacionais. Esses perfis complementam a investigação já preservada sobre fronteiras de confiança.

### 8.1 Execução local sem proteção forte

O perfil local admitia execução apenas como conveniência, com testes públicos, sem alegação de isolamento contra código hostil e sem validação protegida. O uso seria adequado somente quando a finalidade não exigisse segurança ou evidência autoritativa equivalentes a um ambiente protegido.

### 8.2 Host conectado com isolamento candidato

O perfil conectado considerava jobs efêmeros, testes protegidos no host, rede desativada por padrão, armazenamento temporário limitado e limites de CPU, tempo, memória e saída. Container ou microVM apareciam como alternativas após revisão de segurança, não como escolhas.

### 8.3 Serviço autogerenciado sujeito a conformidade

O perfil autogerenciado permitia que o operador fornecesse seu próprio serviço de execução, desde que demonstrasse isolamento, limites e comportamento compatíveis com os critérios definidos. A ausência de uma capacidade precisaria ser declarada, sem downgrade silencioso.

### 8.4 Ferramenta local de autoria

O quarto perfil separava código confiável do autor de código produzido por estudantes. Uma ferramenta de desenvolvimento do autor não deveria ser reutilizada automaticamente como serviço de execução para estudantes.

Esses quatro perfis são candidatos de análise. Eles não aprovam runtime, container, microVM, filesystem, política de rede, limites de recursos ou serviço de execução.

## 9. Execução local e validação protegida

A principal distinção preservada é que **execução funcional não equivale a isolamento nem a autoridade avaliativa**.

Uma implantação pode oferecer execução local para retorno rápido e estudo offline e, ainda assim, não possuir capacidade para validação protegida. Quando isso ocorrer, a indisponibilidade precisa permanecer explícita em vez de ser apresentada como equivalência.

A investigação sobre execução protegida permanece em `MODEL-003`, `EXP-009`, `VAL-002`, `INF-001` e no documento público específico sobre fronteiras de confiança. Nenhum perfil deste lote resolve essa questão.

## 10. Interoperabilidade entre implantações

O corpus usa interoperabilidade em sentidos diferentes, que não devem ser fundidos:

- portabilidade de cursos, referências e artefatos;
- compatibilidade semântica das identidades de domínio;
- comparabilidade de configuração e capacidades;
- conformidade de serviços opcionais;
- interoperabilidade de pesquisa e exportação de evidências.

Uma implementação futura precisa declarar qual desses problemas está resolvendo. A presença de um padrão técnico ou de um serviço equivalente não demonstra, por si só, equivalência de significado, autoridade, acessibilidade, privacidade ou evidência.

`DATA-003` trata especificamente interoperabilidade de pesquisa. `INF-001` mantém portabilidade e factibilidade abertas. `EXP-009` trata governança de capacidades. `PARAM-002` mantém disponibilidade e fallback separados de autoridade normativa.

## 11. Planos de implementação superados

As issues históricas R4 e R5 foram encerradas sem implementação quando o projeto retornou ao pré-desenvolvimento.

Por isso, não permanecem vigentes:

- releases R4 e R5;
- critérios executáveis de fechamento;
- modelo concreto de organização, workspace, coorte ou matrícula;
- ordem histórica de precedência;
- provider allowlist ou denylist;
- OIDC, PostgreSQL, S3-compatible ou Supabase;
- catálogo público e seu schema;
- registry de capacidades;
- packages assinados;
- `CapabilityManifest`;
- container ou microVM;
- CDN ou topologia de publicação;
- runtime ou serviço de execução;
- arquitetura ou implementação.

Somente problemas, invariantes candidatos, alternativas e restrições permanecem úteis.

## 12. Não autorizações

Este documento não seleciona:

- perfil padrão de implantação;
- stack diferente por perfil;
- provedor gerenciado ou autogerenciado;
- identidade ou autorização federada;
- banco ou armazenamento de objetos;
- mecanismo de catálogo ou distribuição pública;
- formato de package ou manifesto;
- assinatura ou registry;
- política de instalação, atualização ou rollback;
- container, microVM, sandbox ou runtime;
- padrão de interoperabilidade;
- schema, API, interface ou implementação.

A contribuição preservada é mais limitada: contextos de implantação podem exigir capacidades, responsabilidades e restrições diferentes, mas essas diferenças precisam permanecer explícitas, portáveis quando necessário e compatíveis com autoridade, direitos, proveniência, funcionamento offline e evidências de conformidade.