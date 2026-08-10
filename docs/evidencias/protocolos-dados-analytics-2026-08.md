# Evidências sobre protocolos, dados de pesquisa e analytics

**Categoria:** evidência de concepção metodológica, levantamento de referências e análise de sistemas  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva evidências usadas para investigar como o ARA pode apoiar pesquisa educacional reproduzível sem transformar toda atividade de estudo em coleta de dados.

O material não aprova objetos de domínio, campos, eventos, medidas, instrumentos, fórmulas, limiares, políticas jurídicas, padrões de interoperabilidade, banco de dados, schema, event store, LRS, warehouse, dashboard, modelo preditivo, arquitetura, interface, stack, coleta com participantes ou implementação. As decisões vigentes continuam sendo registradas exclusivamente em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Problema investigado

A investigação partiu de uma tensão central: o ARA deve poder sustentar estudos quantitativos, qualitativos, mistos e de desenvolvimento, mas também deve continuar útil em estudo pessoal com coleta mínima.

A disponibilidade técnica de um evento não autoriza sua coleta. A existência de um registro operacional também não o transforma automaticamente em evidência educacional. Para reduzir esse risco, o levantamento separou a seguinte cadeia conceitual:

```text
pergunta e finalidade
→ protocolo
→ condição e atribuição
→ evento autorizado ou instrumento
→ evidência
→ medida
→ construto
→ interpretação
→ decisão ou intervenção
```

Nenhuma camada deve ser inferida automaticamente da anterior. Em particular, tempo, número de tentativas, uso de pistas, navegação ou conclusão estrutural não demonstram por si só atenção, esforço, dificuldade, domínio ou aprendizagem.

## 2. Conceitos candidatos para protocolos reproduzíveis

O modelo histórico explorou conceitos para representar:

- pergunta de pesquisa e finalidade;
- protocolo versionado;
- condição e variante;
- participante e modo de identidade;
- atribuição a condição;
- definição de evento;
- definição e instância de instrumento;
- definição de medida;
- definição de construto;
- regra de interpretação;
- registro de evidência;
- pacote de pesquisa com proveniência e limitações.

Esses conceitos são candidatos analíticos, não entidades ou schemas aprovados.

Uma condição reproduzível foi investigada como um snapshot capaz de relacionar, quando pertinente:

- versões de conteúdo e composição;
- configuração efetiva;
- capacidades disponíveis e comportamentos alternativos autorizados;
- instrumentos e agenda de administração;
- eventos e propriedades cuja coleta foi autorizada;
- dimensões bloqueadas pela condição;
- acomodações ou exceções exigidas por direitos;
- desvios observados e limitações de comparabilidade.

Rótulos como randomizado, contrabalanceado, quase experimental ou causal só são metodologicamente defensáveis quando os respectivos requisitos de desenho forem satisfeitos. Uma acomodação exigida por direitos não deve ser tratada automaticamente como falha do participante; seu efeito sobre comparabilidade e interpretação precisa ser documentado.

## 3. Governança de dados investigada

Foram registradas quinze regras históricas de governança. Elas preservam problemas e salvaguardas a decidir, não uma política jurídica vigente.

| Tema | Regra investigada | Autoridade ou momento relevante | Comportamento diante de falha |
|---|---|---|---|
| Vinculação à finalidade | Cada elemento de dado deve estar ligado a finalidade explícita e pergunta vigente | antes de autorizar coleta ou uso | bloquear coleta ou uso sem finalidade definida |
| Minimização | Somente eventos e propriedades declarados devem ser autorizados | snapshot da condição | rejeitar dados adicionais não previstos |
| Consentimento | Registrar estado e versão quando consentimento for base jurídica ou requisito ético aplicável | antes de coleta ou uso | não coletar ou isolar até resolução adequada |
| Retirada | Interromper coleta prospectiva e aplicar a política declarada de retenção ou eliminação | mediante solicitação | colocar dados afetados em tratamento controlado |
| Modo de identidade | Declarar se a classe de dados é anônima, pseudonimizada ou identificada | antes de participação | bloquear mapeamento de identidade não resolvido |
| Retenção | Toda classe de dados precisa de duração ou regra baseada em evento | aprovação do protocolo | impedir retenção indefinida sem finalidade |
| Acesso | Papel, finalidade, escopo e auditoria precisam estar explícitos | antes de divulgação | negar por padrão quando não autorizado |
| Exportação | Finalidade, campos, identificadores, formato e destinatário devem estar definidos | antes da exportação | gerar pacote reduzido ou negar |
| Uso secundário | Requer finalidade compatível e aprovações aplicáveis | antes de reutilização | negar reutilização não autorizada |
| Pseudonimização | Separar chaves e autoridade de reidentificação | antes do armazenamento | não chamar dado pseudonimizado de anônimo |
| Dados sensíveis | Dados de acessibilidade, acomodação, identidade e material qualitativo requerem acesso restrito | transversalmente | minimizar e separar conforme sensibilidade |
| Separação operacional | Logs operacionais não são analytics educacionais por padrão | coleta e consulta | manter finalidade e uso separados |
| Transparência ao participante | Explicar dados, finalidade, acesso, retenção e direitos | antes da participação | não iniciar coleta sem informação adequada |
| Incidentes | Definir contenção, notificação e auditoria para incidentes de dados de pesquisa | antes de uso com participantes | suspender o fluxo afetado |
| Equivalência entre implantações | Registrar versão semântica, perdas de mapeamento e evidência de conformidade | antes de agregar resultados | não combinar dados semanticamente incomparáveis |

O levantamento também registrou que dados pseudonimizados continuam podendo ser dados pessoais. A conclusão jurídica depende de finalidade, jurisdição, contexto institucional e revisão qualificada; esta consolidação não estabelece base legal, texto de consentimento ou política regulatória específica.

## 4. Quatro autoridades de analytics

A investigação distinguiu quatro finalidades que não devem compartilhar autoridade automaticamente:

| Superfície | Finalidade candidata | Restrição principal |
|---|---|---|
| Pessoal | reflexão privada e gestão do próprio estudo | adesão e visibilidade não implicam acesso institucional ou de pesquisa |
| Pedagógica | perguntas formativas autorizadas para ensino ou tutoria | não autoriza vigilância individual ou ranking por padrão |
| Pesquisa | evidência vinculada a protocolo e condição | coleta, acesso, retenção e interpretação dependem do protocolo |
| Operacional | confiabilidade, sincronização, disponibilidade e segurança | não deve ser reutilizada como analytics educacionais sem nova finalidade autorizada |

O perfil histórico de estudo pessoal foi data-minimal: estado funcional necessário para continuidade e escolhas explícitas, sem exigir histórico central de tentativas, tempo, navegação ou interações com IA. Esse perfil é referência candidata, não regra universal.

## 5. Vocabulário histórico de eventos

Foram examinados vinte e quatro eventos candidatos. Os identificadores abaixo são históricos e não constituem API ou contrato vigente.

| Identificador histórico | Uso que motivou o registro | Inferência explicitamente proibida ou limitada |
|---|---|---|
| `session.started` | contexto de início ou retomada | não demonstra atenção ou engajamento |
| `session.ended` | fechamento explícito ou timeout | não determina tempo de tarefa sem regra de atividade |
| `study.resumed` | continuidade funcional | não demonstra persistência ou motivação |
| `card.presented` | denominador de exposição quando autorizado | não demonstra leitura ou atenção |
| `practice.response_submitted` | evidência de resposta | não demonstra domínio isoladamente |
| `practice.feedback_shown` | fidelidade de tratamento | não demonstra compreensão |
| `practice.answer_revealed` | fidelidade da condição | não demonstra aprendizagem |
| `practice.hint_requested` | uso de apoio | não demonstra dificuldade |
| `progression.status_changed` | estado funcional ou fidelidade de protocolo | não demonstra domínio sem definição separada |
| `review.scheduled` | estado de agenda | não mede força de memória |
| `review.deferred` | gestão de fila ou agenda | não demonstra desengajamento |
| `annotation.created` | evidência qualitativa ou fluxo de trabalho | não mede gravidade de defeito sem codificação |
| `annotation.resolved` | estado de fluxo | não demonstra correção por si só |
| `artifact.revision_created` | proveniência de autoria | não mede qualidade |
| `artifact.review_completed` | processo de qualidade | não demonstra efetividade educacional |
| `artifact.published` | proveniência de publicação | não implica visibilidade pública sem audiência explícita |
| `configuration.snapshot_created` | reprodutibilidade | não demonstra equivalência de implementação |
| `condition.assigned` | registro de atribuição | não autoriza o rótulo randomizado sem método correspondente |
| `instrument.administered` | momento e fidelidade de instrumento | não produz escore válido sem modelo de pontuação |
| `consent.status_changed` | estado de direitos | nunca é resultado educacional |
| `withdrawal.requested` | estado de direitos | nunca é comportamento adverso do participante |
| `sync.completed` | saúde operacional e conformidade | não é analytics educacional |
| `sync.conflict_detected` | qualidade de dados e operação | não descreve comportamento do estudante |
| `capability.unavailable` | disponibilidade e fidelidade | não mede desempenho do estudante |

## 6. Medidas candidatas e restrições de interpretação

Foram registradas dezesseis medidas candidatas. As fórmulas e nomes são evidência do espaço analisado, não definições aprovadas.

| Medida histórica | Definição investigada | Uso permitido no recorte | Uso proibido ou inadequado |
|---|---|---|---|
| Conclusão estrutural | colocações obrigatórias concluídas / colocações obrigatórias elegíveis | descrever conclusão e fidelidade | aprendizagem, domínio ou competência |
| Acerto na primeira resposta | primeiras respostas válidas corretas / primeiras respostas válidas elegíveis | desempenho descritivo sob política declarada | habilidade, domínio ou efeito causal |
| Acerto na resposta final | respostas finais válidas corretas / respostas finais elegíveis | resultado descritivo sob política de tentativas e revelação | comparação entre políticas incompatíveis |
| Número de tentativas | contagem de respostas válidas submetidas | fluxo e carga de interação | esforço, persistência ou dificuldade |
| Exposição a feedback | feedback exibido / práticas elegíveis concluídas | fidelidade de tratamento | compreensão |
| Conclusão de revisões agendadas | revisões concluídas / revisões elegíveis agendadas | descrição de fila e fidelidade | retenção ou motivação |
| Resultado tardio | regra de pontuação de instrumento aplicado após atraso declarado | retenção quando instrumento for apropriado | inferir retenção a partir de eventos da plataforma |
| Tempo ativo | soma de intervalos ativos sob regra declarada de inatividade | carga operacional ou exposição, com limitações | atenção, engajamento ou esforço |
| Uso de pistas | ocorrências com pedido de pista / práticas elegíveis | descrição de uso de apoio | dificuldade ou dependência |
| Latência de resolução de observação | tempo entre criação e resolução | operação de autoria | qualidade da revisão ou competência do autor |
| Número de revisões de artefato | contagem de revisões semânticas distintas | fluxo, custo e proveniência | qualidade |
| Cobertura de consentimento | participantes com consentimento ativo / participantes que o exigem | auditoria de governança | disposição para participar |
| Latência de processamento de retirada | tempo entre pedido e conclusão do processamento | conformidade operacional | satisfação do participante |
| Taxa de dados ausentes | observações elegíveis ausentes / observações elegíveis | qualidade de dados e planejamento analítico | assumir ausência aleatória |
| Desvios de fidelidade | contagem de desvios verificados da condição | interpretação e análise de sensibilidade | classificar automaticamente como não conformidade do participante |
| Armazenamento por participante | bytes de pesquisa autorizados armazenados / participantes ativos | planejamento de capacidade e custo | valor dos dados |

Toda medida candidata precisa, antes de uso, explicitar pergunta, fórmula, denominador quando aplicável, unidade, unidade de análise, janela, entradas, tratamento de dados ausentes, limitações e uso permitido.

## 7. Famílias históricas de instrumentos

O levantamento registrou quatorze famílias de instrumentos como exemplos do espaço metodológico.

| Família | Momento ou uso investigado | Limite relevante |
|---|---|---|
| Pré-teste de conhecimento | antes da exposição à condição | traduções não validadas não são intercambiáveis |
| Pós-teste de conhecimento | imediatamente após a condição | conclusão estrutural não substitui aprendizagem |
| Teste tardio de conhecimento | após atraso declarado | eventos de revisão não substituem resultado tardio |
| Escala de autorregulação | conforme protocolo | não inferir autorregulação de rastros de interação |
| Questionário de usabilidade | após tarefa ou período | percepção de usabilidade não é efetividade educacional |
| Item ou escala de carga cognitiva | após tarefa | autorrelato não é capacidade cognitiva objetiva |
| Julgamento de confiança | após resposta ou item | confiança não é competência isoladamente |
| Avaliação por rubrica | após tarefa ou artefato | requer processo de avaliadores e adjudicação adequados |
| Entrevista semiestruturada | momento agendado | evidência interpretativa não representa prevalência quantitativa |
| Grupo focal | momento agendado | participação em grupo não produz anonimato |
| Diário | cadência declarada | registro não equivale a comportamento diretamente observado |
| Observação estruturada | sessão ou tarefa | não revela estado interno do participante |
| Análise de artefatos | conjunto versionado de artefatos | não é resultado de aprendizagem por si só |
| Inspeção de usabilidade | protótipo ou versão | avaliação especializada não substitui estudo com usuários |

A lista não determina quais instrumentos devem ser usados em uma dissertação, estudo ou avaliação futura.

## 8. Cenários de coerência conceitual

Doze cenários foram marcados historicamente como `passed`. O resultado significa somente que o modelo analisado conseguiu representar o cenário de forma coerente. Não é validação empírica, jurídica, de usabilidade, desempenho ou produção.

| Cenário | Questão examinada | Resolução histórica |
|---|---|---|
| Estudo pessoal mínimo e offline | ausência de protocolo de pesquisa | somente estado funcional local; analytics pessoais desligados |
| Analytics reflexivos privados | adesão pessoal explícita | visibilidade privada e controles de exportação ou eliminação |
| Comparação entre participantes | variantes versionadas e atribuição | rótulo randomizado apenas quando houver alocação aleatória real |
| Comparação intraparticipante | ordem, período e carryover | plano analítico inclui ordem e dependência por participante |
| Pesquisa qualitativa e de desenvolvimento | entrevistas e artefatos versionados | contagens de eventos não substituem interpretação qualitativa |
| Ensino formal | agregados formativos autorizados | sem ranking ou vigilância individual por padrão |
| Desvio por acessibilidade | acomodação modifica condição bloqueada | direito preservado; limitação de comparabilidade documentada |
| Retirada | participante retira-se após coleta parcial | coleta prospectiva cessa; destino dos dados segue política declarada |
| Pesquisa offline | dados autorizados são sincronizados depois | conflito e fidelidade ficam separados de resultados educacionais |
| Falha de capacidade conectada | IA ou instrumento conectado indisponível | comportamento alternativo precisa ser previamente autorizado ou ficar indisponível |
| Agregação entre implantações | cenários gerenciados e autogerenciados | combinar apenas campos e medidas com evidência de equivalência semântica |
| Dados ausentes diferentes entre condições | missingness diferencial | não assumir análise causal simples por casos completos |

## 9. Interoperabilidade e pacotes de pesquisa

Foram identificados mapeamentos candidatos para interoperabilidade:

- Caliper e xAPI para eventos;
- QTI para itens e testes de avaliação;
- DDI para metadados de estudos, instrumentos e variáveis;
- PROV-O para proveniência;
- RO-Crate para pacotes portáveis de pesquisa;
- DPV para finalidade, processamento, papéis, retenção, direitos e medidas de privacidade.

Esses padrões não definem a semântica interna do ARA e podem exigir mapeamentos parciais ou com perdas. Nenhum foi adotado como contrato obrigatório.

Um pacote de pesquisa candidato incluiria, conforme a finalidade, referências ao protocolo e às versões relevantes, dicionário de dados, mapeamentos semânticos, definições de medidas, classificação de dados ausentes, proveniência, classe de acesso, artefatos exportados e limitações. A forma concreta continua aberta.

## 10. Corpus de referências preservado

O levantamento reuniu vinte e quatro fontes ou antecedentes. A tabela preserva a organização do corpus sem transformar a presença de uma fonte em recomendação de adoção.

| Fonte ou antecedente | Categoria de procedência | Papel na investigação | Limite de uso |
|---|---|---|---|
| Taxonomia histórica de configuração do ARA | evidência de concepção | perfis, precedência, snapshots e restrições de interpretação | autoridade histórica, não decisão vigente |
| Experiência de desenvolvimento do AraLearn | experiência de desenvolvimento | estado funcional mínimo, offline, autoria em etapas e publicação explícita | referência funcional, não arquitetura universal |
| 1EdTech Caliper Analytics 1.2 | especificação oficial | vocabulário e perfis de eventos, conformidade | mapeamento candidato, não domínio do ARA |
| Experience API (xAPI) 2.0 | especificação oficial | statements e LRS para interoperabilidade | mapeamento candidato; semântica compartilhada depende de perfis |
| W3C Data Privacy Vocabulary | especificação comunitária | finalidade, processamento, papéis, retenção, direitos e riscos | vocabulário candidato, não política jurídica do ARA |
| W3C PROV-O | recomendação | proveniência de entidades, atividades e agentes | mapeamento candidato |
| W3C Web Annotation Data Model | recomendação | comentários qualitativos e ancoragem de evidências | precedente de representação |
| OSF Registries e preregistration | orientação institucional | registro de protocolos e snapshots imutáveis | referência metodológica, não requisito universal |
| CONSORT | diretriz de relato | transparência em estudos randomizados | aplicável apenas a desenhos pertinentes |
| SPIRIT | diretriz de protocolo | conteúdo de protocolos intervencionais | aplicável apenas a estudos pertinentes |
| APA Journal Article Reporting Standards | diretriz de relato | pesquisa quantitativa, qualitativa e mista | referência metodológica |
| FAIR Principles | princípios comunitários | organização e reutilização de produtos de pesquisa | sujeito a governança e direitos |
| RO-Crate | especificação comunitária | manifests e proveniência de pacotes de pesquisa | mapeamento candidato |
| DataCite Metadata Schema | schema oficial | identificação e citação de pacotes exportados | candidato para metadados, não modelo de domínio |
| Autoridade Nacional de Proteção de Dados do Brasil | orientação regulatória | finalidade, salvaguardas e transparência em pesquisa | exige análise jurídica contextual |
| Regulamento Geral sobre a Proteção de Dados da União Europeia | legislação | limitação de finalidade, minimização, direitos e segurança | aplicação depende de jurisdição e contexto |
| NIST Privacy Framework 1.0 | framework oficial | identificação, governança, controle, comunicação e proteção de riscos | referência de governança |
| NIST AI Risk Management Framework 1.0 | framework oficial | governança e supervisão de riscos de IA | referência transversal, não regra educacional |
| WCAG 2.2 | recomendação | acessibilidade de instrumentos e superfícies analíticas | baseline técnico a confrontar com necessidades educacionais |
| 1EdTech QTI | especificação oficial | interoperabilidade de itens e testes | não constitui modelo completo de pesquisa |
| DDI Lifecycle | especificação oficial | metadados de estudo, instrumento, variável e ciclo de dados | mapeamento candidato |
| RFC 3339 | padrão técnico | representação de timestamps e fusos | utilidade técnica, não semântica educacional |
| padrões HTTP pertinentes | padrões técnicos | metadados de transporte | não definem significado educacional |
| Open edX Aspects/OARS | sistema implementado | precedente de transporte xAPI, LRS e separação de analytics | evidência comparativa, não escolha de arquitetura |

Os endereços consultados no levantamento histórico incluem:

- `https://www.1edtech.org/standards/caliper`
- `https://github.com/adlnet/xAPI-Spec`
- `https://w3id.org/dpv/`
- `https://www.w3.org/TR/prov-o/`
- `https://www.w3.org/TR/annotation-model/`
- `https://www.cos.io/initiatives/prereg`
- `https://www.consort-statement.org/`
- `https://www.spirit-statement.org/`
- `https://apastyle.apa.org/jars`
- `https://www.go-fair.org/fair-principles/`
- `https://www.researchobject.org/ro-crate/`
- `https://schema.datacite.org/`
- `https://www.gov.br/anpd/`
- `https://eur-lex.europa.eu/eli/reg/2016/679/oj`
- `https://www.nist.gov/privacy-framework`
- `https://www.nist.gov/itl/ai-risk-management-framework`
- `https://www.w3.org/TR/WCAG22/`
- `https://www.1edtech.org/standards/qti`
- `https://ddialliance.org/Specification/DDI-Lifecycle/`
- `https://www.rfc-editor.org/rfc/rfc3339`
- `https://www.rfc-editor.org/`
- `https://docs.openedx.org/projects/openedx-aspects/`

Esses endereços registram o corpus consultado no recorte histórico. Informações temporais ou normativas que possam ter mudado precisam ser revalidadas antes de decisões futuras, conforme `RES-002`.

## 11. Alternativa arquitetural histórica

Uma proposta arquitetural separava estado pessoal básico, telemetria operacional e evidência de pesquisa, com um plano de dados segregado para eventos e instrumentos autorizados. A proposta mencionava PostgreSQL separado por schema ou banco e adiava LRS ou warehouse especializado até existirem workloads representativos.

Essa proposta não é decisão arquitetural vigente. O conteúdo residual a preservar é o problema: dados operacionais e evidência de pesquisa podem ter finalidades, direitos, acesso, retenção e riscos diferentes e precisam ser tratados de forma verificável. Banco, schema, topologia, mecanismo de separação e tecnologia permanecem para investigação de infraestrutura.

## 12. Limites da validação histórica

A auditoria do pacote registrou ausência de bloqueadores apenas para consistência conceitual e metodológica. Foram verificadas separação de camadas, representabilidade de protocolos e condições, instrumentos quantitativos e qualitativos, governança, metadados de medidas, exportação, inferências proibidas e cenários de custo.

O resultado não demonstrou:

- efetividade educacional;
- validade de qualquer construto ou instrumento específico;
- conformidade jurídica de um estudo concreto;
- adequação ética em uma instituição ou jurisdição;
- usabilidade com pesquisadores, educadores ou participantes;
- escalabilidade ou segurança de produção;
- equivalência semântica real entre duas implantações;
- desempenho de event store, LRS, warehouse ou banco de dados;
- qualidade de qualquer dashboard ou modelo preditivo.

Não houve estudo com participantes nem implementação de analytics de produção.

## 13. Destino atual

Na orientação vigente:

- `DATA-001` deve manter aberta a definição de protocolos, condições, atribuição, snapshots e desvios reproduzíveis;
- `DATA-002` deve manter aberta a governança de dados, finalidade, minimização, identidade, direitos, retenção, acesso, exportação e uso secundário;
- `DATA-003` deve manter aberta a definição de eventos, instrumentos, medidas, construtos, analytics e interoperabilidade;
- `PED-003` continua limitando inferências a partir de respostas, tempo, tentativas e rastros;
- `PROV-004` continua separando proveniência operacional de uso em pesquisa;
- `VAL-001` e `VAL-002` continuam tratando corpus de validação, estados, evidências e limites;
- `PARAM-001` e `PARAM-002` continuam responsáveis por taxonomia, autoridade e snapshots de configuração;
- `ACCESS-002` continua responsável por autenticação e autorização conectada;
- infraestrutura física e implantação permanecem sem decisão técnica;
- `DEC-006` e `DEC-007` continuam impedindo herança automática da arquitetura anterior e qualquer autorização implícita de implementação.
