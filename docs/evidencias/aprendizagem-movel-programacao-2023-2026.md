# Evidências sobre aprendizagem móvel de programação, 2023 a 2026

**Categoria:** síntese de pesquisa e evidência educacional  
**Recorte temporal:** 2 de agosto de 2026  
**Estado:** histórico, provisório e não normativo

Este documento preserva uma atualização crítica sobre aprendizagem móvel de programação e temas adjacentes. A atualização parte de uma revisão sistemática publicada em 2023 sobre ferramentas móveis para lógica e programação introdutória e acrescenta estudos e revisões posteriores localizados até o recorte temporal indicado.

A finalidade desta evidência é manter separadas categorias que não podem ser usadas como equivalentes:

- aplicativo móvel e microlearning;
- microlearning e currículo completo;
- execução automatizada e feedback pedagógico;
- satisfação, confiança, engajamento ou continuidade e aprendizagem;
- geração de código e aprendizagem de programação;
- pesquisa sobre inteligência artificial em programação e pesquisa sobre aprendizagem móvel.

A atualização não se apresenta como revisão exaustiva. Seu próprio desenho registra dependência de buscas formais posteriores e preserva lacunas, evidências negativas e limites de transferência.

## 1. Corpus estruturado preservado

A atualização organiza oito registros principais entre revisões sistemáticas, revisão de escopo, estudo comparativo de experiência e estudo transversal.

| Referência resumida | Ano | Tipo | Escopo ou amostra | Limite crítico registrado |
|---|---:|---|---|---|
| Coelho, Marques e Oliveira | 2023 | revisão sistemática | 12 ferramentas móveis, estudos de 2011 a 2022 | três bases, heterogeneidade de tarefas e resultados, dados incompletos sobre participantes e duração |
| Moore, Hwang e Moses | 2024 | revisão sistemática | 9 estudos de microlearning móvel em adultos | corpus pequeno, heterogêneo e não específico de programação |
| Messer, Brown, Kölling e Shi | 2024 | revisão sistemática | 121 trabalhos sobre correção e feedback automatizados | feedback frequentemente reduzido a aprovação/reprovação ou esperado/observado; datasets muitas vezes indisponíveis |
| Wibisono, Maringga e Sunardi | 2024 | estudo comparativo de UX | Mimo e SoloLearn | experiência de uso não demonstra aprendizagem ou transferência |
| Monib, Qazi e Apong | 2024 | revisão sistemática | 40 estudos de microlearning | definições e desenhos heterogêneos; não específico de programação |
| Parrales-Bravo | 2026 | revisão sistemática ou de escopo | 21 estudos empíricos em engenharia de software | concentração em introdução; pouca evidência sobre arquitetura, requisitos, testes, manutenção e transferência longitudinal |
| Essel | 2026 | estudo transversal | 708 estudantes de graduação em uma universidade de Gana | uma instituição, autorrelato parcial, seleção dos usuários e ausência de inferência causal |
| Livaja Mušac, Nakić e Sović Kržić | 2026 | revisão sistemática | 39 estudos de avaliação automática de programação | validação empírica limitada, comparação humana insuficiente e pouco trabalho com programação visual ou por blocos |

Os identificadores DOI registrados na atualização são, respectivamente:

- `10.15388/infedu.2023.24`;
- `10.30191/ETS.202401_27(1).SP02`;
- `10.1145/3636515`;
- `10.1109/ICIMTech63123.2024.10780836`;
- `10.1016/j.heliyon.2024.e41413`;
- `10.3390/educsci16030487`;
- `10.25082/AMLER.2026.02.003`;
- `10.3390/app16115658`.

A presença no corpus não implica adoção de mecanismo, aplicativo, tecnologia ou conclusão educacional.

## 2. Linha de base sobre ferramentas móveis

A revisão de 2023 examinou literatura de 2011 a 2022 e identificou doze ferramentas móveis para programação introdutória. As atividades descritas eram cognitivamente diferentes, incluindo:

- reconhecimento de conceitos;
- ordenação;
- previsão de resultados;
- identificação de erros;
- produção de código;
- execução.

Feedback automático aparecia com frequência, mas parte importante dos estudos media motivação, engajamento, aceitação, percepção ou usabilidade em vez de retenção ou transferência.

Essa diferença é metodologicamente relevante para o ARA: presença de uma funcionalidade ou resultado positivo de experiência não deve ser transformado em evidência de aprendizagem.

## 3. Microlearning e integração curricular

As revisões posteriores registram experimentação com unidades breves, formatos móveis, gamificação e projetos, mas também concentração em programação introdutória e conhecimento declarativo.

Áreas pouco representadas incluem:

- arquitetura de software;
- engenharia de requisitos;
- estratégias de teste;
- manutenção de sistemas complexos;
- integração de competências técnicas e profissionais;
- desempenho autêntico longitudinal.

A consequência provisória é limitada: unidades breves podem apoiar objetivos delimitados, revisão e prática distribuída, mas a evidência preservada não sustenta apresentá-las como substitutas de projetos, integração conceitual ou desempenho profissional complexo.

A duração também não define por si só a natureza pedagógica de uma atividade. Uma unidade breve continua dependente de objetivo, integração instrucional, tarefa, feedback, progressão e contexto de uso.

## 4. Aprendizagem autodirigida e experiência de uso

O estudo transversal sobre SoloLearn registra associações entre autogestão, motivação, monitoramento, estratégias e desempenho percebido ou acadêmico, além de problemas como conteúdo avançado restrito, anúncios e feedback insuficiente.

A interpretação permanece restrita porque o estudo é transversal, localizado em uma única instituição e parcialmente autorrelatado. Intensidade de uso não pode ser tratada como medida direta de aprendizagem.

A comparação de experiência entre Mimo e SoloLearn reforça outra separação necessária:

- facilidade de uso;
- utilidade percebida;
- satisfação;
- continuidade;
- aprendizagem observada;
- transferência para produção de programas.

Esses desfechos podem se relacionar, mas não são intercambiáveis.

## 5. Avaliação e feedback automatizados

A revisão de 121 trabalhos sobre correção e feedback automatizados identifica mecanismos recorrentes:

- testes unitários;
- comparação de saída;
- análise estática;
- comparação com solução de referência;
- retorno quase imediato;
- múltiplos reenvios.

Também registra pouca avaliação de legibilidade, manutenção e documentação e indisponibilidade frequente de conjuntos de avaliação.

O principal cuidado conceitual é que **feedback automático não é necessariamente feedback explicativo**. Uma mensagem de compilador, um teste falho, uma diferença entre saída esperada e observada, uma pista e uma explicação pedagógica correspondem a camadas distintas.

## 6. Avaliação automática com inteligência artificial

A revisão de 39 estudos sobre avaliação automática descreve métodos que vão de execução e análise estática a aprendizagem de máquina, aprendizagem profunda e modelos de linguagem.

A evidência preservada registra potencial para feedback mais rico, mas também:

- validação empírica ainda limitada;
- comparação insuficiente com avaliadores humanos;
- questões de confiabilidade;
- pouca pesquisa em programação visual ou por blocos;
- necessidade de avaliação pedagógica e de combinações híbridas.

Por isso, a expressão "avaliado por IA" é insuficiente como descrição metodológica. Estudos e futuros mecanismos precisam distinguir, quando aplicável:

- teste determinístico;
- análise estática;
- regra ou padrão;
- classificador estatístico;
- modelo generativo;
- avaliação humana;
- combinação entre métodos;
- possibilidade de revisão ou contestação.

Essa taxonomia é evidência de investigação, não contrato de validação aprovado.

## 7. Taxonomia de tarefas de programação

A síntese organiza sete famílias de tarefas que não devem ser tratadas como equivalentes.

### 7.1 Conhecimento declarativo

Inclui conceitos, sintaxe, vocabulário, finalidade de comandos e reconhecimento de estruturas. Questões de seleção ou respostas textuais podem exercitar esse nível, mas não substituem desempenho em código.

### 7.2 Leitura e rastreamento

Inclui prever saída, acompanhar estado de variáveis, identificar caminho de execução, interpretar trechos e reconhecer efeitos. Pode exigir representações auxiliares, como tabelas de rastreamento.

### 7.3 Detecção e explicação de erros

Inclui localizar erros sintáticos ou semânticos, explicar falhas lógicas, interpretar mensagens e propor correções. Localizar, corrigir e explicar são respostas diferentes.

### 7.4 Completar e ordenar

Inclui preencher lacunas, escolher expressões, ordenar blocos, montar algoritmos e completar funções. Soluções semanticamente equivalentes podem exigir tratamento diferente de simples correspondência literal.

### 7.5 Produção e execução

Inclui escrever expressões, funções ou programas, executar, verificar testes, corrigir, reenviar e explicar escolhas. A avaliação pode combinar mecanismos diferentes, sem que a presença de um deles determine a autoridade dos demais.

### 7.6 Depuração

Inclui reproduzir falha, formular hipótese, inspecionar estado, alterar código e validar a correção. A depuração é processo iterativo, não apenas resultado final correto ou incorreto.

### 7.7 Projeto e transferência

Inclui resolver problemas novos, decompor requisitos, selecionar estruturas, integrar componentes, testar, documentar, revisar e manter. A evidência preservada indica que essa família é menos compatível com unidades isoladas e mais dependente de integração longitudinal.

## 8. Matriz de caracterização

A síntese propõe caracterizar sistemas e estudos por dimensões distintas, entre elas:

- domínio;
- tarefa;
- unidade de aprendizagem;
- presença e extensão de teoria;
- ambiente de execução;
- método de avaliação;
- tipo de feedback;
- política de tentativas;
- progressão;
- consequência;
- desfecho medido;
- natureza da evidência.

A utilidade desta matriz está em impedir comparações inadequadas entre estudos que medem objetos diferentes. Seus valores e categorias continuam sujeitos a revisão e não constituem schema do produto.

## 9. Sistemas nominalmente relacionados

SoloLearn possui literatura direta localizada, mas os resultados preservados ainda deixam abertas validação longitudinal, tarefas autênticas e controle de conhecimentos prévios.

Mimo aparece em comparação de experiência de uso, com evidência mais forte para experiência do que para aprendizagem ou transferência.

Encode e Enki permanecem antecedentes observados, mas a atualização não localizou base independente suficiente para conclusões educacionais sobre eles.

Ambientes de correção automática também são relevantes, mesmo quando não são aplicativos móveis, porque expõem mecanismos de execução, pontuação, feedback e reenvio que podem ser utilizados em superfícies móveis ou responsivas.

Nenhum desses sistemas é requisito, modelo de produto ou tecnologia selecionada.

## 10. Evidências negativas e abandono

A atualização preserva como fatores que precisam ser observados, e não descartados como ruído:

- anúncios e interrupções;
- limitações de conteúdo avançado;
- feedback insuficiente;
- falhas técnicas;
- poucos exemplos;
- dificuldade de corrigir erros;
- distância entre exercícios breves e tarefas reais;
- custo, assinatura e arrependimento de compra;
- continuidade e abandono;
- acessibilidade;
- funcionamento offline.

Abandono não demonstra, por si só, falta de disciplina do estudante. Desenho, custo, relevância, carga, contexto e barreiras precisam ser examinados antes de qualquer interpretação.

## 11. Limite da frente de inteligência artificial

A atualização inclui inteligência artificial apenas quando ela participa diretamente de avaliação de código, feedback, pistas, diagnóstico de erros ou adaptação de tarefas em contexto de aprendizagem de programação.

Não entram automaticamente na mesma categoria:

- uso geral de chatbots por programadores;
- geração de código sem desenho educacional;
- produtividade profissional;
- detecção genérica de código;
- estudos sem relação com aprendizagem móvel, microlearning ou prática estruturada.

Essa delimitação impede que literatura ampla sobre IA em programação seja usada como substituta de evidência sobre aprendizagem móvel.

## 12. Lacunas registradas

Permanecem lacunas sobre:

- estudos experimentais ou longitudinais de aplicativos comerciais;
- retenção tardia e transferência para problemas novos;
- adultos trabalhadores e estudo sob transporte ou interrupção;
- contextos do Brasil e de Portugal;
- programação além do nível introdutório;
- arquitetura, requisitos, testes e manutenção;
- acessibilidade de editores móveis;
- funcionamento offline;
- relação entre pistas, reenvios e dependência;
- validade de feedback gerado por modelos;
- custos e desigualdade de acesso;
- comparação entre ambientes móveis e desktop;
- efeitos de publicidade e assinatura;
- experiência negativa e abandono.

Essas lacunas permanecem pendências futuras de pesquisa. Esta consolidação não executa buscas adicionais para preenchê-las.

## 13. Consequências provisórias para investigação do ARA

A síntese histórica recomenda que futuras investigações consigam representar e comparar, sem fixar padrões antecipadamente:

- atividades declarativas e executáveis;
- ambientes de código como capacidades específicas de domínio;
- testes públicos e protegidos;
- tentativas e pistas graduais;
- feedback técnico e pedagógico separados;
- transferência e projetos além de unidades isoladas;
- unidades breves integradas a percursos mais longos;
- autoria, versão e procedência de exercícios;
- satisfação separada de aprendizagem;
- avaliação determinística, probabilística e humana identificada;
- funcionamento móvel, offline e retomada.

Esses pontos são **recomendações e perguntas de investigação**, não requisitos aprovados. Eles devem ser lidos em conjunto com as pendências vigentes sobre lacunas de interação, precedentes externos, validação, acessibilidade, factibilidade e separação entre resposta, avaliação e retorno pedagógico.

## 14. Relação com a orientação vigente

Esta evidência é compatível com a orientação de continuidade funcional sem herança automática de arquitetura e com o estágio de pré-desenvolvimento do projeto.

Ela não seleciona:

- SoloLearn, Mimo, Encode, Enki ou outro aplicativo;
- linguagem de programação;
- editor;
- compilador ou interpretador;
- sandbox;
- runtime;
- biblioteca de avaliação;
- modelo de linguagem;
- mecanismo de feedback;
- política de tentativas;
- plataforma móvel ou desktop;
- arquitetura ou implementação.

A contribuição preservada é metodológica e comparativa: diferentes tarefas de programação, mecanismos de avaliação e tipos de resultado exigem evidências distintas, e resultados de uso ou experiência não podem ser promovidos silenciosamente a evidência de aprendizagem.