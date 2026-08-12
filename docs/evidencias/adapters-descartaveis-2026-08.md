# Evidências da rodada de adapters descartáveis

**Categoria:** protótipo técnico e evidência de pesquisa  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma rodada executável de prototipagem usada para testar se uma fronteira estreita de adapter poderia atender quatro famílias de atividade materialmente diferentes sem incorporar geometria de renderização, estado transitório de runtime, campos de bibliotecas externas ou testes protegidos à resposta canônica.

O código, os testes e os relatórios da rodada foram preservados como [artefato executável de pesquisa](prototipos/adapters-descartaveis-01/README.md). O artefato não é componente de produção, não seleciona stack e não autoriza implementação.

## 1. Pergunta investigada

A rodada buscou verificar, em um recorte controlado, se quatro famílias poderiam compartilhar um lifecycle operacional reduzido e uma fronteira canônica de resposta sem apagar suas diferenças semânticas:

- matemática semântica;
- construção relacional;
- programação executável;
- argumento com fontes.

O lifecycle ensaiado foi:

```text
load(instance)
start()
importResponse(response)
exportResponse()
validate(options)
produceFeedback(validation)
dispose()
```

A hipótese testada era de interface entre o núcleo e adapters substituíveis. O resultado não aprova esse lifecycle como contrato do produto.

## 2. Fronteira canônica e estado derivado

A rodada tratou `exportResponse()` como fronteira canônica experimental. O objetivo foi demonstrar que estado necessário à resposta pode permanecer separado de detalhes do renderer ou do runtime.

Na construção relacional, por exemplo, posições dos nós são derivadas para renderização e removidas da resposta exportada. O teste de round-trip confirmou que a resposta semântica pode ser exportada e importada novamente sem coordenadas ou `rendererState`.

Esse resultado sustenta a investigação de separação de responsabilidades, mas não aprova formato JSON, nomes de campos, classes, schemas ou granularidade de contratos.

## 3. Matemática semântica

O adapter matemático separou quatro estados que não devem ser confundidos:

- entrada sintaticamente inválida;
- interpretação semântica válida;
- equivalência com a referência;
- satisfação da forma solicitada.

A rodada demonstrou os casos `2*(x+`, `2*x+6` e `2*(x+3)` como, respectivamente, inválido, parcialmente satisfatório e satisfatório para a atividade de fatoração usada no ensaio.

A equivalência foi estimada por avaliação em um conjunto determinístico de pontos. A própria análise rejeitou esse procedimento como prova matemática geral ou validador produtivo. Um sistema real precisaria de escopo formal e autoridade de validação adequados ao domínio.

## 4. Construção relacional

O adapter relacional manteve nós, arestas, restrições e log de operações como estado semântico e calculou o layout visual separadamente.

O cenário ensaiado exigiu as arestas A-B e B-D. A validação verificou integridade estrutural, operações permitidas, existência de caminho e igualdade do conjunto de arestas.

A interface forneceu alternativa linear à representação SVG e operações por controles convencionais, sem exigir arraste. Isso demonstra uma possibilidade de separar semântica, geometria e interação, mas não valida grafos densos, outras gramáticas relacionais nem acessibilidade completa.

## 5. Programação executável

A rodada separou resposta de código, testes públicos, testes protegidos, execução e evidência diagnóstica.

No caminho Node, testes protegidos foram injetados pelo host e não apareceram na resposta exportada. No navegador, apenas testes públicos foram executados. Parsing inválido, falha de teste e timeout receberam estados distintos.

Dois resultados negativos são centrais:

- Web Worker não foi considerado fronteira de segurança suficiente contra código hostil;
- Node `vm` não foi considerado fronteira de segurança suficiente contra código hostil.

Essas rejeições valem para a função de sandbox produtiva no recorte ensaiado. Elas não proíbem Worker ou `vm` em funções que não façam alegação equivalente de isolamento.

Container, microVM, runtimes de navegador e serviços protegidos continuam alternativas não selecionadas.

## 6. Argumento com fontes

O quarto adapter separou integridade documental de avaliação interpretativa.

Fontes foram identificadas por digest. Seletores registraram citação, contexto e offsets. Quando offsets foram deliberadamente alterados, o protótipo conseguiu reencontrar o trecho pela combinação de citação e contexto.

A integridade do vínculo foi verificada deterministicamente, enquanto relevância da evidência e qualidade da justificativa permaneceram sob revisão humana. O ensaio, portanto, não atribuiu ao mecanismo de seleção autoridade para avaliar a qualidade do argumento.

## 7. Testes Node registrados

O relatório da rodada registra seis testes executados em Node.js 22.16.0 sobre Linux x64.

Resultado registrado: **6 de 6 aprovados**.

A cobertura foi limitada a:

1. estados matemáticos inválido, parcial e correto;
2. round-trip relacional sem geometria do renderer;
3. exclusão dos testes protegidos da resposta de programação;
4. parsing, falha e timeout de programação;
5. re-resolução de seletor e passagem para revisão humana;
6. round-trip de resposta canônica nas quatro famílias.

Esse resultado valida somente os casos exercitados no protótipo. Não é validação do produto, de efetividade educacional, segurança produtiva, escalabilidade ou interoperabilidade geral.

## 8. Walkthrough de navegador registrado

O walkthrough automatizado registrou quinze verificações em Chromium 144.0.7559.96.

Resultado registrado: **15 de 15 aprovadas**.

Foram exercitados estados de matemática, construção relacional, ausência de geometria na resposta, alternativa linear ao grafo, testes públicos de programação, ausência de testes protegidos no cliente, timeout, revisão humana, re-resolução de seletor, ordem de foco, regiões de status e reflow em 320 CSS pixels.

O relatório não registrou solicitações externas de rede, além de URLs `blob:` internas criadas para workers.

A aprovação do walkthrough não é estudo com usuários, conformidade de acessibilidade nem evidência de segurança de produção.

## 9. Inspeção de acessibilidade

Uma inspeção da árvore de acessibilidade do Chromium registrou:

- controles com nomes acessíveis;
- sete nós de status;
- seis headings;
- regiões `aria-live` educadas e assertivas.

A própria fonte limita o resultado: não houve estudo com pessoa usuária de leitor de tela nem avaliação completa de conformidade.

Também permaneceram abertas a leitura semântica de matemática, grafos densos, navegação em editores de código, anúncio de traces e seleção de texto com tecnologias assistivas.

## 10. Medições registradas

O `standalone.html` gerado pela rodada tinha 46.023 bytes na execução registrada e inicialização aproximada de 163,55 ms no walkthrough documentado. O Chromium reportou aproximadamente 3,27 MB de heap JavaScript usado e 5,85 MB de heap total naquele ponto da execução.

Em 500 ciclos de lifecycle por adapter no ambiente Node registrado, os arquivos-fonte individuais mediam de 4.333 a 9.195 bytes e as médias observadas ficaram aproximadamente entre 0,021 e 0,050 ms por ciclo.

Os deltas de heap dessa medição são ruidosos, incluindo valor negativo em uma família, e não representam pico de memória. O pacote não incluía runtimes externos, portanto esses números não predizem custo de motores simbólicos, editores especializados, bibliotecas de grafo, runtimes de outras linguagens ou execução protegida.

Nenhum desses valores é budget, SLA ou requisito de desempenho vigente.

## 11. Reprodutibilidade e limites do ambiente

O ambiente registrado incluía:

- Node.js 22.16.0 para os testes e medições Node;
- Python 3.13.5 para o walkthrough;
- Playwright para automação do navegador;
- Chromium 144.0.7559.96.

O pacote Node não declara dependências JavaScript externas e inclui `package-lock.json`. A versão do Playwright, entretanto, não foi registrada em arquivo de dependências próprio do pacote. Por isso, a rodada documenta um ambiente de reprodução, mas não encapsula integralmente todas as dependências do walkthrough de navegador.

O arquivo `standalone.html` não é preservado porque é gerado pelo script `scripts/build-standalone.mjs` a partir das fontes versionadas.

### Candidatos externos apenas registrados

O registro de risco e licenças da rodada catalogou alternativas para comparações posteriores sem empacotá-las nem executá-las. A fotografia histórica incluía:

- MathLive/MathJSON, revisão `d10bd8dd0f428b4d1c0b19293431cba8373566d6`, licença MIT, como candidato para entrada e renderização matemática;
- Cytoscape.js, revisão `c668509bf965340ebf2a46d1ab0dcb3b4dd6fb0e`, licença MIT, como candidato a motor e renderer de grafos;
- Pyodide, revisão `9048e6309c6b027351673f2fc1856a6969ba7a9b`, licença MPL-2.0, como candidato a runtime Python no navegador;
- Papyros, revisão `831b58227e63a84313b841dcd46992c747165289`, licença MIT, como candidato a execução e depuração de código;
- Recogito Text Annotator, revisão `092be72b5fc6d670123b8f918998fe9c424050a1`, licença BSD-3-Clause, como candidato a interface de anotação de fontes.

Os riscos registrados eram específicos da investigação: tamanho e cadeia de fornecimento e isolamento para Pyodide; requisitos de COOP/COEP, service worker e custo de pacotes para Papyros; acessibilidade, isolamento de geometria, seletores e integração canônica para os demais candidatos. Esses registros são temporais e não demonstram adequação atual, segurança, acessibilidade ou compatibilidade produtiva. Versões, licenças e condições técnicas precisariam ser revalidadas antes de qualquer decisão futura.

Nenhuma dessas alternativas foi selecionada nessa rodada.

## 12. Dez alterações contratuais propostas

A síntese histórica registrou dez alterações candidatas para uma iteração posterior do protótipo:

1. versão do adapter e versão de canonicalização;
2. garantia de isolamento e elegibilidade produtiva;
3. localização da validação;
4. política explícita para estado derivado;
5. representação de capacidade indisponível com proveniência;
6. política de re-resolução e ambiguidade de seletores;
7. alternativas de acessibilidade por operação;
8. perfil medido de tamanho, inicialização e memória;
9. visibilidade e retenção das evidências de validação;
10. limites separados de tempo, memória, saída e cancelamento.

Esses itens permanecem **propostas históricas**. Não são requisitos, schema, contratos ou decisões vigentes.

## 13. Relação com as pendências vigentes

A rodada fornece evidência para questões já abertas:

- `MODEL-003`: separação entre representação, prática, resposta, validação e retorno pedagógico;
- `EXP-008`: gramáticas de domínio e primitivas compartilhadas;
- `EXP-009`: governança de capacidades instaladas e alternativas para extensões fornecidas pelo conteúdo;
- `PED-004`: acessibilidade por operação e equivalência de interação;
- `INF-001`: factibilidade, custo, desempenho e fronteiras de execução;
- `VAL-001`: corpus de estados e falhas representativos;
- `VAL-002`: validade, satisfação de critérios, disponibilidade, autoridade e evidência;
- `SCOPE-005`: extensibilidade governada sem plataforma universal de componentes;
- `DEC-006` e `DEC-007`: continuidade funcional sem herança automática de arquitetura e manutenção do projeto em pré-desenvolvimento.

A rodada não resolve nenhuma dessas pendências por si só.

## 14. Não autorizações

Esta evidência não seleciona:

- lifecycle de produção;
- formato de resposta ou schema;
- Node.js, Python, Playwright ou Chromium como stack;
- Web Worker ou Node `vm` como sandbox;
- container, microVM ou runtime alternativo;
- motor matemático;
- biblioteca de grafo;
- editor de código;
- biblioteca de anotação;
- servidor, transporte ou provider;
- política de acessibilidade;
- política de evidências ou retenção;
- arquitetura ou implementação.

A contribuição preservada é delimitada: no protótipo registrado, uma fronteira estreita de adapter e uma resposta canônica sem estado visual ou de runtime mostraram-se representáveis em quatro famílias distintas, ao mesmo tempo em que os ensaios expuseram limites importantes de segurança, validade, acessibilidade e generalização.