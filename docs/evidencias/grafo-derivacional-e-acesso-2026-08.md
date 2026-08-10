# Evidências para grafo derivacional e acesso

**Categoria:** levantamento comparativo e cenários de análise  
**Recorte temporal:** 5 de agosto de 2026  
**Estado:** histórico, não normativo

Este documento preserva a investigação que comparou mecanismos de visibilidade hierárquica, atenuação de autoridade, autorização relacional, proveniência, grafos de versões e edição local para avaliar um possível modelo de acesso em derivações do ARA.

A investigação não demonstra que exista um sistema consolidado com o comportamento integral proposto para o ARA. Os precedentes sustentam mecanismos parciais. Em especial, a hipótese de que uma revogação em um ancestral possa bloquear um descendente para seu próprio autor derivado é uma escolha de desenho a validar, não uma consequência universal das fontes examinadas.

Nenhum modelo de ACL, mecanismo de autorização, biblioteca de grafo, schema ou stack é selecionado aqui. As decisões vigentes sobre grafo e histórico permanecem em [`DECISOES.md`](../../DECISOES.md); as questões abertas permanecem em [`BACKLOG.yaml`](../../BACKLOG.yaml).

## 1. Pergunta investigada

A investigação examinou se uma interface simples de visibilidade e audiência poderia coexistir com um grafo de derivações no qual restrições de acesso acompanhassem as origens necessárias sem exigir do usuário a administração direta de ACLs, policies, branches ou estruturas técnicas equivalentes.

A formulação técnica candidata usada no estudo foi **controle de acesso derivacional com atenuação monotônica**. Esse termo não é vocabulário público aprovado do produto.

## 2. Precedentes examinados

| Frente | Fonte | Observação relevante | Limite para o ARA |
|---|---|---|---|
| Visibilidade hierárquica | GitLab, project and group visibility | Projetos e subgrupos não podem exceder a visibilidade do grupo pai | O comportamento de revogação em descendentes proposto para o ARA não é o mesmo mecanismo do GitLab |
| Guardrails | AWS Organizations, service control policies | Políticas superiores funcionam como limites máximos e permissões efetivas dependem das restrições aplicáveis | O domínio é autorização em contas de nuvem, não artefatos educacionais derivados |
| Guardrails | AWS IAM policy evaluation logic | Permissões efetivas podem resultar da interseção de políticas; negações explícitas prevalecem | A superfície de uso pretendida para o ARA é muito menor |
| Atenuação | RFC 7521 | Escopo solicitado ou emitido não deve exceder o escopo originalmente concedido | Escopos de credenciais não definem grafos de proveniência de conteúdo |
| Atenuação | RFC 6749, OAuth 2.0 | Renovação não pode solicitar escopo não concedido originalmente | Não define ancestrais de conteúdo nem audiência derivacional |
| Atenuação | Macaroons | Credenciais delegadas podem receber caveats que restringem autoridade | A investigação não exige adoção de credenciais macaroon |
| Fluxo de informação | Decentralized Label Model | Políticas associadas à informação podem acompanhar processamento e transformação | O ARA necessita de um modelo de aplicação mais simples |
| Dados derivados | A Policy Framework for Data Fusion and Derived Data Control | Examina restrições aplicáveis a informações derivadas de múltiplas fontes | O modelo precisa ser adaptado a artefatos educacionais versionados |
| Autorização relacional | Zanzibar | Demonstra autorização baseada em relações em escala muito elevada | Reproduzir essa complexidade seria prematuro para o ARA |
| Autorização relacional | OpenFGA modeling guides | Documenta acesso público, relações pai-filho e combinação de restrições | É referência de modelagem, não escolha de implementação |
| Proveniência | W3C PROV-O | Representa entidades, atividades, agentes e relações de derivação | Exige especialização para o domínio e linguagem de interface do ARA |
| DAG de versões | Git data model | Commits e objetos são imutáveis e revisões apontam para pais e snapshots | O ARA precisa acrescentar semântica educacional e regras de acesso |
| DAG de versões | Git glossary | O grafo de commits é um DAG formado por commits relacionados | A terminologia Git não precisa ser exposta ao usuário |
| Versionamento sobre objetos | lakeFS model | Mantém commits, referências e histórico sobre armazenamento de objetos | É um sistema de data lake, não uma plataforma educacional nem BaaS |
| Versionamento sobre objetos | lakeFS FAQ | Criação de branch pode ser somente de metadados e novos objetos aparecem quando há alterações | O ARA ainda precisaria tratar acesso granular e funcionamento offline |
| Local-first | Local-first software | Defende trabalho local, operação offline, colaboração, posse dos dados e preservação | Não define checkpoints nem semântica de acesso |
| Histórico operacional | Microsoft Event Sourcing pattern | Eventos append-only favorecem auditoria, com custo relevante de complexidade | Sustenta estudar registro seletivo de operações, não event sourcing integral |
| Modelos de leitura | Microsoft Materialized View pattern | Projeções pré-computadas podem reduzir o custo de consultas derivadas | Introduzem custos próprios de armazenamento e consistência |
| Interface de grafo | Mermaid flowchart interaction | Nós podem ter callbacks e links em grafos declarativos | Interatividade rica e escala exigem avaliação; não é solução completa de exploração |
| Interface de grafo | Cytoscape.js | Oferece visualização e análise de grafos, eventos, travessia, layouts e viewport | Exige trabalho próprio de UX e avaliação de desempenho |
| Interface de grafo | React Flow | Oferece nós customizáveis, seleção e controles de viewport | Análise de grafo e layout automático dependem de complementos |
| Layout de grafo | ELK.js | Oferece algoritmos de layout, inclusive em Web Workers | É motor de layout, não renderer nem interface completa |

Fontes registradas no recorte:

- GitLab project and group visibility: https://docs.gitlab.com/user/public_access/
- AWS Organizations SCPs: https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- AWS IAM policy evaluation logic: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html
- RFC 7521: https://www.rfc-editor.org/rfc/rfc7521.html
- RFC 6749: https://www.rfc-editor.org/rfc/rfc6749.html
- Macaroons: https://research.google/pubs/macaroons-cookies-with-contextual-caveats-for-decentralized-authorization-in-the-cloud/
- Decentralized Label Model: https://doi.org/10.1145/363516.363526
- Derived Data Control: https://doi.org/10.1145/2875491.2875492
- Zanzibar: https://research.google/pubs/zanzibar-googles-consistent-global-authorization-system/
- OpenFGA modeling guides: https://openfga.dev/docs/modeling
- W3C PROV-O: https://www.w3.org/TR/prov-o/
- Git data model: https://git-scm.com/docs/gitdatamodel.html
- Git glossary: https://git-scm.com/docs/gitglossary.html
- lakeFS model: https://docs.lakefs.io/v1.81/understand/model/
- lakeFS FAQ: https://docs.lakefs.io/understand/faq/
- Local-first software: https://www.inkandswitch.com/essay/local-first/
- Microsoft Event Sourcing pattern: https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing
- Microsoft Materialized View pattern: https://learn.microsoft.com/en-us/azure/architecture/patterns/materialized-view
- Mermaid flowchart interaction: https://mermaid.js.org/syntax/flowchart.html
- Cytoscape.js: https://js.cytoscape.org/
- React Flow: https://reactflow.dev/
- ELK.js: https://github.com/kieler/elkjs

## 3. Modelo candidato, sem autoridade de decisão

A investigação combinou as fontes acima em uma hipótese de produto com estas propriedades candidatas:

- cada objeto ou revisão aplicável poderia declarar visibilidade pública ou privada;
- um objeto privado poderia identificar pessoas e grupos autorizados;
- um descendente poderia restringir a audiência recebida das origens necessárias, mas não ampliá-la silenciosamente;
- múltiplos pais e contêineres poderiam impor uma interseção de restrições;
- revogação em uma origem poderia bloquear acesso a descendentes dependentes sem apagar o histórico;
- restauração do acesso poderia reativar descendentes retidos, conforme política futura;
- estado de acesso e existência histórica do artefato seriam responsabilidades distintas.

Nada nesta formulação define o padrão de visibilidade, o modelo de grupos, exceções de desclassificação, metadata visível em nós bloqueados, política de reativação ou mecanismo de autorização. Esses pontos permanecem pendentes.

## 4. Cenários candidatos para validação

Os cenários abaixo são casos de análise do modelo, não critérios de aceite aprovados.

| Cenário | Configuração explorada | Resultado esperado no modelo estudado | Questão exercitada |
|---|---|---|---|
| Raiz pública | revisão A pública | acesso para todos | audiência de uma origem pública |
| Raiz privada | A privada para autora, Ana e grupo X | autora, Ana e membros vigentes de X | compartilhamento privado ordinário |
| Derivação pública para privada | A pública, B privada para Ana | Ana acessa B | descendente restringe audiência |
| Subconjunto privado | A privada para Ana e Bruno, B derivada para Ana | Ana acessa B | seleção de subconjunto |
| Tentativa de ampliação | A privada para Ana, B solicita Ana e Carlos | Carlos é rejeitado no modelo candidato | proibição de ampliar audiência herdada |
| Revogação em cascata | A privada para Ana, B criada por Ana, depois Ana é removida de A | Ana perde acesso efetivo a A e B | ausência de bypass automático por autoria derivada |
| Reativação | acesso de Ana a A é restaurado | B pode voltar a ficar acessível se sua própria política ainda incluir Ana | preservação do grafo durante bloqueio |
| Múltiplos pais | C deriva de A e B | audiência limitada pelas origens necessárias e pela própria política de C | composição de restrições |
| Contêiner privado | curso privado e card declarado público | card não excede a audiência do curso no modelo candidato | teto imposto pelo contêiner |
| Snapshot de pesquisa | membros de grupo mudam após início de uma condição experimental | análise utiliza snapshot explicitamente fixado pelo protocolo | separação entre acesso operacional e evidência de pesquisa |

## 5. Consequências para investigação

Antes de qualquer decisão, o modelo precisa ser confrontado com:

- significado de autoria, propriedade, licença e responsabilidade sobre derivações;
- comportamento esperado quando o autor de um descendente perde acesso à origem necessária;
- privacidade e minimização da metadata exibida sobre artefatos bloqueados;
- grupos dinâmicos, snapshots e alterações de participação;
- múltiplos pais, consolidações e exceções autorizadas;
- retirada, revogação, supersessão, retenção e exclusão física;
- funcionamento offline e acesso revogado enquanto um artefato está materializado localmente;
- custos de cálculo, invalidação e cache de audiência efetiva;
- usabilidade da superfície pública/privada e das listas de acesso;
- necessidades institucionais e jurídicas que possam exigir modelos adicionais.

A evidência comparativa sustenta investigar o modelo. Ela não sustenta tratá-lo como decisão já aprovada.