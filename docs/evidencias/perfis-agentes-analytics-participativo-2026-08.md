# Evidências sobre perfis de agentes, curadoria participativa e analytics assistidos

**Categoria:** levantamento bibliográfico, análise de sistema e concepção metodológica  
**Recorte temporal:** 4 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação inicial sobre configuração de agentes, avaliação de suas operações, curadoria participativa e análise quantitativa, qualitativa e mista no ARA.

O material não aprova perfis de agentes, objetos de domínio, campos, eventos, métricas, taxonomias, rubricas, fixtures, modelos, provedores, MCP, base vetorial, motor de analytics, dashboard, banco de dados, schema, arquitetura, interface, coleta com participantes ou implementação. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Problema investigado

A experiência funcional anterior demonstrou que assistência por inteligência artificial pode participar de planejamento, construção, auditoria, reparo e reauditoria de cursos declarativos. A investigação examinou como preservar essa continuidade funcional sem herdar uma configuração monolítica nem confundir a implementação anterior com a arquitetura interna futura do ARA.

Foram exploradas, como dimensões separadas:

- instruções do agente;
- papel operacional;
- perfil de domínio;
- coleções de conhecimento;
- templates de tarefa;
- recursos e ferramentas conectadas;
- política de contexto;
- escopo de escrita;
- modelo e provedor;
- rubricas e avaliações;
- configuração efetiva versionada;
- observações participativas;
- evidência operacional;
- análises posteriores.

A disponibilidade de contexto não concede autoridade para mutação. Da mesma forma, uma observação, um evento, uma medida ou uma codificação analítica não se transforma automaticamente em conclusão pedagógica ou científica.

## 2. Correção posterior sobre a referência funcional e os evals

Uma correção posterior do próprio levantamento restringiu interpretações excessivas da primeira síntese.

A referência funcional anterior oferece:

- jornadas reais de estudo, autoria, auditoria e reparo;
- problemas observados de acoplamento entre instruções, conhecimento e ferramentas;
- exemplos de operações assistidas;
- casos negativos e padrões de uso úteis como contraste.

Ela não oferece, por si só:

- uma implementação equivalente de perfis modulares de agentes;
- snapshots administráveis de coleções de conhecimento;
- templates modulares equivalentes aos candidatos do ARA;
- suítes de avaliação próprias do ARA;
- diffs de configuração efetiva;
- a escala futura de versões, analytics ou pesquisa;
- uma especificação física obrigatória.

Por isso, avaliações futuras devem partir principalmente de:

1. tarefas-alvo do ARA;
2. invariantes estruturais e de autorização;
3. casos controlados e sintéticos;
4. rubricas pedagógicas e técnicas;
5. casos negativos e limítrofes;
6. repetições para estimar estabilidade;
7. operações reais do ARA quando elas existirem.

Jornadas e falhas da referência funcional podem ser usadas como casos de contraste. Não constituem requisito de equivalência interna nem autorização para copiar schemas, ferramentas, armazenamento, sincronização ou organização física.

## 3. Camadas que não devem ser confundidas

A investigação resultou em uma separação útil para analytics de autoria, qualidade de agentes e pesquisa educacional:

```text
fato operacional observável
→ evidência preservada
→ codificação analítica versionada
→ medida
→ construto
→ interpretação
→ conclusão ou decisão científica
```

Nenhuma passagem é automática.

Exemplos:

- um reparo aceito é um fato observável, não prova de melhoria educacional;
- uma concentração de findings em um recurso não demonstra inferioridade pedagógica do recurso;
- uma mudança de perfil associada a menos erros não demonstra causalidade sem desenho apropriado;
- uma classificação de contribuição produzida por um modelo não determina autoria jurídica, criticidade, passividade ou dependência;
- um resultado de análise produzido por IA não constitui autoridade científica.

A interpretação assistida deve permanecer separada da evidência primária e da decisão humana responsável.

## 4. Corpus bibliográfico preservado

O levantamento reuniu 34 registros em sete frentes. Trata-se de uma revisão de escopo inicial, não de revisão sistemática concluída. Algumas fontes eram preprints no recorte e permanecem classificadas como tal.

A presença de uma fonte no corpus não significa adoção de sua tecnologia, terminologia, método ou recomendação.

| ID | Frente | Fonte e ano | Tipo no levantamento | Contribuição utilizada | Limitação principal |
|---|---|---|---|---|---|
| AP001 | arquitetura de agentes | Model Context Protocol, *Understanding MCP servers*, 2026 | especificação oficial | diferencia prompts, resources e tools por semântica e controle | não define o modelo de produto do ARA nem valor educacional |
| AP002 | arquitetura de agentes | Model Context Protocol, visão geral do servidor, 2025 | especificação oficial | trata prompts, resources e tools como primitivas distintas | evidência apenas de especificação técnica |
| AP003 | arquitetura de agentes | Model Context Protocol, *Resources*, 2025 | especificação oficial | documenta formas de seleção e inclusão de contexto | não resolve qualidade de retrieval, privacidade ou seleção pedagógica |
| AP004 | arquitetura de agentes | Model Context Protocol, *Prompts*, 2025 | especificação oficial | prompts parametrizados, descobríveis e controláveis | o modelo de controle pode exigir adaptação ao ARA |
| AP005 | prompting | Sahoo et al., levantamento de prompt engineering, 2024 | survey em preprint | mostra espaço amplo e dependente de tarefa | campo de rápida evolução e anterior a fluxos de agentes mais recentes |
| AP006 | prompting e reprodutibilidade | Korn et al., relato de prompting em engenharia de software, 2026 | diretriz empírica em preprint | aponta falhas de documentação de prompts, versões e justificativas | contexto de engenharia de software e preprint |
| AP007 | reprodutibilidade | Siddiq et al., reprodutibilidade de LLMs em engenharia de software, 2025 | estudo sistemático-empírico em preprint | aponta lacunas de dados, ambiente, modelo e versionamento | domínio de engenharia de software e preprint |
| AP008 | avaliação | OpenAI, orientação sobre evals, 2025 | orientação oficial de fornecedor | trata avaliação como especificar, medir e melhorar com casos reais | não é evidência educacional revisada por pares |
| AP009 | avaliação | OpenAI, avaliação de terceiros, 2026 | orientação oficial de fornecedor | desempenho depende de modelo, ferramentas, workflow e ambiente | foco em avaliação de modelos de fronteira |
| AP010 | RAG educacional | Li et al., revisão sistemática de RAG em educação, 2025 | revisão sistemática | identifica desafios de alucinação, cobertura, atualização, custo e multimodalidade | aplicações heterogêneas não permitem inferir efetividade da arquitetura |
| AP011 | RAG de domínio | Sharma et al., RAG para perguntas de domínio, 2024 | estudo em preprint | adaptação de retrieval pode melhorar geração em domínio específico | domínio não educacional e sistema interno |
| AP012 | RAG de domínio | Siriwardhana et al., adaptação de RAG, 2022 | estudo em preprint | adaptação conjunta de retriever e gerador melhora QA em alguns domínios | pode não transferir para agentes baseados em APIs |
| AP013 | RAG educacional | Nguyen et al., RAG sensível ao contexto e nível escolar, 2026 | estudo revisado por pares | explora retrieval e adaptação a heterogeneidade de aprendizes | aplicação única e transferência limitada |
| AP014 | avaliação de RAG | Hua et al., avaliação de assistentes RAG em engenharia, 2025 | framework revisado por pares | separa avaliação de retrieval de qualidade da resposta | caso de engenharia e métricas específicas do framework |
| AP015 | LLM em educação | Shi et al., revisão sistemática, 2026 | revisão sistemática | registra benefícios relatados e riscos de dependência, equidade, privacidade e confiabilidade | evidência heterogênea e em rápida mudança |
| AP016 | GenAI e learning analytics | Misiejuk et al., 2025 | revisão sistemática | mapeia codificação, scoring e classificação assistidos por GenAI | base ainda jovem e poucas implantações maduras |
| AP017 | analytics centrados em humanos | Alfredo et al., 2024 | revisão sistemática | aponta participação limitada de usuários e necessidade de controle humano e confiança | operacionalização de human-centred é inconsistente |
| AP018 | design participativo | Tuhkala, 2021 | revisão sistemática | demonstra variedade de participação docente em tecnologia educacional | anterior à atual geração de GenAI e focada em professores |
| AP019 | dashboards | Paulsen e Lindsay, 2024 | revisão sistemática | mostra maior conexão entre dashboards estudantis e desenho da aprendizagem | não valida qualquer intervenção analítica específica |
| AP020 | análise qualitativa | Goyanes, Lopezosa e Jordá, 2025 | protocolo empírico | mostra que protocolos estruturados podem tornar análise temática assistida mais transparente | um único arranjo metodológico; interpretação humana continua necessária |
| AP021 | análise qualitativa | Mehta et al., 2025 | comparação empírica | identifica utilidade e limites de LLMs diante de análise humana experiente | um dataset de saúde e uma configuração de modelo |
| AP022 | análise qualitativa | Parfenova, Denzler e Pfeffer, 2024 | proposta de pesquisa | organiza limites e lacunas de codificação temática automatizada | proposta, não validação concluída |
| AP023 | análise qualitativa | Martinez Montes et al., 2025 | estudo em preprint | aponta fragmentação, perda de interpretação latente e fronteiras incertas de temas | preprint e dataset de engenharia de software |
| AP024 | análise qualitativa | Leça et al., 2024 | mapeamento sistemático em preprint | registra ganhos de eficiência e problemas de variabilidade, nuance, privacidade e transparência | preprint e foco em engenharia de software empírica |
| AP025 | raciocínio quantitativo | Liu et al., 2024 | benchmark revisado por pares | mostra limitações em combinar dados com raciocínio estatístico e causal | benchmark não cobre workflows de pesquisa completos |
| AP026 | código estatístico | Song et al., StatLLM, 2026 | dataset revisado por pares | fornece tarefas estatísticas e código verificado para avaliação | foco em SAS e conjunto de modelos temporalmente limitado |
| AP027 | confiabilidade | Shyr et al., 2025 | framework metodológico em preprint | trata repetibilidade e reprodutibilidade de saídas de LLM como propriedades mensuráveis | domínio médico e preprint |
| AP028 | métodos mistos | Gonzalez et al., 2026 | estudo educacional em preprint | integra comparação estatística e análise qualitativa de reflexões | um estudo e workflow específico de sentimento |
| AP029 | raciocínio científico | Wang et al., SciBench, 2024 | benchmark revisado por pares | mostra limitações em problemas científicos universitários complexos | mede resolução de problemas, não análise completa de pesquisa |
| AP030 | governança | NIST AI 600-1, 2024 | orientação institucional | oferece ações de gestão de riscos para GenAI | exige contextualização educacional e jurisdicional |
| AP031 | governança | UNESCO, orientação sobre GenAI em educação e pesquisa, 2023 | orientação institucional | enfatiza agência humana, privacidade e validação pedagógica | orientação de alto nível, não especificação de implementação |
| AP032 | privacidade | Amo-Filva et al., 2024 | revisão sistemática | discute edge/fog como alternativas para reduzir centralização | foco arquitetural e não específico de agentes LLM |
| AP033 | ética | An et al., 2024 | revisão sistemática | identifica diferenças entre frameworks formais e preocupações vividas por usuários | base empírica pequena e encerrada em 2023 |
| AP034 | interoperabilidade | 1EdTech Caliper Analytics, 2026 | especificação oficial | oferece vocabulários de eventos educacionais | não define medidas, construtos ou consentimento do ARA |

### Endereços registrados no levantamento

- `https://modelcontextprotocol.io/docs/learn/server-concepts`
- `https://modelcontextprotocol.io/specification/2025-06-18/server/index`
- `https://modelcontextprotocol.io/specification/2025-11-25/server/resources`
- `https://modelcontextprotocol.io/specification/2025-06-18/server/prompts`
- `https://arxiv.org/abs/2402.07927`
- `https://arxiv.org/abs/2601.01954`
- `https://arxiv.org/abs/2512.00651`
- `https://openai.com/pt-BR/index/evals-drive-next-chapter-of-ai/`
- `https://openai.com/index/trustworthy-third-party-evaluations-foundations/`
- `https://doi.org/10.1016/j.caeai.2025.100417`
- `https://arxiv.org/abs/2404.14760`
- `https://arxiv.org/abs/2210.02627`
- `https://doi.org/10.1002/cae.70153`
- `https://doi.org/10.1111/mice.70063`
- `https://doi.org/10.1016/j.caeai.2025.100529`
- `https://doi.org/10.18608/jla.2025.8591`
- `https://doi.org/10.1016/j.caeai.2024.100215`
- `https://doi.org/10.1111/ejed.12471`
- `https://doi.org/10.1007/s10639-023-12401-4`
- `https://doi.org/10.1007/s11135-025-02199-3`
- `https://doi.org/10.1038/s41598-025-18969-w`
- `https://doi.org/10.18653/v1/2024.acl-srw.17`
- `https://arxiv.org/abs/2510.18456`
- `https://arxiv.org/abs/2412.06564`
- `https://doi.org/10.18653/v1/2024.findings-acl.548`
- `https://doi.org/10.1038/s41597-026-06731-4`
- `https://doi.org/10.1101/2025.08.06.25333170`
- `https://arxiv.org/abs/2605.27403`
- `https://proceedings.mlr.press/v235/wang24z.html`
- `https://doi.org/10.6028/NIST.AI.600-1`
- `https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research`
- `https://doi.org/10.1016/j.chb.2024.108303`
- `https://doi.org/10.1016/j.heliyon.2024.e39357`
- `https://www.1edtech.org/standards/caliper`

Esses endereços registram o corpus histórico. Versões, vigência, conteúdo e aplicabilidade precisam ser revalidados antes de uso decisório futuro, conforme `RES-002`.

## 5. Mapa histórico de perguntas de analytics

Foram registradas 14 perguntas candidatas. Elas definem questões investigáveis e limites de inferência, não métricas aprovadas.

| ID | Família | Pergunta | Saída admissível no recorte | Inferência proibida |
|---|---|---|---|---|
| AQ01 | qualidade do agente | quais perfis produzem falhas estruturais recorrentes? | taxas de falha e recomendações delimitadas | concluir dano educacional causado pelo perfil sem desenho de estudo |
| AQ02 | qualidade do agente | perfis de domínio melhoram tarefas específicas em relação ao perfil geral? | comparação com incerteza | superioridade universal entre domínios |
| AQ03 | retrieval | quais consultas falham em recuperar evidência necessária? | cobertura, relevância e taxonomia de falhas | afirmar efetividade pedagógica da fonte recuperada |
| AQ04 | contratos conectados | saídas inválidas decorrem de instruções, ferramentas ou contratos? | hipóteses de causa e casos reproduzíveis | atribuir causalidade exclusiva por correlação |
| AQ05 | qualidade de recursos | quais recursos concentram observações e reparos? | contagens, distribuições e padrões qualitativos | inferioridade pedagógica sem evidência controlada |
| AQ06 | curadoria participativa | quais observações são apoiadas, contraditas, duplicadas ou não resolvidas? | síntese argumentativa com discordâncias preservadas | equiparar maioria à verdade |
| AQ07 | efetividade de reparo | reparos aceitos evitam recorrência do problema? | regressão e recorrência | afirmar melhoria da aprendizagem sem outcomes pertinentes |
| AQ08 | avaliação de perfis | qual revisão melhora evals específicos da tarefa? | recomendação delimitada e evidência para rollback | presumir estabilidade em futuras versões de modelo |
| AQ09 | experimento | condições diferem no outcome primário pré-especificado? | estimativa, incerteza, pressupostos e sensibilidade | causalidade além do desenho |
| AQ10 | experimento | diferenças observadas podem estar associadas a imbalance, attrition ou exposição? | diagnósticos, estimativas ajustadas e limitações | afirmar que ajuste pós-hoc remove viés |
| AQ11 | qualitativa | como participantes descrevem dificuldades e benefícios? | temas, casos, contradições e trilha de evidências | tratar prevalência de temas como frequência populacional |
| AQ12 | métodos mistos | que evidência qualitativa explica ou contesta padrões quantitativos? | convergências, divergências e explicações | assumir que uma vertente valida automaticamente a outra |
| AQ13 | assistência à pesquisa | que análises e conclusões são admissíveis sob o protocolo? | explicação metodológica, alternativas e conclusão delimitada | tratar saída do modelo como autoridade científica |
| AQ14 | governança | quem pode acessar dados brutos, análises e recomendações? | decisão de acesso e trilha de auditoria | derivar autoridade da capacidade técnica do provedor |

## 6. Fixtures candidatos de avaliação

Foram registrados 16 cenários para avaliação de configurações e análises. Eles não são critérios de aceite do produto nem resultados validados.

| ID | Família | Cenário histórico | Propriedade investigada | Limite atual |
|---|---|---|---|---|
| EV01 | continuidade funcional | planejar curso completo a partir de syllabus delimitado | cobertura e estrutura | a comparação histórica com configuração monolítica deve ser tratada apenas como contraste funcional |
| EV02 | continuidade funcional | construir uma microssequência em lotes persistidos | JSON válido e progresso parcial visível | referência anterior é caso de contraste, não arquitetura equivalente |
| EV03 | separação de papéis | auditar revisão congelada sem mutação | apenas findings, sem alteração | permissões e autoridade continuam não aprovadas |
| EV04 | escopo de reparo | reparar somente findings selecionados | ausência de mutação fora do escopo | exige diff semântico, ainda candidato |
| EV05 | domínio, programação | criar prática autêntica de debugging e tracing | adequação de tarefa e feedback | validação protegida permanece responsabilidade separada |
| EV06 | domínio, matemática | criar entrada matemática semântica e feedback | separar validade de correção | controle de entrada não é autoridade de prova |
| EV07 | domínio, língua | criar exemplos e prática linguística | estrutura correta e alternativas acessíveis | revisão humana especializada pode ser necessária |
| EV08 | domínio, exame | criar distratores funcionais a partir de padrões | adequação sem copiar questões protegidas | limites de fonte e direitos precisam ser explícitos |
| EV09 | retrieval | responder tarefa que exige fonte aprovada | recuperar e citar fonte pertinente | retrieval deve ser avaliado antes da geração |
| EV10 | política de contexto | editar card com microssequência integral e vizinhos resumidos | coerência local sem mutação de vizinhos | orçamento de contexto, tokens e latência permanece aberto |
| EV11 | seleção de recurso | escolher recurso para tarefa de domínio | preservar estrutura epistêmica necessária | variedade por si só não é objetivo |
| EV12 | síntese participativa | consolidar observações conflitantes | deduplicar sem apagar divergências | popularidade não decide verdade |
| EV13 | análise qualitativa | codificar conjunto congelado de comentários | códigos rastreáveis e incerteza | interpretação latente requer revisão humana |
| EV14 | análise quantitativa | comparar condições em dataset sintético verificado | código correto, incerteza e pressupostos | não representa estudo com participantes reais |
| EV15 | reprodutibilidade | repetir análise com configurações iguais e diferentes | medir variação e preservar snapshots | repetibilidade semântica precisa ser explicitamente avaliada |
| EV16 | recuperação de falha | lidar com timeout, JSON inválido e revisão desatualizada | recuperação estruturada sem perda de trabalho | comportamento alternativo não pode ser silencioso |

A correção posterior do levantamento estabelece que o conjunto deve evoluir a partir de tarefas-alvo do ARA e casos controlados. Nenhum fixture aprova perfil, modelo, provedor, política de contexto ou mecanismo de execução.

## 7. Questões abertas registradas

Dezessete questões permaneceram explicitamente abertas:

1. terminologia pública para perfil, instrução, conhecimento e papel;
2. composição por herança ou cópia em snapshots de configuração;
3. critério para justificar perfil de domínio em vez de orientação específica de curso;
4. identidade de versão de coleções de conhecimento quando fontes ou índices derivados mudam;
5. seleção e orçamento de contexto integral, indexado e resumido;
6. fronteira entre prompts, resources, tools e objetos do domínio da aplicação;
7. conjunto de evals e avaliadores suficiente para ativar uma revisão de perfil;
8. representação de qualidade argumentativa sem prejudicar contribuintes menos eloquentes;
9. preservação e apresentação de observações contraditórias;
10. fronteira entre dados operacionais reutilizáveis para melhoria de produto e dados de pesquisa;
11. métodos estatísticos que poderiam compor uma futura bancada de pesquisa;
12. métodos qualitativos que podem ser assistidos responsavelmente por LLMs;
13. representação da integração entre vertentes quantitativas e qualitativas;
14. situações em que análises por LLM exigem repetição, modelos alternativos ou codificação humana independente;
15. critério para recomendar novo recurso em vez de alteração de perfil, instrução ou contrato;
16. subpapéis que precisam ser visíveis no produto e aqueles que são apenas metadados de contribuição;
17. capacidade futura de preservar continuidade funcional com perfis compostos sem perda de qualidade.

A última questão precisa ser lida à luz da correção v2: continuidade funcional não significa equivalência arquitetural com o sistema anterior.

## 8. Campos candidatos para execução reprodutível de análise

O levantamento registrou 32 campos candidatos agrupados por finalidade. Eles não constituem schema vigente.

### Identidade da análise

- `analysis_run_id`;
- `protocol_version_id`;
- `dataset_snapshot_id`;
- `analysis_plan_version_id`.

### Configuração do agente

- `agent_configuration_snapshot_id`;
- `model_provider_version`;
- `prompt_template_versions`;
- `knowledge_collection_snapshots`, quando pertinente;
- `tools_and_contract_versions`;
- `context_policy_version`.

### Execução

- `code_artifact`, quando pertinente;
- `environment_and_dependencies`, quando pertinente;
- `random_seed_and_sampling_parameters`, quando pertinente;
- `start_end_time`;
- `actor_and_role`.

### Análise quantitativa

- `variables_and_units`;
- `missingness_handling`;
- `assumption_checks`;
- `effect_estimates_and_uncertainty`;
- `sensitivity_analyses`.

### Análise qualitativa

- `method_and_codebook_version`;
- `codes_themes_and_evidence_links`;
- `analyst_memos_and_reflexivity`;
- `agreement_or_comparison_method`.

### Métodos mistos

- `explicit_integration_method`;
- `joint_display_or_linkage`.

### Saídas e autoridade

- `raw_outputs`;
- `validated_results`;
- `interpretations_and_alternatives`;
- `admissible_and_prohibited_conclusions`;
- `human_review_decision`;
- `limitations_and_deviations`.

O valor intelectual desse registro é a necessidade de relacionar análise, protocolo, dataset congelado, configuração efetiva, código ou procedimento, saídas brutas, resultados verificados, interpretações concorrentes, decisão humana e limitações. Os nomes de campos e sua obrigatoriedade permanecem candidatos.

## 9. Curadoria participativa e contribuição observável

A investigação propôs tratar observações de usuários como evidência situada, não como votação.

Uma observação candidata relaciona:

- alvo e versão;
- autor, papel ou pseudônimo autorizado;
- tipo e finalidade;
- texto, exemplo, fonte ou evidência;
- visibilidade e uso permitido;
- relações com outras observações;
- estado e decisão posterior.

Síntese assistida pode agrupar duplicações, contradições e convergências, mas deve preservar divergências e contraexemplos. Eloquência, extensão textual ou quantidade de votos não conferem autoridade automática.

Contribuição observável também não deve ser convertida automaticamente em percentuais de autoria, qualidade, criticidade, dependência ou passividade. Essas categorias, quando investigadas, exigem esquemas de codificação explícitos, evidência, versão, método e revisão humana apropriada.

## 10. Papel candidato da inteligência artificial em pesquisa

A investigação considerou assistência para:

- formular questões e hipóteses;
- verificar coerência entre desenho, condição, instrumento e medida;
- elaborar planos de análise;
- executar código estatístico reproduzível em ambiente controlado;
- verificar pressupostos e dados ausentes;
- propor análises alternativas;
- auxiliar codificação e síntese qualitativa;
- integrar evidência quantitativa e qualitativa;
- distinguir resultado, interpretação e conclusão admissível;
- explicar métodos e limitações.

Essas possibilidades são linhas de investigação, não atribuição de autoridade científica ao agente. Análises materiais devem preservar dados e versões pertinentes, procedimento ou código, configuração, saídas, verificação, decisão humana e limitações. Resultados estocásticos relevantes podem exigir repetição ou avaliação de estabilidade.

## 11. Limites e não autorizações

O pacote explicitamente não selecionou:

- schema de produção ou layout de banco;
- modelo ou provedor;
- base vetorial;
- motor de analytics;
- algoritmo final de retrieval;
- mecanismo de otimização automática de prompts;
- política de ativação de perfis;
- taxonomia final de papéis;
- catálogo final de métricas;
- interface administrativa;
- coleta com participantes;
- implementação.

Também rejeitou como padrão:

- configuração monolítica única para todos os domínios e tarefas;
- popularidade ou eloquência como autoridade de observação;
- mutação autônoma de prompts, conhecimento, recursos ou publicação;
- autoaprovação ou autopublicação por LLM;
- conclusões estatísticas em linguagem natural sem verificação executável quando a análise exigir cálculo;
- analytics sem finalidade, autorização e política de retenção.

Essas rejeições pertencem ao pacote histórico. Quando houver orientação vigente equivalente, sua autoridade vem das decisões e itens canônicos atuais.

## 12. Destino atual

Na orientação vigente:

- `AGENT-001` mantém aberta a investigação de perfis, versões, papéis, conhecimento, contexto, avaliações, falhas e análise assistida;
- `AUTH-002` mantém separadas identidade, papel, contribuição e autoridade;
- `DATA-001` mantém protocolos, condições e atribuição reproduzíveis;
- `DATA-002` mantém governança de dados e direitos dos participantes;
- `DATA-003` mantém eventos, medidas, analytics e interoperabilidade como questões de pesquisa;
- `PED-003` limita inferências educacionais a partir de rastros e resultados;
- `PROV-004` mantém aberta a proveniência operacional mínima e sua retenção;
- `PARAM-001` e `PARAM-002` mantêm taxonomia, composição, autoridade e snapshots de configuração em investigação;
- `RES-002` exige preservar autoridade e estabilidade temporal das fontes;
- `VAL-001` e `VAL-002` mantêm abertos corpus, estados e evidências de validação;
- `DEC-006` mantém a inteligência artificial como assistente, não autoridade de aprovação ou publicação;
- `DEC-007` mantém o projeto em pré-desenvolvimento.

Nenhuma dessas pendências autoriza implementação ou transforma o pacote histórico em especificação atual.