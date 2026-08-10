# Evidências sobre configuração de referência, autonomia, adaptação, acessibilidade e IA

**Categoria:** evidência de experiência de desenvolvimento e levantamento bibliográfico  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva evidências usadas para investigar parametrização no ARA. Ele combina uma leitura contrastiva da configuração funcional anterior com um levantamento focado sobre autonomia, autorregulação, adaptação, acessibilidade e assistência por inteligência artificial.

O material não aprova perfis, parâmetros, valores, defaults, precedência, modelos adaptativos, provedores, MCP, analytics, schema, interface, arquitetura, stack ou implementação. As pendências vigentes permanecem em `PARAM-001`, `PARAM-002`, `PED-004`, `PED-010` e `AGENT-001` no [`BACKLOG.yaml`](../../BACKLOG.yaml).

## 1. Correção de interpretação da referência funcional

A investigação de configurações modulares de agentes foi corrigida para evitar uma equivalência inexistente entre a experiência anterior e a arquitetura futura do ARA.

A referência funcional deve ser usada para:

- identificar jornadas que funcionam e não devem regredir silenciosamente;
- registrar limitações e acoplamentos que motivam o ARA;
- fornecer exemplos reais de operações e falhas;
- fornecer amostras de payload e workload para estudos posteriores;
- formular tarefas e cenários representativos do ARA.

Ela não demonstra que já existam equivalentes internos de perfil de agente, template de prompt, coleção de conhecimento, suíte de avaliação ou snapshot de configuração modular.

Pela mesma razão, avaliações futuras de configurações de agentes devem partir das tarefas-alvo do ARA. Jornadas e falhas anteriores podem integrar o corpus de contraste, mas não devem ser tratadas como fixtures de uma arquitetura modular equivalente.

A linha de investigação de agentes continua incluindo, como candidatos não aprovados: perfis versionados, papéis, perfis de domínio, coleções de conhecimento, templates de tarefa, fronteiras entre instruções, recursos e ferramentas, políticas de contexto e escrita, snapshots efetivos, avaliações de regressão, administração em linguagem simples, ciclo de vida de configurações, proveniência de operações, observações, reparo, taxonomia de falhas e análise assistida. Esses tópicos permanecem sob `AGENT-001` e os domínios específicos de autoria, dados e pesquisa.

## 2. Mapa da configuração funcional de referência

Foram registradas 28 características para distinguir comportamento demonstrado, limitações e possibilidades ainda não presentes. A tabela abaixo preserva o conteúdo analítico sem transformar a referência em default universal.

| Área | Comportamento ou evidência de referência | Interpretação e limite |
|---|---|---|
| Estrutura educacional | projeto, curso, módulo, lição, microssequência e card | estrutura empiricamente usada, não prova de superioridade nem hierarquia universal |
| Função do card | unidade ordenada básica de estudo e interação | não deve ser reduzido conceitualmente a flashcard |
| Microssequência | objetivo local e unidade ordenada de progressão | termo, tamanho e eficácia permanecem investigáveis |
| Teoria e prática | cards de teoria e prática estruturalmente distintos | ponto de partida empírico, não separação universal obrigatória |
| Estudo móvel | prioridade a smartphone, uso com uma mão, rolagem e retomada após interrupção | contexto móvel envolve fragmentação, conectividade e recuperação, não apenas viewport |
| Estudo offline | curso publicado e estado funcional disponíveis sem conexão | extensões conectadas exigem semântica explícita de indisponibilidade |
| Consequência da prática | tentar novamente, limpar, revelar e avançar sem punição acumulada | perfil de baixa consequência, não regra universal |
| Formas de prática | ausência de prática, lacuna, escolha simples ou múltipla e prática estreita de fluxo | diversidade de resposta menor que diversidade representacional |
| Validação de lacuna | correspondência literal ou variantes enumeradas | não demonstra equivalência semântica |
| Validação de escolha | conjunto selecionado exato | crédito parcial e retorno por distrator permanecem questões separadas |
| Retorno pedagógico | explicação posterior, retorno local opcional e resultado após confirmação | conteúdo, momento, persistência e relação com nova tentativa precisam ser separados |
| Telemetria | cursor, conclusão estrutural, marcação para revisão e observação situada | não inferir atenção, esforço ou domínio a partir desse estado funcional |
| Observações | observação situada por pessoa e card, com estados de tratamento | escopo, visibilidade e ciclo de vida podem ser ampliados, mas não são voto nem nota |
| Recursos estruturados | conjunto implementado de recursos declarativos com contratos fechados | baseline verificável, não ontologia universal do ARA |
| Semântica e geometria | dados semânticos persistidos e geometria ou estilo derivados pelo renderizador | gramáticas especializadas podem exigir outras fronteiras sem tornar geometria livre o conteúdo canônico |
| Composição | blocos compostos com limites conservadores | limites observados são evidência situada, não política futura aprovada |
| Autoria assistida | planejamento, leitura, recombinação, mutação e publicação por operações delimitadas | autoria por assistência é critério funcional, não escolha de protocolo ou arquitetura |
| Reparo contextual | alvo reduzido, contexto de leitura, prévia, confirmação e verificação de versão | favorece reparo localizado em vez de regeneração ampla, sem aprovar contrato técnico |
| Ciclo de qualidade | planejamento, construção, auditoria, reparo e reauditoria | separação das funções é evidência útil; terminologia e variantes de processo permanecem abertas |
| Autoridade humana | aplicação e publicação confirmadas por pessoa autorizada | níveis de automação podem variar, mas a autoridade não decorre do modelo por padrão |
| Publicação | autoria privada separada de publicação explícita | publicação não equivale a validação acadêmica nem necessariamente a acesso público |
| Proveniência de fontes | suporte anterior limitado e necessidade futura de ancoragem e contradição | não usar porcentagem genérica de precisão sem métrica definida |
| Localização | distinção entre idioma de interface, curso e agente | localização futura não altera o português do Brasil como idioma documental canônico |
| Papéis e capacidades | a mesma pessoa pode acumular capacidades de estudo, autoria, revisão e administração | evitar converter capacidades contextuais em identidades rígidas do domínio |
| Limites dos recursos | limites semânticos e de tamanho orientados a dispositivos móveis | limites futuros dependem de evidência de desempenho e acessibilidade |
| Respostas estruturadas ausentes | construção, ordenação, plotagem, execução e argumento aberto aparecem pouco ou não aparecem | ausência revela lacunas, mas não cria requisito automático de implementação |
| Analytics e pesquisa | telemetria mínima e ausência de objetos de protocolo na referência | eventos, medidas, construtos e interpretações precisam permanecer separados |
| Perfis de implantação | referência pessoal, com cenários gerenciados e autogerenciados ainda futuros | implantações podem variar em serviços sem romper a semântica do produto |

O mapa é coerente com `DEC-006`: a continuidade funcional deve ser preservada ou reformulada explicitamente, sem herdar automaticamente arquitetura, configuração ou escolha técnica.

## 3. Horizonte externo e metamodelagem da configuração

A síntese comparativa rejeitou dois extremos como orientação de pesquisa:

1. limitar a parametrização à decomposição das escolhas já existentes na referência funcional;
2. construir antecipadamente uma plataforma universal de componentes, runtimes e gramáticas.

A recomendação histórica foi investigar um núcleo educacional reconhecível com parametrização explícita e extensibilidade governada por camadas. Na orientação vigente, isso permanece recomendação e questão de pesquisa, não decisão de arquitetura.

A descoberta de parâmetros foi organizada em quatro conjuntos:

- configuração funcional de referência;
- dimensões externas recorrentes suficientemente definidas para modelagem;
- candidatos imaturos que ainda exigem evidência ou definição;
- dimensões dependentes de capacidades instaladas ou autorizadas.

Essa organização reforça `PARAM-001`: descoberta, definição, evidência, recomendação e decisão não são estados equivalentes.

## 4. Famílias de dimensões investigadas em autonomia, adaptação, acessibilidade e IA

O levantamento estruturou 50 dimensões candidatas em cinco famílias. Os nomes abaixo descrevem o espaço investigado e não constituem identificadores públicos aprovados.

### Autonomia

- escopo do controle;
- modo de escolha;
- política de recomendação;
- política de bloqueio, exceção e reversão.

### Autorregulação

- apoio a objetivos;
- planejamento;
- monitoramento;
- reflexão;
- estratégias;
- busca de ajuda;
- autoavaliação.

### Adaptação

- modo de adaptação;
- alvo;
- gatilho;
- base de evidência;
- autoridade;
- modo de aplicação;
- transparência;
- exceção e contestação;
- rollback;
- snapshot de estado efetivo;
- fallback.

### Acessibilidade

- modo de desenho inclusivo;
- escopo da acomodação;
- política de declaração;
- controle de preferências;
- modalidade;
- equivalência da acomodação;
- preservação do construto;
- compatibilidade com tecnologia assistiva;
- persistência de preferências e acomodações;
- privacidade de dados de acessibilidade.

### Assistência por inteligência artificial

- função;
- iniciação;
- escopo de contexto;
- ancoragem e fontes;
- estado da saída;
- autoridade;
- requisito de revisão;
- política de validação;
- comunicação de incerteza;
- proveniência;
- editabilidade;
- contestação;
- fronteira de dados;
- retenção;
- política de modelo e provedor;
- comportamento offline;
- falha e recuperação;
- reprodutibilidade.

A decomposição sustenta a investigação de configurações combináveis, mas não aprova os valores históricos associados a essas dimensões.

## 5. Restrições analíticas recorrentes

O material convergiu em restrições úteis para investigação futura:

- autonomia não equivale a escolha ilimitada;
- autorregulação deve ser apoiada por funções explícitas, não inferida como traço do estudante a partir de rastros;
- adaptação e acomodação são responsabilidades diferentes;
- qualquer adaptação relevante precisa tornar explícitos alvo, evidência, autoridade, estado efetivo, possibilidade de contestação e comportamento alternativo;
- acessibilidade é responsabilidade transversal e não deve depender de exposição desnecessária de diagnóstico;
- modalidades alternativas não devem ser presumidas equivalentes sem revisão do construto;
- assistência por IA não deve adquirir autoridade final por fluência, citação, confiança declarada ou revisão por outra IA;
- contexto, dados, fontes e retenção devem ser delimitados proporcionalmente à tarefa;
- indisponibilidade de IA conectada não deve impedir o caminho básico de estudo quando a capacidade não for essencial à condição declarada;
- falhas operacionais e uso de ajuda não são evidência automática de dificuldade, esforço ou domínio;
- condições de pesquisa que dependem de configuração, modelo, contexto ou saída precisam de snapshots suficientes para interpretação e reprodução apropriada.

Essas restrições devem ser confrontadas com os itens canônicos dos domínios correspondentes antes de qualquer promoção a requisito.

## 6. Perfis históricos usados para contraste

Nove perfis foram usados para verificar se as dimensões conseguiam representar contextos distintos:

- referência funcional pessoal e não punitiva;
- estudo autodirigido reflexivo;
- curso ou tutoria com controle compartilhado;
- condição de pesquisa bloqueada;
- sobreposição centrada em acessibilidade;
- autoria assistida por IA;
- estudo assistido por IA;
- uso determinístico offline;
- uso institucional governado de IA.

Esses perfis eram casos de contraste. Nenhum está aprovado como configuração padrão, catálogo obrigatório ou contrato do produto.

## 7. Levantamento bibliográfico focado

O corpus estruturado reuniu 34 registros. A tabela preserva a contribuição analítica e a limitação registrada em cada fonte.

| Ano | Fonte | Frente | Contribuição para a investigação | Limitação registrada |
|---:|---|---|---|---|
| 2002 | Zimmerman, *Becoming a self-regulated learner: An overview*, DOI `10.1207/S15430421TIP4102_2` | autorregulação | separa antecipação, desempenho e autorreflexão; sustenta metas, planejamento, monitoramento e reflexão como dimensões distintas | revisão conceitual, não avaliação de produto nem prescrição de defaults digitais |
| 2017 | Panadero, *A Review of Self-regulated Learning: Six Models and Four Directions for Research*, DOI `10.3389/fpsyg.2017.00422` | autorregulação | impede reduzir autorregulação a um único parâmetro ao reunir processos cognitivos, metacognitivos, motivacionais, comportamentais e afetivos | comparação de modelos, não evidência para implementar todos os subprocessos |
| 2015 | Broadbent e Poon, *Self-regulated learning strategies & academic achievement in online higher education learning environments*, DOI `10.1016/j.iheduc.2015.04.007` | autorregulação | sustenta candidatos explícitos de planejamento, regulação de tempo e esforço, metacognição e pensamento crítico | predomínio de evidência correlacional e contextos de ensino superior anteriores a 2015 |
| 2008 | Dignath, Buettner e Langfeldt, *How can primary school students learn self-regulated learning strategies most effectively?*, DOI `10.1016/j.edurev.2008.02.003` | autorregulação | apoia ensino explícito de estratégias e múltiplas famílias de apoio | populações escolares e características de intervenção não mapeiam diretamente para parâmetros de software |
| 2008 | Dignath e Buettner, *Components of fostering self-regulated learning among students*, DOI `10.1007/s11409-008-9029-x` | autorregulação | sustenta decompor apoio cognitivo, metacognitivo e motivacional e preservar moderadores educacionais | intervenções antigas; prompts ou dashboards não reproduzem automaticamente as intervenções |
| 2014 | Karich, Burns e Maki, *Updated Meta-Analysis of Learner Control Within Educational Technology*, DOI `10.3102/0034654314526064` | controle do estudante | resultado acadêmico médio próximo de zero contra universalizar controle irrestrito e a favor de decompor dimensões de controle | tecnologias heterogêneas e anteriores às interfaces atuais de LLM |
| 2023 | Admiraal et al., *Effects of Students’ Autonomy Support on their Self-Regulated Learning Strategies*, DOI `10.46328/ijres.3343` | controle do estudante | trata apoio à autonomia como estrutura desenhada, não abandono, e sustenta cenários de controle compartilhado | escolas secundárias e medidas específicas da intervenção |
| 2026 | Kooi et al., *Exploring shared control in upper primary school learners working with an adaptive learning technology*, DOI `10.14786/flr.v13i3.1471` | controle compartilhado | oferece exemplo implementado em que estudantes ajustam dificuldade enquanto o sistema seleciona tarefas | população e domínio estreitos; não sustenta defaults adaptativos gerais |
| 2006 | Aleven et al., *Toward Meta-cognitive Tutoring: A Model of Help Seeking with a Cognitive Tutor*, DOI `10.3233/IRG-2006-16(2)02` | busca de ajuda | separa disponibilidade de ajuda, solicitação, uso de pistas, retorno sobre busca de ajuda e objetivos metacognitivos | tutor baseado em regras e domínio específico; não deve virar vigilância automática |
| 2011 | Roll et al., *Improving students’ help-seeking skills using metacognitive feedback in an intelligent tutoring system*, DOI `10.1016/j.learninstruc.2010.07.004` | busca de ajuda | sustenta retorno metacognitivo opcional e ensino da busca de ajuda | ITS e população específicos; automação depende de modelo comportamental validado |
| 2014 | Ma et al., *Intelligent Tutoring Systems and Learning Outcomes: A Meta-Analysis*, DOI `10.1037/a0037123` | aprendizagem adaptativa | indica que ITS podem melhorar resultados em algumas comparações, tratando adaptação como família de capacidades | evidência anterior à IA generativa, com alta heterogeneidade |
| 2026 | Wang et al., *A Meta-Analysis of Moderators of the Effects of Technology-Enhanced Adaptive Learning*, DOI `10.1002/jcal.70168` | aprendizagem adaptativa | reforça tratamento sensível a moderadores e separação de resultados cognitivos, afetivos e comportamentais | populações escolares e estudos de 2012 a 2021; não valida algoritmo do ARA |
| 2025 | Kestin et al., *AI tutoring outperforms in-class active learning*, DOI `10.1038/s41598-025-97652-6` | assistência de estudo por IA | mostra potencial de tutoria cuidadosamente desenhada e sustenta perfis de IA específicos por função | tutor customizado, conteúdo selecionado, uma instituição e intervenção breve |
| 2025 | Bastani et al., *Generative AI without guardrails can harm learning*, DOI `10.1073/pnas.2422633122` | assistência de estudo por IA | mostra que melhor desempenho durante prática pode coexistir com pior aquisição sem assistência; sustenta salvaguardas e preservação do esforço cognitivo | matemática e interfaces específicas de GPT-4; generalização limitada |
| 2024 | Bo et al., *Disclosures & Disclaimers: Investigating the Impact of Transparency Disclosures and Reliability Disclaimers on Learner-LLM Interactions*, DOI `10.1609/hcomp.v12i1.31597` | transparência de IA | disclaimers e transparência podem alterar confiança e comportamento; exposição deve ser tratada conforme finalidade | uma tarefa e um tutor; disclosures não melhoraram desempenho de forma uniforme |
| 2019 | Amershi et al., *Guidelines for Human-AI Interaction*, DOI `10.1145/3290605.3300233` | interação humano-IA | sustenta limites de capacidade, correção, explicação por escopo, feedback, controle e falha compreensível | diretrizes gerais, exigindo adaptação educacional por domínio |
| 2021 | Buçinca et al., *To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI*, DOI `10.1145/3449287` | interação humano-IA | explicações isoladas não garantem confiança adequada; revisão ativa pode reduzir dependência excessiva com custo de usabilidade | tarefas de decisão fora da educação e efeitos moderados por subgrupos |
| 2025 | de Jong et al., *Cognitive Forcing for Better Decision-Making: Reducing Overreliance on AI Systems Through Partial Explanations*, DOI `10.1145/3710946` | interação humano-IA | sustenta explicações parciais e reflexão configuráveis em vez de assumir que explicação completa é sempre mais segura | tarefas não educacionais; carga e acessibilidade podem piorar |
| 2018 | Dietvorst et al., *Overcoming Algorithm Aversion: People Will Use Imperfect Algorithms If They Can Modify Them*, DOI `10.1287/mnsc.2016.2643` | interação humano-IA | sustenta editabilidade e override delimitado como mecanismos de controle | contexto de previsão; alterações humanas podem também reduzir qualidade e exigem proveniência |
| 2024 | Kücking et al., *Automation Bias in AI-Decision Support*, DOI `10.3233/SHTI240871` | interação humano-IA | evidencia vulnerabilidade da supervisão humana a concordância incorreta e sustenta treinamento, inspeção e defaults não autoritativos | tarefa clínica, com transferência apenas inferencial para educação |
| 2024 | Gaudeul et al., *Understanding the Impact of Human Oversight on Discriminatory Outcomes in AI-Supported Decision-Making*, DOI `10.3233/FAIA240598` | interação humano-IA | humano no circuito não corrige automaticamente vieses; sustenta controles sistêmicos e orientação explícita de override | decisões de emprego e crédito, não autoria educacional |
| 2024 | CAST, *Universal Design for Learning Guidelines 3.0* | acessibilidade e UDL | sustenta múltiplos meios de engajamento, representação, ação e expressão e atenção a barreiras sistêmicas | framework, não estimativa de efeito de produto |
| 2026 | CAST, *UDL Guidelines 3.0: A Community-Driven, Research-Based Process Toward Fulfilling the Promise of Universal Design for Learning* | acessibilidade e UDL | reforça variabilidade do estudante como entrada de desenho e participação de pessoas afetadas na validação | relato de processo, não definição de parâmetros nem conformidade do ARA |
| 2023 | W3C, *Web Content Accessibility Guidelines (WCAG) 2.2* | acessibilidade | oferece baseline técnico testável para interfaces perceptíveis, operáveis, compreensíveis e robustas | não cobre toda necessidade cognitiva nem equivalência pedagógica |
| 2023 | Almeqdad et al., *The effectiveness of universal design for learning*, DOI `10.1080/2331186X.2023.2218191` | acessibilidade e UDL | sustenta UDL como família de desenho informada por evidência, sem universalizar uma implementação | intervenções heterogêneas e operacionalizações inconsistentes |
| 2025 | Devitt et al., *A Systematic Literature Review on the Effectiveness of Universal Design for Learning in Second-Level Education*, DOI `10.34874/PRSM.ijududl-vol1iss1.4913` | acessibilidade e UDL | registra sinais positivos e menor implementação de autonomia e autorregulação, reforçando sua separação explícita | base ainda jovem e heterogênea em escolas regulares |
| 2024 | Panjwani, Charania e Zhai, *AI for Students with Learning Disabilities: A Systematic Review* | acessibilidade e IA | mostra oportunidades de acessibilidade e cobertura estreita de condições, exigindo validação específica | dez de dezesseis estudos tratam dislexia; pouca evidência para outras deficiências |
| 2024 | *Impact of Artificial Intelligence and Virtual Reality on Educational Inclusion*, DOI `10.3390/educsci14111223` | acessibilidade e IA | registra possibilidades de personalização e assistência com necessidade de avaliação de inclusão, acessibilidade e implementação | combina IA e realidade virtual e reúne estudos heterogêneos |
| 2023 | UNESCO, *Guidance for generative AI in education and research* | governança de IA | sustenta uso centrado em pessoas, apropriado ao papel, protetor de privacidade, validado e acompanhado de desenvolvimento de capacidades | orientação, não prova empírica; regras jurídicas permanecem específicas por jurisdição |
| 2023 | NIST, *Artificial Intelligence Risk Management Framework 1.0*, DOI `10.6028/NIST.AI.100-1` | governança de IA | sustenta ciclo contínuo de governança, mapeamento, medição e gestão, com documentação de uso e riscos | framework transversal e não especificação de produto educacional |
| 2024 | NIST, *Generative Artificial Intelligence Profile*, DOI `10.6028/NIST.AI.600-1` | governança de IA | sustenta documentação de confabulação, privacidade, configuração humano-IA, proveniência, integridade e avaliação | não específico de educação e não determina defaults |
| 2021 | Scheiter, *The Learner Control Principle in Multimedia Learning*, DOI `10.1017/9781108894333.043` | controle do estudante | sustenta controle condicionado, aconselhamento e desenho sensível à experiência | síntese centrada em multimídia, não autoria contemporânea com IA |
| 2002 | Aleven e Koedinger, *An effective metacognitive strategy: learning by doing and explaining with a computer-based Cognitive Tutor*, DOI `10.1207/s15516709cog2602_1` | apoio metacognitivo | sustenta autoexplicação como operação opcional e ajuda a distinguir produção de resposta por IA de prompts que preservam raciocínio | geometria e tutor baseado em regras; assistência por LLM é diferente |
| 2026 | Zhao et al., *Effectiveness of a generative AI-powered digital tutor integrated with a knowledge graph in anatomy education for nursing students* | assistência de estudo por IA | oferece evidência recente de tutoria combinando IA generativa e grafo de conhecimento, reforçando domínio e contexto delimitados | uma faculdade e anatomia; intervenção combina IA, grafo e modelo instrucional |

O corpus é heterogêneo quanto a população, domínio, desenho e profundidade de acesso. Ele sustenta perguntas, decomposições e salvaguardas, não um perfil educacional ou mecanismo adaptativo universal.

## 8. Incertezas que podem alterar decisões futuras

A investigação registrou, entre outras, as seguintes incertezas:

- quais apoios de autonomia e autorregulação ajudam estudantes adultos em estudo móvel, fragmentado e offline;
- quanto controle do estudante é produtivo por domínio, experiência, consequência e estrutura do curso;
- que evidência pode acionar adaptação sem transformar operação funcional em vigilância;
- como usuários não técnicos compreendem perfis, sobreposições, estado da IA, proveniência e consequências;
- como previews, avisos e mecanismos de reflexão afetam dependência excessiva, carga e acessibilidade;
- se assistência de estudo por IA preserva desempenho sem assistência e transferência em prazo maior;
- como avaliar variantes de curso geradas ou alteradas por IA sem confundir efeitos pretendidos e acidentais;
- como representar acomodações e seus efeitos em snapshots sem expor informação sensível;
- quais funções de IA dependem de conexão e quais exigem alternativa determinística;
- como mudanças de modelo ou provedor afetam comparabilidade de pesquisa e manutenção de artefatos;
- como perfis avançados podem ser administrados sem esconder consequências nem impor vocabulário técnico.

Essas incertezas permanecem pesquisa futura. Não há resultado validado de produto neste levantamento.
