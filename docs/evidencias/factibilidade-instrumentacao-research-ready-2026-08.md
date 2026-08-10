# Evidências sobre factibilidade de instrumentação para pesquisa

**Categoria:** síntese de factibilidade, análise de sistema e concepção metodológica  
**Recorte temporal:** 5 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma revisão dirigida sobre como tornar o ARA apto a sustentar pesquisas educacionais sem transformar a instrumentação em uma segunda carga de interpretação por inteligência artificial nem em coleta indiscriminada de dados.

A revisão não autoriza implementação. Também não aprova objetos de domínio, campos, schemas, taxonomias, métricas, eventos, políticas de retenção, provedores, MCP, banco de dados, event store, dashboard, arquitetura, interface, coleta com participantes ou stack. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Problema de factibilidade

O problema investigado foi preservar classes de evidência suficientes para pesquisas futuras sem exigir que cada operação de autoria ou estudo seja reinterpretada por uma nova chamada de modelo.

A revisão registrou seis riscos principais:

- duplicar o esforço cognitivo da assistência autoral;
- exigir uma segunda análise semântica completa para telemetria;
- aumentar tokens, latência e custo sem benefício proporcional;
- reter indiscriminadamente conversas, contextos e eventos de interface;
- prejudicar planejamento, construção, auditoria, reparo e reauditoria;
- converter proxies operacionais em afirmações científicas sobre autoria, criticidade, qualidade ou aprendizagem.

A recomendação histórica foi preparar o produto para pesquisa sem torná-lo maximalista em coleta.

## 2. Quatro responsabilidades separadas

A revisão distinguiu quatro responsabilidades que não devem ser fundidas automaticamente:

1. **assistência autoral:** planeja, constrói, audita, repara ou reaudita dentro da autoridade concedida;
2. **registro determinístico pelo sistema:** preserva fatos que a aplicação já conhece ou pode calcular;
3. **instrumentação educacional:** emite observações ou eventos autorizados para uma finalidade declarada;
4. **análise posterior:** deriva medidas, codificações, construtos e interpretações sob método e autoridade próprios.

A separação evita usar inteligência artificial para redescobrir fatos já disponíveis ao sistema e mantém codificações científicas posteriores distintas do registro operacional primário.

## 3. Evidência primária por referência

A revisão propôs que uma operação possa ser reconstruída por referências persistentes, sem copiar integralmente o conteúdo em cada evento. Entre os elementos candidatos estavam:

- revisão-base;
- proposta ou artefato produzido;
- decisão humana pertinente;
- achados e observações utilizados;
- objetos-alvo;
- diferença efetivamente aplicada;
- revisão resultante;
- reauditoria ou validação posterior;
- configuração efetiva do agente.

O princípio residual é a **referenciabilidade** da evidência, não os nomes de campos nem um schema específico.

## 4. Evento operacional mínimo candidato

Foi explorado um evento pequeno, estruturado e versionado contendo apenas dados já conhecidos ou calculáveis pelo sistema, como identidade do evento, versão semântica, tempos, ator, ação, objeto, revisão do curso, operação, autoridade, resultado resumido e referências de contexto.

Esse desenho foi comparado conceitualmente com xAPI e Caliper, mas a revisão não concluiu que qualquer padrão externo deva definir a semântica interna do ARA.

O princípio de factibilidade é que fatos operacionais básicos não precisam passar por nova interpretação de linguagem natural para serem registrados.

## 5. Recibo de transformação candidato

Para mudanças que materializem uma nova revisão, a revisão investigou um registro determinístico capaz de relacionar:

- revisão-base e revisão resultante;
- tipo de operação e gatilho;
- alvos afetados;
- quantidades de propostas aceitas, rejeitadas ou modificadas;
- objetos criados, alterados ou removidos;
- validação;
- resolução de achados;
- regressões observadas em reauditoria;
- autoridade humana;
- configuração efetiva do agente.

Essas informações são exemplos do que o sistema poderia calcular. Não constituem campos obrigatórios nem contrato aprovado.

## 6. Codificação analítica posterior

Interpretações como autoria ratificadora, intervenção deliberativa, coprodução, criticidade ou dependência de inteligência artificial foram explicitamente separadas dos fatos operacionais.

Uma codificação analítica candidata precisaria registrar, conforme o método, o alvo analisado, esquema e versão de codificação, variáveis, codificador, evidências, confiança quando pertinente e estado de validação.

O resultado residual é uma restrição de método: **a codificação não sobrescreve o fato original e não recebe autoridade científica apenas por ter sido produzida por inteligência artificial**.

## 7. Informações observáveis e construtos

A revisão enumerou fatos que podem ser observados sem inferência científica, como:

- quem iniciou uma operação;
- quem propôs ou autorizou uma alteração;
- quantidades de itens aceitos, rejeitados ou modificados;
- número de rodadas deliberativas;
- objetos criados, alterados ou removidos;
- extensão estrutural de uma diferença;
- reversões posteriores;
- achados confirmados ou refutados;
- regressões detectadas;
- revisões e configurações efetivamente utilizadas.

Esses fatos podem apoiar perguntas de pesquisa, mas não demonstram automaticamente autoria intelectual, qualidade, criticidade, passividade, dependência, aprendizagem ou efetividade educacional.

## 8. Envelope estruturado na mesma inferência

Quando uma operação já exige interpretação de linguagem natural, a revisão explorou a possibilidade de retornar um envelope estruturado mínimo **na mesma inferência**, por exemplo para relacionar itens aceitos, rejeitados, modificados, requisitos adicionados, alvos novos e ambiguidades ainda não resolvidas.

A proposta possui limites explícitos:

- não provocar uma segunda chamada apenas para telemetria;
- usar poucos campos;
- não exigir justificativa semântica adicional extensa;
- permitir validação determinística e correção posterior;
- não classificar autoria, criticidade ou qualidade em tempo real.

O envelope permanece alternativa de factibilidade. Nenhum formato ou contrato foi aprovado.

## 9. Análises diferidas

A revisão recomendou não colocar no fluxo autoral obrigatório tarefas de alto custo ou grande carga interpretativa, como:

- classificação de autoria passiva ou crítica;
- análise argumentativa detalhada;
- inferência de dependência de inteligência artificial;
- avaliação global de qualidade da interação;
- agrupamento semântico em grande escala;
- comparação longitudinal de linhagens;
- process mining;
- codificação qualitativa;
- análise causal;
- explicações científicas.

Essas tarefas podem ser investigadas posteriormente, sob protocolo, em lote, por amostragem ou com validação humana, conforme o método adotado.

## 10. Instrumentação ativada por finalidade

A revisão manteve a distinção entre **capacidade de instrumentar** e **autorização para coletar**.

Um protocolo candidato poderia selecionar perguntas, população, condições, conjuntos de parâmetros, eventos autorizados, instrumentos, retenção, direitos, pseudonimização, exportação e plano de análise. Essa enumeração é um espaço de investigação, não um objeto de domínio aprovado.

A existência de suporte técnico não autoriza coleta universal, e a coleta ampliada não deve decorrer apenas da disponibilidade de um evento.

## 11. Perfil de custo investigado

A revisão organizou três ordens de custo.

### Registro de baixo custo conceitual

- identificadores e relações;
- diferenças estruturais;
- contagens;
- estado de validação;
- parâmetros efetivos;
- fatos já conhecidos pelo sistema;
- eventos emitidos diretamente pela interface quando autorizados.

### Acréscimo potencialmente reduzido

- envelope estruturado na mesma inferência já necessária;
- tipo amplo de operação;
- dimensão ampla de um achado já produzida durante auditoria;
- referências aos itens discutidos.

### Processamento a diferir

- resumo semântico integral de sessão;
- autoria percentual;
- análise de sentimento;
- classificação de criticidade;
- comparação com histórico integral;
- narrativa automática de proveniência;
- codificação científica completa.

Essas classificações são hipóteses de custo a medir, não resultados de benchmark.

## 12. Classes históricas de retenção

A revisão explorou três classes de retenção.

### Evidência candidata a retenção durável

Incluía revisões, relações de derivação, registros de transformação, configuração efetiva do agente, achados ou decisões diretamente usados, instrumentos e parâmetros efetivos e referências a protocolos ou conjuntos de dados congelados.

### Conteúdo candidato a retenção configurável

Incluía mensagens completas, respostas brutas de modelos, contexto recuperado, propostas rejeitadas detalhadas, eventos finos de navegação, anexos e telemetria técnica ampliada.

### Estado candidato a tratamento transitório

Incluía digitação, undo/redo, hover, foco, movimentos, caches, respostas inválidas e checkpoints locais não promovidos.

As classes são alternativas históricas. Prazos, públicos, eliminação, direitos, retenção jurídica e uso secundário permanecem questões de `PROV-004`, `DATA-002` e infraestrutura.

## 13. Workloads propostos para avaliar factibilidade

Antes de congelar qualquer schema, a revisão propôs medir cenários indicativos com:

- cursos de tamanhos diferentes;
- 10, 100 e 1.000 autores ou estudantes;
- 10 mil, 100 mil e 1 milhão de revisões ou eventos;
- diferentes políticas de retenção;
- envelope estruturado habilitado e desabilitado;
- custo e latência da assistência;
- tamanho médio de registros;
- custo de consulta e exportação;
- reconstrução de conjuntos de dados;
- backup e restauração;
- pseudonimização e eliminação conforme política.

Essas escalas são cenários de benchmark, não requisitos de capacidade aprovados.

Para o envelope adicional, a revisão sugeriu medir:

- ausência de segunda chamada;
- acréscimo de tokens;
- eventual degradação da qualidade do artefato;
- taxa de parse e validação;
- comportamento quando a estrutura não puder ser classificada.

Nenhum limiar de aceite foi aprovado.

## 14. Programa histórico de validação

A sequência investigada foi:

1. extrair jornadas reais da referência funcional;
2. identificar fatos que o sistema já conhece;
3. prototipar um núcleo de eventos sem inteligência artificial adicional;
4. prototipar um envelope mínimo na mesma inferência;
5. medir tokens, latência, erro e qualidade do artefato;
6. testar a taxonomia com codificadores humanos e agentes;
7. verificar concordância e categorias ausentes;
8. simular perguntas de pesquisa e verificar suficiência dos dados;
9. comparar retenção mínima e extensiva;
10. somente depois formular schema candidato e decisão arquitetural.

Essa sequência permanece proposta de investigação. Não autoriza protótipo ou desenvolvimento no estágio atual.

## 15. Fontes iniciais registradas

A revisão dirigida utilizou principalmente padrões e documentação oficial como ponto de partida:

- W3C PROV-O e documentos relacionados do modelo de proveniência;
- Experience API, xAPI;
- 1EdTech Caliper Analytics 1.2 e perfis de métricas;
- CRediT Contributor Roles Taxonomy, ANSI/NISO Z39.104-2022.

A revisão não se apresenta como levantamento acadêmico abrangente. Ela própria registrou a necessidade futura de aprofundar literatura sobre colaboração humano-IA, learning analytics, trace data, process mining, instrumentos de percepção, privacidade, ética e plataformas experimentais educacionais.

## 16. Relação com as pendências vigentes

Na orientação atual:

- `PROV-004` mantém aberta a definição dos fatos operacionais mínimos e da retenção sustentável;
- `DATA-003` mantém aberta a semântica de eventos, medidas, analytics e interoperabilidade;
- `DATA-002` mantém aberta a governança de coleta, acesso, retenção e uso secundário;
- `AGENT-001` mantém aberta a avaliação de agentes e análises assistidas;
- `AUTH-002` mantém separadas contribuição observável, papel e autoridade;
- `VAL-001` e `VAL-002` mantêm abertos os corpora, estados e evidências de validação;
- `INF-001` mantém abertos custo, desempenho, armazenamento, backup, restauração e workloads;
- `DEC-005` preserva a separação entre deliberação e materialização;
- `DEC-006` preserva a inteligência artificial como assistente sem autoridade de aprovação ou publicação;
- `DEC-007` impede interpretar esta revisão como autorização para implementação.

A revisão de factibilidade, portanto, preserva critérios e perguntas para investigação futura sem selecionar tecnologia, schema ou política de coleta.