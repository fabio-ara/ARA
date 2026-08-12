# Métodos históricos de avaliação e validação

**Categoria:** método de avaliação, plano de validação técnica e evidência de pesquisa  
**Recorte temporal:** agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva dois planos complementares elaborados durante a definição do ARA: um plano de conformance arquitetural e um plano formativo de avaliação de experiência de uso. Eles registram perguntas, cenários, métodos e formas de evidência que podem orientar avaliações futuras.

Os planos não constituem validação do produto, não autorizam implementação e não transformam critérios históricos em requisitos vigentes. As decisões aprovadas permanecem em `DECISOES.md`, e as questões abertas permanecem em `BACKLOG.yaml`.

## 1. Escopos de avaliação distintos

O plano de conformance arquitetural tratava da pergunta: uma implementação ou perfil de implantação preserva propriedades técnicas e semânticas declaradas sob os cenários exercitados?

O plano de avaliação de experiência tratava de perguntas diferentes: pessoas conseguem compreender estados e consequências, concluir tarefas, recuperar-se de falhas e operar as interfaces com acessibilidade adequada?

Nenhum dos dois planos pretendia demonstrar efetividade educacional. A aprovação em conformance também não autorizava alegações de escala de produção além dos workloads efetivamente testados.

## 2. Suítes históricas de conformance arquitetural

O plano técnico organizava nove famílias de verificação. Elas são preservadas como repertório de investigação, não como suíte de release vigente.

1. **Domínio e pacotes:** identidade, versões, digests, ocorrências contextuais, snapshots de configuração, licenças e descrições de capacidades.
2. **Funcionamento offline:** instalação ou disponibilidade local, materialização recuperável, estudo, retomada, remoção, pressão de armazenamento e recuperação da versão anterior.
3. **Sincronização:** repetição segura de operações quando necessária, divergência de revisão, reexecução, reaplicação, fork, efeitos de revogação e remoção. Mecanismos históricos como outbox e `expected revision` eram exemplos de desenho, não contratos aprovados.
4. **Operações assistidas e integração por ferramentas:** autorização, descoberta e contexto delimitados, validação de contratos, registro de operações, erros recuperáveis e proibição de autopublicação. O plano usava MCP como mecanismo histórico; isso não seleciona MCP para o ARA.
5. **Segurança e privacidade:** threat model, mínimo privilégio, validação de conteúdo, expiração de acesso temporário quando aplicável, espaços confidenciais e separação de dados de pesquisa. Mecanismos específicos de URL assinada ou política de provedor permanecem alternativas históricas.
6. **Pesquisa:** snapshot de condição, autorização de eventos e instrumentos, retirada, retenção, exportação e equivalência semântica entre perfis de implantação quando essa comparação for necessária.
7. **Capacidades:** comportamento quando uma capacidade é requerida, opcional ou indisponível, fallback explícito e ausência de corrupção de fluxos não relacionados.
8. **Operações de implantação:** instalação, migração, backup, restauração, diagnóstico, atualização e rollback.
9. **Desempenho, acessibilidade e localização:** medições e verificações em ambientes documentados. Budgets e limiares históricos não são SLAs nem critérios de aceite atuais.

## 3. Fixtures representativos propostos

O plano de conformance propunha um conjunto de casos de contraste para evitar que a validação técnica dependesse apenas de cenários triviais:

- curso pequeno com estudo offline inspirado na referência funcional anterior;
- curso maior com recursos reutilizados em diferentes ocorrências;
- operações de autoria offline em conflito;
- espaço institucional confidencial;
- condição de pesquisa com eventos ou instrumentos autorizados;
- pacote educacional aberto com materiais de terceiros sob licenças distintas;
- capacidade de inteligência artificial ou runtime indisponível;
- exportação da referência anterior submetida a uma migração experimental.

Esses casos são candidatos de corpus para avaliação. Sua presença em um plano não aprova migração, formato de pacote, modelo institucional, política de inteligência artificial ou arquitetura de sincronização.

## 4. Evidência mínima para alegações de conformance

O plano propunha que toda alegação de arquitetura ou release preservasse, conforme aplicável:

- versões das ferramentas usadas;
- ambiente de execução;
- identidade ou digest do fixture;
- resultado observado;
- limitações;
- artefatos produzidos.

Esse princípio continua metodologicamente útil: um resultado deve ser interpretável segundo o instrumento, o ambiente, o caso testado e seus limites. Passar em conformance não demonstra aprendizagem e não demonstra desempenho ou escala além do workload exercitado.

## 5. Objetivos históricos da avaliação formativa de experiência

O plano de experiência de uso propunha avaliar quatro dimensões principais:

- compreensão do estado e das consequências das ações;
- conclusão de tarefas representativas;
- acessibilidade das interações;
- recuperação diante de falhas, conflitos ou estados offline.

A formulação histórica falava em contratos de tela então considerados aprovados. Na orientação vigente, somente decisões explicitamente registradas em `DECISOES.md` possuem essa autoridade. Os demais fluxos e telas permanecem candidatos de pesquisa ou exploração.

## 6. Públicos e papéis considerados

O plano propunha avaliação formativa com diversidade de papéis, incluindo:

- estudantes autodirigidos, inclusive pessoas que estudam em sessões breves ao longo da rotina de trabalho;
- autores, docentes e tutores sem conhecimento especializado de bancos de dados;
- revisores e pesquisadores;
- pessoas usuárias de tecnologias assistivas e especialistas em acessibilidade;
- administradores institucionais.

O próprio plano proibia inferir autorização de recrutamento ou coleta de dados. Qualquer execução com participantes exige protocolo aprovado, governança adequada e definição explícita dos usos permitidos dos dados.

## 7. Tarefas formativas propostas

O plano histórico registrava dez tarefas de contraste:

1. tornar um curso disponível localmente e retomar o estudo sem rede;
2. explicar versão atual, perfil ou configuração relevante e estado offline;
3. alterar um parâmetro de alto impacto e distinguir mudança de runtime, conteúdo ou composição;
4. inspecionar artefatos produzidos com assistência de inteligência artificial, comentar um elemento e solicitar reparo delimitado;
5. distinguir referência, cópia e fork;
6. auditar sem editar, autorizar reparo e verificar o resultado;
7. publicar para audiência delimitada e identificar audiência, versão e possibilidade de retirada;
8. resolver conflito de autoria offline sem perder o trabalho local;
9. montar um protocolo mínimo de pesquisa e distinguir evento, medida e construto;
10. alterar um papel de workspace sem criar autoridade administrativa global.

Essas tarefas não são requisitos de fluxo atuais. Várias dependem de decisões ainda abertas sobre modelo de conteúdo, colaboração e acesso, parametrização, publicação, pesquisa e sincronização. O plano usava GPT como exemplo histórico de assistência; isso não seleciona provedor, modelo ou protocolo de integração.

## 8. Métodos formativos propostos

O repertório metodológico incluía:

- walkthroughs moderados de tarefas;
- think-aloud, com cautela para não aumentar indevidamente a carga cognitiva ou prejudicar participantes em avaliações de acessibilidade;
- perguntas de compreensão após decisões consequenciais;
- inspeção por teclado e leitor de tela, além de zoom e reflow;
- walkthrough de desempenho e usabilidade em dispositivo físico de entrada;
- revisão heurística e revisão por especialista em acessibilidade;
- revisão de localização;
- injeção de falhas usando estados estáticos ou protótipos.

O Samsung Galaxy A07 aparecia historicamente como classe de dispositivo representativo para alguns ensaios. Ele não é gate vigente nem dispositivo obrigatório. Da mesma forma, a revisão em inglês, português do Brasil e português de Portugal era uma proposta histórica de localização; o escopo futuro de idiomas da interface continua aberto.

## 9. Critérios históricos de sucesso

O plano propunha observar se:

- tarefas críticas eram concluídas sem correção do moderador;
- a pessoa conseguia explicar alvo, versão e consequência antes de publicar, excluir, derivar ou alterar configuração relevante;
- nenhuma ação essencial dependia exclusivamente de arraste, hover, visão ou cor;
- erros preservavam o trabalho já produzido e apresentavam recuperação compreensível;
- participantes distinguiam estado local/offline de estado sincronizado ou publicado;
- autores localizavam comentários e achados e distinguiam auditoria de reparo;
- pesquisadores distinguiam eventos, medidas e construtos;
- problemas de acessibilidade críticos eram identificados e bloqueavam a conclusão do ensaio quando necessário;
- achados permaneciam ligados à tela ou estado exercitado e voltavam ao modelo ou à arquitetura quando o problema era semântico, não apenas de interface.

O plano usava ausência de bloqueador crítico de WCAG 2.2 AA como limiar histórico. O alvo WCAG 2.2 AA permanece referência a validar no backlog atual, não requisito aprovado por este documento.

## 10. Pacote de evidências da avaliação de experiência

Para tornar a avaliação auditável, o plano propunha preservar:

- versão do protótipo;
- roteiro das tarefas;
- ambiente de execução;
- governança dos participantes;
- achados e severidade;
- política de gravações e notas;
- idioma ou locale, dispositivo e tecnologia assistiva quando aplicáveis;
- decisões tomadas após a avaliação;
- riscos não resolvidos.

A presença de uma decisão nesse pacote não a torna decisão canônica. Mudanças de produto continuam dependendo do processo registrado em `METODO_DE_TRABALHO.md` e `DECISOES.md`.

## 11. Relação com as pendências vigentes

Os dois planos fornecem método e casos para questões já abertas:

- `VAL-001`: construir corpus representativo de cursos, estados, capacidades ausentes, conflitos e falhas recuperáveis;
- `VAL-002`: distinguir validade, satisfação de critérios, disponibilidade de capacidade, autoridade e evidências;
- `UX-002`: avaliar arquitetura de informação e divulgação progressiva com tarefas representativas;
- `UX-003`: tornar estados offline, conflito, permissão, falha e recuperação compreensíveis;
- `UX-004` e `PED-004`: avaliar teclado, foco, reflow, alternativas não visuais e tecnologias assistivas;
- `INF-001`: medir factibilidade, desempenho, implantação, backup, restauração e limites operacionais;
- `SCOPE-002` e `DEC-007`: impedir que planos de teste históricos sejam tratados como gates atuais de implementação;
- `DEC-006`: preservar funcionamento offline, uso móvel e controle humano sem herdar automaticamente a arquitetura da referência funcional.

Os planos não resolvem essas pendências. Eles preservam um repertório de perguntas, cenários, métodos e evidências para investigações futuras.

## 12. Não autorizações

Este documento não aprova:

- suíte de conformance como gate de release atual;
- contrato de package, capability manifest ou formato de migração;
- outbox, `expected revision`, URL assinada, MCP ou qualquer mecanismo específico citado nos planos históricos;
- Galaxy A07 ou outro dispositivo como requisito;
- WCAG 2.2 AA como baseline já decidido;
- inglês ou português de Portugal como idiomas obrigatórios da interface;
- recrutamento, gravação ou coleta de dados de participantes;
- telas, fluxos, papéis ou políticas de publicação ainda não decididos;
- arquitetura, stack ou implementação.

A contribuição preservada é metodológica: avaliações futuras devem declarar a pergunta, o instrumento, o ambiente, o caso exercitado, a autoridade do resultado e suas limitações, mantendo conformance técnica, usabilidade, acessibilidade, efetividade educacional e escala como categorias distintas.