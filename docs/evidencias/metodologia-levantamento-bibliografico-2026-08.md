# Metodologia histórica do levantamento bibliográfico e de evidências

**Categoria:** levantamento bibliográfico, método de pesquisa e evidência metodológica  
**Recorte temporal:** 2 a 5 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva a estrutura metodológica construída para organizar a base bibliográfica e documental do ARA. O objetivo histórico era permitir que decisões sobre pedagogia, produto, pesquisa educacional, experiência de uso, arquitetura, governança e aspectos institucionais fossem relacionadas a evidências rastreáveis, sem converter preferências do projeto em regras gerais.

A estrutura é uma **evidência de método já desenvolvido**, não um protocolo formal vigente para uma futura publicação acadêmica. Qualquer revisão de escopo, revisão sistemática ou outro estudo destinado a publicação deverá definir sua pergunta própria, revalidar a orientação metodológica aplicável e registrar prospectivamente os critérios efetivamente usados.

## 1. Princípios metodológicos preservados

A organização histórica adotava princípios que permanecem úteis para a investigação futura:

- pesquisar literatura e outras fontes pertinentes antes de converter uma generalização em orientação de produto;
- distinguir evidência, interpretação dos autores, inferência do pesquisador, hipótese de desenho, recomendação e decisão;
- não declarar leitura integral quando somente metadados, resumo, trecho ou relato secundário estiverem disponíveis;
- preservar datas, bases, strings de busca, filtros, contagens, decisões de triagem e registros de extração;
- usar revisões e orientações institucionais para mapear um campo, recorrendo a estudos primários quando uma afirmação central exigir verificação mais direta;
- registrar evidências contraditórias, limitações e incerteza;
- não tratar uma base, sistema ou tradição de pesquisa isolada como descrição completa do espaço de possibilidades;
- preservar materiais restritos sem redistribuí-los indevidamente;
- separar achados de pesquisa de implicações para o ARA e submeter qualquer mudança normativa ao método canônico do projeto.

Esses princípios complementam `METODO_DE_TRABALHO.md`. Eles não criam uma segunda governança paralela.

## 2. Enquadramento bibliográfico histórico

A primeira formulação ampla foi concebida como uma **revisão de escopo programática**, acompanhada por mapeamento de revisões, handbooks, estudos primários centrais, bibliografias curriculares, pesquisadores e grupos, além de levantamentos normativos, jurídicos e técnicos em frentes próprias.

O enquadramento inicial partia de cards e flashcards digitais, prática de recuperação, repetição espaçada e estudo autodirigido, mas já abrangia temas mais amplos: feedback, progressão, autorregulação, acessibilidade, aprendizagem móvel e offline, avaliação, learning analytics, autoria assistida, métodos de pesquisa, infraestrutura, interoperabilidade, ética, privacidade e governança.

Esse ponto de partida histórico não define o gênero acadêmico atual do ARA nem limita o produto a flashcards. O enquadramento acadêmico permanece questão própria do backlog.

### Referências metodológicas então adotadas como orientação

O protocolo histórico registrava como referências iniciais:

- *JBI Manual for Evidence Synthesis*, edição de 2024 e atualizações online;
- capítulo sobre scoping reviews do JBI Manual;
- Tricco et al. (2018), PRISMA-ScR.

A distinção metodológica registrada era importante: PRISMA-ScR foi tratado como guia de relato, não como substituto do protocolo nem como rótulo automático para toda busca. Essas referências precisam ser revalidadas quanto à versão e à aplicabilidade antes de um estudo acadêmico futuro.

## 3. Fontes de informação planejadas

O plano histórico identificava, conforme disponibilidade e pertinência, bases como:

- Scopus;
- Web of Science;
- ERIC;
- APA PsycInfo;
- Education Source;
- ACM Digital Library;
- IEEE Xplore;
- PubMed/MEDLINE;
- SciELO;
- RCAAP;
- BDTD/IBICT;
- ProQuest Dissertations & Theses.

Também previa fontes complementares como Crossref, OpenAlex, Google Scholar para busca suplementar e encadeamento de citações, repositórios institucionais, páginas oficiais, normas, legislação, documentação técnica primária e listas de referências.

Esta lista registra **fontes previstas**, não afirma que todas foram consultadas. A execução efetiva de cada busca deve ser comprovada pelos registros correspondentes.

## 4. Registro reproduzível de busca

Uma busca documentada deveria preservar, no mínimo:

- identificador da busca;
- frente ou pergunta de pesquisa;
- base ou fonte consultada;
- data e fuso horário;
- string exata;
- campos pesquisados;
- filtros;
- quantidade recuperada;
- formato de exportação;
- referência ao arquivo de exportação, quando existente;
- responsável;
- observações e limitações.

O princípio central é que a estratégia efetivamente executada seja reconstruível. Uma string ilustrativa ou planejada não deve ser apresentada como busca realizada.

## 5. Registro de fontes e nível real de acesso

O esquema histórico de registro bibliográfico separava identificação, descoberta, acesso, triagem, classificação temática, qualidade e proveniência da síntese.

### Identificação

Entre os campos candidatos estavam:

- identificador interno estável;
- tipo de fonte;
- título original;
- autores ou organização;
- ano e veículo de publicação;
- volume, número e páginas, quando aplicáveis;
- DOI normalizado e outros identificadores persistentes;
- endereço canônico;
- idioma.

O título original deveria ser preservado sem tradução no campo bibliográfico canônico.

### Descoberta

A procedência da descoberta poderia registrar:

- base ou fonte de descoberta;
- identificador da busca;
- data;
- consulta ou caminho de descoberta;
- lote de importação.

### Estados de acesso

A estrutura histórica distinguia explicitamente:

- `full_text_verified`: texto completo examinado;
- `full_text_partial`: apenas parte relevante examinada;
- `abstract_verified`: apenas resumo examinado;
- `metadata_only`: apenas metadados;
- `secondary_report`: fonte conhecida por relato de outra fonte;
- `requested`: acesso solicitado;
- `unavailable`: não obtida após tentativa documentada;
- `superseded_or_retracted`: substituída, corrigida ou retratada.

A categoria de acesso limita a autoridade da extração. Uma síntese convincente não pode ocultar que o texto completo não foi examinado.

## 6. Deduplicação e triagem

O procedimento histórico propunha deduplicação progressiva por:

1. DOI normalizado;
2. PMID, ISBN, arXiv ID ou identificador equivalente;
3. título normalizado, ano e primeiro autor;
4. inspeção manual de casos ambíguos.

A triagem era separada em:

1. título e resumo;
2. texto completo.

Cada decisão deveria registrar estado, data, razão e nível de acesso. A estrutura reconhecia explicitamente que triagem realizada por uma pessoa não deve ser descrita como dupla triagem independente. Protocolos futuros podem exigir procedimentos adicionais conforme a pergunta, o desenho e o objetivo de publicação.

Um registro mínimo de triagem continha identificador da fonte, título, ano, DOI, tipo, decisão e razão em título/resumo, estado e decisão de texto completo, razão de exclusão, data, revisor e notas.

## 7. Extração adaptada ao tipo de estudo

O esquema de extração não tratava todos os estudos como equivalentes. Campos não aplicáveis deveriam ser marcados como tais, em vez de omitidos silenciosamente.

As principais famílias de informação eram:

### Referência e acesso

- referência completa;
- estado de acesso;
- páginas, tabelas, figuras ou suplementos usados;
- versão examinada.

### Natureza e contexto

- objetivo, pergunta ou hipótese;
- país, instituição, nível educacional e área;
- modalidade, ambiente e dispositivo;
- duração e acompanhamento.

### Participantes

- população-alvo;
- critérios de inclusão e exclusão;
- recrutamento;
- amostras inicial e final;
- distribuição entre condições;
- características relevantes, experiência prévia, perdas e adesão;
- limitações de representatividade.

### Desenho metodológico

- tipo de desenho;
- unidade de alocação e análise;
- randomização, pareamento ou controle;
- comparador;
- cegamento, quando aplicável;
- pré-registro ou protocolo;
- justificativa amostral;
- procedimentos qualitativos, mistos ou de investigação de desenvolvimento.

### Fundamento teórico e intervenção

- teorias declaradas e mecanismo proposto;
- definição de construtos;
- relação entre teoria e intervenção;
- plataforma ou material;
- forma de produção do conteúdo;
- tipo de resposta;
- multimodalidade;
- feedback, pistas, tentativas e revelação;
- notas, pontuação ou gamificação;
- tempo;
- agendamento, repetição, espaçamento e intercalação;
- progressão, adaptação e controle do participante;
- mediação, acessibilidade e fidelidade de implementação.

### Instrumentos, dados e análise

- resultados primários e secundários;
- instrumentos, escalas, origem, validação e licença;
- testes de conhecimento, retenção e transferência;
- eventos, medidas derivadas e fórmulas;
- questionários, entrevistas, observações e diários;
- momentos de coleta e dados faltantes;
- técnicas estatísticas, modelos, covariáveis, efeitos e incerteza;
- análise qualitativa e integração de métodos mistos;
- análises de sensibilidade, moderadores e subgrupos.

### Resultados, qualidade e limitações

- resultados principais, nulos ou adversos;
- magnitude e incerteza;
- exposição real e adesão;
- distinção entre resultado imediato, retenção e transferência;
- discrepâncias entre texto, tabelas e conclusão;
- risco de viés e instrumento de avaliação usado;
- limitações declaradas e adicionais;
- conflitos de interesse e financiamento;
- generalizações sustentáveis e generalizações proibidas.

## 8. Implicações para o ARA sem conversão automática

A extração histórica previa registrar implicações para parâmetros, experiência de uso, acessibilidade, arquitetura, armazenamento, pesquisa, ética, privacidade e experimentos.

Essa passagem precisa manter categorias separadas. Um estudo pode sustentar um **achado** sem determinar uma **decisão**. Uma consequência possível para o ARA pode ser hipótese, alternativa, recomendação ou pendência.

O esquema histórico classificava conclusões extraídas como:

- `direct_evidence`: sustentada diretamente pelos dados da fonte;
- `author_interpretation`: interpretação dos autores;
- `reviewer_inference`: inferência produzida durante a análise;
- `design_hypothesis`: hipótese de desenho a avaliar;
- `operational_requirement`: necessidade operacional proposta, distinta de alegação pedagógica.

Na orientação vigente, o último rótulo deve ser lido como **candidato a requisito operacional**, não como requisito aprovado. Uma necessidade só se torna requisito do projeto quando receber a autoridade prevista em `METODO_DE_TRABALHO.md` e `DECISOES.md`.

## 9. Qualidade, confiança e heterogeneidade

O método histórico reconhecia que uma revisão de escopo pode mapear fontes heterogêneas sem excluir automaticamente todas as fontes de menor qualidade, mas isso não torna as evidências equivalentes.

Conforme o desenho e a finalidade, deveriam ser registrados:

- transparência metodológica;
- adequação da amostra e da comparação;
- validade dos instrumentos;
- risco de viés;
- precisão e incerteza;
- aplicabilidade ao contexto investigado;
- consistência ou conflito com outras fontes;
- revisão por pares;
- limitações;
- conflitos de interesse.

A ferramenta de avaliação de qualidade deveria ser escolhida conforme o tipo de fonte e a pergunta, e não adotada universalmente sem justificativa.

## 10. Ética, direitos autorais e materiais restritos

A estrutura preservava os seguintes limites:

- textos integrais restritos não devem ser redistribuídos apenas por terem sido usados na pesquisa;
- instrumentos protegidos não devem ser reproduzidos integralmente sem autorização;
- metadados, referências, extrações e análises podem ser preservados dentro dos limites aplicáveis;
- dados de participantes exigem governança própria e não pertencem automaticamente a uma etapa bibliográfica;
- uma proposta de pesquisa deve explicitar consentimento, privacidade, acesso restrito, direitos autorais, aprovação institucional e retenção quando esses temas forem aplicáveis.

Solicitações de textos inacessíveis deveriam indicar a referência, o identificador persistente, a parte necessária, a razão da relevância, substitutos aceitáveis e a limitação produzida pela ausência do texto.

## 11. Alterações de protocolo

Uma mudança metodológica relevante deveria registrar:

- data;
- motivo;
- impacto;
- seção afetada;
- relação com a pergunta ou decisão que motivou a alteração.

O princípio preservado é não reescrever retrospectivamente o método como se uma decisão posterior estivesse prevista desde o início.

## 12. Relação com o backlog vigente

A estrutura histórica fornece evidência para três itens atuais:

- `RES-001`: já existe uma base metodológica para registrar perguntas, estratégias, bases, corpus, triagem, extração, síntese e limitações; ainda é necessário auditar o corpus existente e definir protocolos futuros adequados às perguntas concretas;
- `RES-002`: já existem campos candidatos para procedência, nível de acesso, autoridade, qualidade, localizações usadas e data; ainda é necessário definir o conjunto mínimo vigente e regras de revalidação de informações temporais;
- `RES-003`: incertezas capazes de alterar decisões devem ser convertidas em perguntas verificáveis, métodos e critérios explícitos de mudança de decisão.

A existência dessa estrutura não encerra esses itens. Ela evita reiniciar o trabalho metodológico do zero.

## 13. Não autorizações

Este documento não aprova:

- um protocolo único para toda a pesquisa futura do ARA;
- a classificação de qualquer levantamento já realizado como revisão sistemática ou revisão de escopo formal sem auditoria específica;
- uma lista obrigatória de bases para toda pergunta;
- a lista histórica de idiomas como critério vigente de inclusão;
- uma string de busca universal;
- critérios universais de inclusão, exclusão, deduplicação ou avaliação de qualidade;
- dupla triagem quando ela não tiver sido realmente realizada;
- JBI, PRISMA-ScR ou qualquer ferramenta metodológica sem revalidação de versão e adequação ao estudo concreto;
- publicação de textos restritos ou dados de participantes;
- um formato físico obrigatório para registros bibliográficos;
- issue, formulário, roadmap ou outro mecanismo administrativo histórico como governança vigente;
- requisito de produto, arquitetura ou implementação.

A contribuição preservada é metodológica: uma investigação reproduzível precisa tornar visíveis a pergunta, a estratégia efetivamente executada, a procedência e o nível de acesso de cada fonte, as decisões de seleção, a extração, a qualidade e as limitações, além de separar os achados das inferências e decisões do projeto.