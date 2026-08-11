# Adapters externos do ARA - rodada 01

**Estado:** artefato histórico de pesquisa, não produtivo

Este diretório preserva uma rodada de auditoria e testes de fronteira com três bibliotecas externas candidatas:

- MathLive, com mapeamento orientado a MathJSON;
- Cytoscape.js;
- Recogito Text Annotator.

As bibliotecas externas não foram instaladas nem executadas nesta rodada. O que foi executado foram adapters escritos para o experimento e testes com fixtures que reproduzem formas de estado compatíveis com as superfícies auditadas.

Por isso, o artefato não demonstra compatibilidade real de runtime, acessibilidade, desempenho ou adequação produtiva das bibliotecas.

## O que foi executado

```bash
npm test
```

O relatório registra quatro testes aprovados:

1. export de estado orientado a MathLive para resposta matemática canônica;
2. export de elementos orientados a Cytoscape sem geometria ou estado de renderer;
3. export de anotações orientadas a Recogito com seletores W3C e sem estado de DOM;
4. substituição dos adapters sem alteração dos documentos canônicos usados do lado do curso.

## Limitação do ambiente

O ambiente histórico não conseguiu resolver hosts externos de pacotes ou CDN, e seu espelho não fornecia os três candidatos. Permaneceram sem execução:

- bundles reais;
- walkthroughs de interação das bibliotecas;
- medições de inicialização, heap e tamanho real;
- testes com tecnologias assistivas;
- avaliação em dispositivos representativos.

Essa limitação não constitui resultado negativo sobre as bibliotecas.

## Fontes e versões observadas

A auditoria de fontes oficiais registrou, no recorte temporal do ensaio:

- MathLive 0.110.0, licença MIT;
- Cytoscape.js em commit com versão 3.35.0-unstable e versão estável publicada observada 3.34.0, licença MIT;
- `@recogito/text-annotator` 4.2.5, licença BSD-3-Clause.

Essas versões e metadados são evidência temporal. Devem ser revalidados antes de qualquer futura seleção.

## Autoridade dos relatórios

O arquivo `reports/source-audit.json` contém campos históricos chamados `ARA_decision`. Esses campos registram a avaliação daquela rodada e **não são decisões canônicas vigentes**. A autoridade atual de decisões permanece exclusivamente em `DECISOES.md`.

Expressões como `source-compatible candidate` significam somente que a superfície auditada parecia compatível com o boundary ensaiado. Não significam biblioteca aprovada, executada, selecionada ou pronta para produção.

## Fronteira testada

Os adapters tentam manter estado transitório de bibliotecas fora dos documentos canônicos:

- seleção, teclado virtual e menus ficam fora da resposta matemática;
- posições, estilos, classes, seleção e scratch data ficam fora da resposta relacional;
- DOM ranges, geometria de highlight, estado de editor e stores internos ficam fora da anotação canônica.

Os campos e funções deste protótipo não constituem schema, API ou lifecycle aprovados.

## Não autorizações

Este artefato não seleciona:

- MathLive;
- MathJSON como semântica interna definitiva;
- Cytoscape.js;
- Recogito Text Annotator;
- versões específicas;
- Node.js ou npm como stack;
- package manager;
- adapter API;
- renderer;
- runtime;
- schema;
- arquitetura;
- implementação.

A síntese interpretativa da rodada está em `../../adapters-externos-2026-08.md`.