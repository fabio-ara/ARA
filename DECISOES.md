# Registro de decisões do projeto ARA

Este arquivo contém decisões aprovadas e suas consequências. Alternativas, hipóteses e questões ainda abertas permanecem no backlog até que haja decisão.

## DEC-001 - Método canônico de pesquisa, decisão e documentação

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

Um projeto que integra computação, educação e investigação empírica exige rastreabilidade entre questões, evidências, alternativas, decisões, requisitos e validação.

### Decisão

Adotar um método canônico, com backlog único, atualização coordenada das fontes vigentes e auditoria de consistência ao final de cada tópico.

### Consequências

- ideias novas são preservadas sem se tornarem automaticamente requisitos;
- decisões aprovadas substituem formulações incompatíveis;
- documentos novos só são criados quando possuem função estável e não redundante;
- itens de implementação dependem de especificação e critérios de aceite suficientes.

### Item relacionado

- `GOV-001`

---

## DEC-002 - Português do Brasil como língua canônica

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

A documentação deve ser tecnicamente rigorosa e, ao mesmo tempo, compreensível para leitores das áreas de educação, tecnologias digitais e computação.

### Decisão

Usar português do Brasil em toda a documentação canônica, com definição de termos especializados e explicações didáticas quando necessárias.

### Consequências

- não haverá versões canônicas concorrentes em outros idiomas;
- termos estrangeiros estabelecidos poderão ser empregados, desde que definidos;
- a redação deve servir a pesquisadores, educadores, avaliadores e profissionais de tecnologia.

### Item relacionado

- `LANG-001`

---

## DEC-003 - Composição inicial da interface desktop

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Contexto

Foi validada uma composição para navegador desktop com navegação de pastas e cursos no painel esquerdo e o grafo de revisões do curso na área principal.

### Decisão

Adotar essa composição como direção aprovada da interface desktop. O painel esquerdo deve apresentar os cursos visíveis ao usuário.

### Consequências

- o artefato visual correspondente deverá ser preservado no registro de telas aprovadas;
- decisões posteriores de interação devem respeitar essa composição, salvo revisão explícita.

### Item relacionado

- `UX-001`

---

## DEC-004 - Grafo principal somente no nível do curso

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

Grafos simultâneos em diferentes níveis hierárquicos podem tornar a navegação difícil e prejudicar a compreensão da evolução do curso.

### Alternativas consideradas

1. grafos recursivos em todos os níveis;
2. grafo do objeto hierárquico selecionado;
3. grafo principal somente para revisões completas do curso.

### Decisão

O grafo principal será renderizado somente no nível do curso. Cada nó representa uma revisão completa e utilizável. Os níveis internos continuam versionados, mas são apresentados por hierarquia, composição, diferenças e proveniência.

### Consequências

- não haverá grafos principais recursivos;
- derivações e consolidações serão representadas entre revisões de curso;
- alterações internas continuarão identificáveis e comparáveis.

### Item relacionado

- `VER-001`

---

## DEC-005 - Histórico deliberativo e histórico materializado

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

Nem toda proposta, análise, observação ou decisão produz uma alteração efetiva no conteúdo educacional. Confundir deliberação com materialização comprometeria a precisão do histórico.

### Decisão

Distinguir:

- **histórico materializado:** revisões completas do curso produzidas por alterações confirmadas e persistidas;
- **histórico deliberativo:** propostas, reformulações, decisões, auditorias, achados e observações relevantes, mesmo quando não produzem revisão.

### Consequências

- toda mutação efetivamente aplicada cria nova revisão do curso;
- propostas rejeitadas ou reformuladas não criam revisão;
- o processo deliberativo pode ser relacionado à materialização que eventualmente produziu;
- a distinção permite estudar processos de autoria, curadoria e qualidade sem alterar o significado técnico de revisão.

### Item relacionado

- `PROV-001`

---

## DEC-006 - Tese de produto e continuidade funcional

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

A evolução do projeto precisa preservar comportamentos demonstrados pela experiência anterior sem transformar sua implementação ou configuração em modelo universal.

### Decisão

Tratar o ARA como sucessor direto do AraLearn e como plataforma educacional aberta, configurável, mobile-first e preparada para funcionamento offline.

O AraLearn permanece como primeira referência funcional e caso de contraste. Essa continuidade não determina a arquitetura interna do ARA nem obriga que a primeira configuração seja adotada em todos os contextos.

A inteligência artificial pode assistir à autoria, à auditoria e ao reparo, mas não recebe autoridade para aprovar ou publicar sua própria saída.

### Consequências

- comportamentos funcionais demonstrados devem ser preservados ou reformulados explicitamente;
- componentes internos e escolhas técnicas do sistema anterior não são herdados automaticamente;
- configurações e capacidades podem variar por contexto, desde que mantenham controle humano e rastreabilidade;
- estudo offline e uso em dispositivos móveis modestos permanecem requisitos de qualidade.

### Item relacionado

- `SCOPE-001`

---

## DEC-007 - Pré-desenvolvimento e gate de implementação

**Estado:** aprovada  
**Data:** 6 de agosto de 2026

### Problema

Rascunhos de backlog, protótipos, estudos de arquitetura e planos de release podem ser confundidos com autorização para desenvolvimento.

### Decisão

Manter o ARA em pré-desenvolvimento enquanto estiverem em curso a pesquisa, a definição do produto, a consolidação do backlog e a exploração de design.

A entrada em desenvolvimento exige:

1. decisão explícita do responsável pelo projeto;
2. revisão das bases conceituais e técnicas vigentes;
3. escolha do primeiro recorte implementável;
4. criação de itens executáveis novos, com requisitos, dependências e critérios de aceite atuais.

### Consequências

- propostas, protótipos e itens candidatos não autorizam código;
- planos de implementação superados não orientam o trabalho atual;
- a visão integral do produto, o primeiro recorte de implementação, a avaliação acadêmica e a adoção institucional permanecem escopos distintos;
- a factibilidade deve ser investigada continuamente sem reduzir prematuramente a visão integral.

### Item relacionado

- `SCOPE-002`
