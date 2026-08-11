# Evidências da rodada de adapters externos

**Categoria:** protótipo técnico, auditoria de fontes e evidência de interoperabilidade  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Esta evidência preserva uma rodada que examinou três bibliotecas externas candidatas atrás da fronteira experimental de componentes do ARA. A pergunta investigada não foi qual biblioteca deveria ser adotada, mas se estados com formas semelhantes às superfícies públicas dessas bibliotecas poderiam ser reduzidos a respostas canônicas sem incorporar estado transitório, geometria, stores internos ou detalhes de interface.

Os candidatos examinados foram:

- MathLive, com mapeamento orientado a MathJSON para entrada matemática;
- Cytoscape.js, para estado relacional e renderização de grafos;
- Recogito Text Annotator, para anotações textuais e seletores compatíveis com o modelo W3C.

O código, os fixtures, os relatórios e os testes da rodada estão preservados como [artefato de pesquisa](prototipos/adapters-externos-01/README.md). Nenhuma das três bibliotecas foi selecionada.

## 1. O que foi executado

Foram executados localmente somente os adapters de fronteira escritos para o experimento e os testes de substituição correspondentes.

O relatório registra **4 de 4 testes aprovados** em Node.js 22.16.0 sobre Linux x86_64. Os testes cobriram:

1. redução de estado orientado a MathLive para resposta matemática canônica;
2. redução de elementos orientados a Cytoscape para nós e arestas sem geometria de renderer;
3. conversão de seletores W3C orientados a Recogito para anotações canônicas;
4. substituição do adapter sem alteração dos documentos canônicos do lado do curso.

Esse resultado demonstra apenas que os wrappers experimentais preservaram as fronteiras testadas com fixtures controlados.

## 2. O que não foi executado

MathLive, Cytoscape.js e Recogito **não foram instalados, empacotados nem executados no navegador nesta rodada**.

O ambiente registrado não conseguiu resolver hosts externos para pacotes ou CDN, e o espelho disponível não fornecia os candidatos. Por isso ficaram sem execução:

- builds reais dos bundles candidatos;
- interação em navegador com as bibliotecas;
- medições de cold start, memória e tamanho dos bundles reais;
- testes com tecnologias assistivas sobre os componentes reais;
- avaliação de desempenho em dispositivos representativos.

A ausência dessas execuções é limitação do ambiente histórico, não falha das bibliotecas.

## 3. Auditoria de fontes oficiais

Na impossibilidade de executar os pacotes, a rodada auditou fontes oficiais fixadas em versões e commits do recorte temporal.

### MathLive

Foram registrados:

- package `mathlive` versão 0.110.0;
- licença MIT;
- superfícies de entrada matemática, valor em LaTeX e mapeamento semântico orientado a MathJSON.

A auditoria tratou MathLive apenas como candidato para **entrada e interpretação**. A biblioteca não recebeu autoridade implícita para prova matemática, correção ou avaliação educacional.

### Cytoscape.js

Foram registrados:

- commit auditado com versão 3.35.0-unstable;
- versão estável publicada observada no recorte: 3.34.0;
- licença MIT;
- modelo de elementos, renderer opcional e capacidades de grafo em modo headless;
- distribuição ESM observada com 305.180 bytes no arquivo auditado.

Esses valores são fotografia temporal do corpus e não devem ser usados como informação vigente sem revalidação. A rodada não selecionou versão estável nem biblioteca de grafo.

### Recogito Text Annotator

Foram registrados:

- package `@recogito/text-annotator` versão 4.2.5;
- licença BSD-3-Clause;
- anotações em formato W3C;
- `TextQuoteSelector` e `TextPositionSelector`.

O candidato foi tratado apenas como possível superfície de captura e intercâmbio de seletores. A qualidade de uma evidência ou argumento continua fora da autoridade do mecanismo de anotação.

## 4. MathLive e estado matemático

O fixture histórico continha LaTeX, MathJSON, texto falado, seleção, estado de teclado virtual e estado de menu.

O adapter experimental exportou somente:

- entrada original;
- expressão semântica canônica;
- prévia de interpretação.

Seleção, teclado virtual, menus e referências de interface ficaram fora da resposta canônica.

O mapeamento implementado cobriu apenas números, símbolos, adição, multiplicação, potência e divisão. Isso é um recorte experimental e não demonstra cobertura suficiente de matemática escolar, universitária ou simbólica geral.

## 5. Cytoscape.js e estado relacional

O fixture histórico incluiu nós e arestas acompanhados de posições, estilos, seleção, classes e scratch data.

O adapter experimental exportou somente o conteúdo semântico necessário ao cenário:

- IDs de nós;
- tipos e rótulos;
- dados de domínio opcionais;
- IDs e endpoints de arestas;
- direção, rótulos e dados de domínio opcionais.

Posições, estilos, classes, seleção, scratch data e dados de layout foram excluídos.

O teste confirmou também que uma geometria derivada pode ser reinjetada na importação sem fazer parte da resposta canônica. Isso sustenta a separação entre semântica e renderer, mas não aprova Cytoscape.js, o formato dos elementos nem a gramática relacional do ARA.

## 6. Recogito e anotações

O fixture histórico usou anotações W3C com corpos textuais e seletores de citação e posição.

O adapter experimental converteu esses dados em:

- identificador de anotação;
- identificador e digest da fonte;
- citação, prefixo, sufixo e offsets;
- finalidade;
- corpo textual;
- tags.

DOM ranges, geometria de highlight, estado do editor e store interno da biblioteca foram excluídos.

O mapeamento demonstra que seletores W3C podem ser representados atrás da fronteira experimental, mas não resolve reancoragem em documentos arbitrários, conflitos, edição concorrente, acessibilidade da seleção ou semântica completa de anotação.

## 7. Substituição sem alteração do curso

Um teste específico verificou que executar os três exports experimentais não alterava os documentos canônicos do lado do curso usados como base.

Esse resultado é relevante para a hipótese de adapters substituíveis: detalhes de biblioteca podem ficar fora do conteúdo canônico.

Ele não prova, entretanto:

- substituição transparente em produção;
- compatibilidade entre versões futuras das bibliotecas;
- migração sem perdas;
- igualdade de comportamento de interface;
- equivalência de acessibilidade;
- desempenho comparável;
- equivalência pedagógica.

## 8. Versões e licenças são evidência temporal

O pacote registra versões, licenças e commits oficiais observados no dia do ensaio. Esses registros são úteis para procedência e reprodutibilidade histórica.

Eles não constituem recomendação de dependência. Antes de qualquer futura seleção, precisam ser revalidados quanto a:

- versão estável vigente;
- manutenção;
- licença e compatibilidade com o projeto;
- API pública;
- tamanho e dependências;
- segurança;
- acessibilidade;
- comportamento offline;
- suporte a localização;
- desempenho;
- custo de substituição e portabilidade.

## 9. Limite do rótulo `ARA_decision`

O relatório estruturado histórico contém campos chamados `ARA_decision`. Esse nome pertence ao vocabulário da rodada e **não representa decisão canônica vigente do projeto**.

As formulações `source-compatible candidate` devem ser lidas como avaliações históricas de compatibilidade em nível de fonte e boundary. A única fonte de decisões aprovadas é `DECISOES.md`.

Nenhum candidato deste lote está aprovado.

## 10. Relação com a rodada de adapters descartáveis

A rodada anterior demonstrou com adapters próprios que uma fronteira canônica estreita era representável em quatro famílias. Esta rodada tentou confrontar a mesma ideia com estados inspirados em bibliotecas externas.

O avanço é limitado:

- os wrappers conseguiram remover estado específico das bibliotecas nos fixtures;
- os documentos canônicos usados nos testes permaneceram independentes;
- fontes oficiais mostraram superfícies plausíveis para integração.

A lacuna principal permaneceu aberta porque os runtimes externos não foram executados.

Por isso, o pacote não supera nem substitui a necessidade de um bake-off real e reproduzível.

## 11. Relação com as pendências vigentes

A evidência se relaciona principalmente a:

- `MODEL-003`: separação entre representação, prática, resposta, validação e retorno pedagógico;
- `EXP-007`: sistemas e bibliotecas externas como precedentes, não requisitos;
- `EXP-008`: gramáticas específicas de domínio e primitivas compartilhadas;
- `EXP-009`: capacidades instaladas, isolamento e governança de extensões;
- `PED-004`: acessibilidade estrutural e equivalência de interação;
- `INF-001`: factibilidade, tamanho, custo, desempenho e portabilidade;
- `VAL-001`: casos representativos e falhas;
- `VAL-002`: distinção entre validade, satisfação de critérios, disponibilidade, autoridade e evidência;
- `SCOPE-005`: extensibilidade governada sem universalização prematura;
- `DEC-006` e `DEC-007`: continuidade funcional sem herança automática de arquitetura e manutenção do projeto em pré-desenvolvimento.

Nenhuma nova decisão é necessária para preservar esta evidência.

## 12. Próxima validação necessária

Uma futura comparação real entre bibliotecas deve manter a fronteira canônica estável durante o ensaio e executar versões estáveis fixadas em ambiente reproduzível com rede e dependências controladas.

A comparação deveria medir, conforme cada candidato:

- fidelidade de importação e exportação;
- comportamento de interação;
- teclado e tecnologias assistivas;
- reflow e dispositivos móveis;
- tamanho de bundle e inicialização;
- consumo de memória;
- funcionamento offline;
- tratamento de erros e indisponibilidade;
- impacto da licença e dependências;
- custo de substituição;
- adequação à gramática educacional específica.

Esses são critérios de investigação, não critérios de aceite aprovados.

## 13. Não autorizações

Esta evidência não seleciona:

- MathLive;
- MathJSON como semântica interna definitiva;
- Cytoscape.js;
- Recogito Text Annotator;
- versões específicas dessas bibliotecas;
- Node.js ou npm como stack;
- package manager;
- API de adapter;
- lifecycle de produção;
- schema ou formato de resposta;
- renderer;
- runtime;
- modelo de anotação definitivo;
- política de acessibilidade;
- arquitetura ou implementação.

A contribuição preservada é mais restrita: no ensaio documentado, wrappers controlados conseguiram projetar estados com forma semelhante aos três candidatos em dados canônicos sem carregar detalhes transitórios das bibliotecas, enquanto a impossibilidade de executar os pacotes reais deixou em aberto toda conclusão de runtime, acessibilidade, desempenho e adequação produtiva.