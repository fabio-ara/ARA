# Artefatos de interface do ARA

Este diretório preserva artefatos visuais com estados de autoridade distintos. A existência de um artefato exploratório não o transforma em requisito, decisão ou contrato de implementação.

## Composição desktop aprovada

[`composicao-desktop-aprovada.svg`](composicao-desktop-aprovada.svg) materializa somente a composição definida por `DEC-003` e `DEC-004`:

- painel esquerdo com pastas e cursos visíveis ao usuário;
- área principal com o grafo de revisões do curso selecionado;
- cada nó do grafo representa uma revisão completa e utilizável do curso;
- níveis internos permanecem fora do grafo principal.

O esquema não define estilo visual final, biblioteca de grafos, algoritmo de layout, painel contextual, interações detalhadas, permissões, comportamento móvel ou recorte de implementação.

## Explorações não normativas

A pasta [`exploracoes-nao-normativas/`](exploracoes-nao-normativas/) preserva doze wireframes usados para explorar biblioteca, estudo, composição, parâmetros, autoria, revisão, diferenças entre versões, assistência, pesquisa, funcionamento offline e administração.

Esses wireframes são evidência do espaço de desenho. Elementos como navegação completa, rótulos de áreas, perfis, operações MCP, fluxos de pesquisa, telas administrativas, valores de configuração e escolhas visuais permanecem candidatos ou podem ter sido substituídos por decisões posteriores. O grafo de dependências mostrado em uma das explorações é uma representação interna auxiliar e não substitui o grafo principal de revisões de curso definido por `DEC-004`.

## Protótipo estrutural não normativo

A pasta [`prototipo-estrutural-nao-normativo/`](prototipo-estrutural-nao-normativo/) preserva uma demonstração estática de estrutura, navegação responsiva e estados de interface. Ela não representa uma especificação vigente, não autoriza implementação e não estabelece o conjunto final de telas ou destinos de navegação.

As questões ainda abertas de arquitetura de informação, estados transversais e acessibilidade permanecem registradas em `UX-002`, `UX-003` e `UX-004` no backlog canônico.
