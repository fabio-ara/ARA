# Triagem bibliográfica da primeira rodada formal

**Categoria:** levantamento bibliográfico, deduplicação, triagem e evidência de execução  
**Recorte temporal:** 2 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva a etapa de deduplicação e primeira triagem por título e resumo do corpus recuperado na rodada formal PubMed-ERIC. Ele complementa os registros públicos de metodologia e de execução das buscas iniciais.

A rodada não constitui uma revisão sistemática concluída, não estabelece inclusão final e não transforma relevância preliminar em qualidade da evidência. Seu papel é registrar de forma verificável como 1.555 registros brutos foram convertidos em 1.471 publicações bibliográficas únicas e como esse conjunto recebeu uma primeira classificação de relevância para recuperação e análise posteriores.

## 1. Unidade de deduplicação

A deduplicação foi realizada no nível de **publicação bibliográfica**.

Isso significa que dois registros foram removidos somente quando representavam a mesma publicação. Publicações distintas relacionadas ao mesmo estudo, experimento ou conjunto de participantes foram preservadas separadamente quando havia justificativa bibliográfica.

Essa regra evita confundir:

- registro em uma base;
- publicação;
- versão de publicação;
- família de estudo;
- experimento ou amostra;
- decisão de triagem.

A vinculação de publicações pertencentes à mesma família de estudo é uma etapa analítica distinta da deduplicação bibliográfica.

## 2. Validação dos arquivos recebidos

A primeira rodada formal reuniu:

- PubMed ESearch com **827 resultados** e **827 PMIDs únicos**;
- exportação bibliográfica PubMed com **827 registros**, correspondendo ao mesmo conjunto de PMIDs;
- quatro lotes ERIC com **200 + 200 + 200 + 128 registros**, totalizando **728**;
- ausência de sobreposição entre os identificadores dos quatro lotes ERIC.

Os arquivos recebidos foram conferidos antes das etapas de deduplicação e triagem. Digests e tamanhos foram usados operacionalmente para verificar integridade, mas não são reproduzidos aqui porque não acrescentam conteúdo intelectual à história pública.

## 3. Deduplicação interna

### PubMed

Não foram identificadas duplicações internas por PMID. Permaneceram **827 publicações**.

### ERIC

Foram identificadas duas duplicações bibliográficas exatas. Nos dois casos, um registro de submissão ou versão depositada correspondia à mesma publicação de periódico, com identidade de título, autoria, DOI, ano e publicação.

Resultado:

- 728 registros ERIC brutos;
- 2 publicações duplicadas removidas;
- **726 publicações ERIC** após deduplicação interna.

Um trabalho apresentado em evento em 1987 e um artigo de periódico de 1988 sobre o mesmo estudo foram deliberadamente mantidos como publicações distintas e vinculados como uma mesma família de estudo.

## 4. Deduplicação entre PubMed e ERIC

A comparação entre bases adotou a seguinte ordem:

1. DOI normalizado exato;
2. título normalizado exato e mesmo ano quando não havia DOI compartilhado;
3. revisão manual de candidatos semelhantes, sem remoção por mera similaridade.

Foram identificadas:

- **81** correspondências exatas por DOI;
- **1** correspondência exata por título e ano sem DOI compartilhado;
- **82** publicações duplicadas entre PubMed e ERIC.

Para essas duplicações, o registro PubMed foi usado como registro canônico na rodada e o identificador ERIC foi preservado como identificador alternativo.

Nenhum candidato adicional foi removido apenas por alta similaridade de título.

## 5. Corpus bibliográfico após deduplicação

| Etapa | Publicações |
|---|---:|
| PubMed bruto | 827 |
| ERIC bruto | 728 |
| Total bruto | 1.555 |
| Após deduplicação interna | 1.553 |
| Duplicações entre bases | 82 |
| **Corpus bibliográfico único** | **1.471** |

A composição final foi:

- **827** registros canônicos PubMed;
- **644** registros exclusivos do ERIC.

O total de 1.471 representa publicações bibliográficas únicas. Não representa 1.471 estudos independentes, experimentos, amostras nem fontes posteriormente incluídas após avaliação em texto completo.

## 6. Publicações relacionadas preservadas

O processo registrou explicitamente situações em que publicações relacionadas não deveriam ser removidas como duplicatas. Quatro pares foram documentados como exemplos concretos:

- trabalho de evento e artigo posterior sobre o mesmo estudo;
- preprint e artigo de periódico posterior com publicação distinta;
- estudo primário e avaliação externa daquele estudo;
- artigo original e aviso de correção.

Esses casos reforçam que deduplicação e identificação de famílias de estudo são responsabilidades diferentes. Uma publicação relacionada pode precisar ser vinculada a outra durante a extração sem desaparecer do corpus bibliográfico.

## 7. Primeira triagem por título e resumo

A primeira triagem foi descrita como:

> primeira passagem por título e resumo, realizada por uma pessoa, assistida por regras determinísticas e auditoria manual

O conjunto completo de **1.471 publicações** recebeu uma das três decisões preliminares:

| Decisão | Publicações | Interpretação |
|---|---:|---|
| `include` | **732** | relevância suficiente para recuperação ou revisão posterior |
| `maybe` | **504** | pertinência incerta ou dependente de avaliação adicional |
| `exclude` | **235** | fora do recorte desta rodada segundo a informação disponível |
| **Total** | **1.471** | corpus deduplicado completo |

`include` não significa inclusão final em uma revisão. `maybe` não significa evidência fraca. Essas categorias expressam somente a relevância preliminar para etapas posteriores.

## 8. Priorização operacional da triagem

A rodada também agrupou as publicações em níveis de prioridade para organizar recuperação e análise:

| Nível histórico | Publicações | Função |
|---|---:|---|
| A - síntese | **26** | sínteses e fontes de alta prioridade para mapeamento do campo |
| B - aplicação direta | **425** | estudos ou aplicações diretamente relacionados ao recorte |
| C - mecanismo direto | **281** | estudos de mecanismos de aprendizagem diretamente relacionados |
| D - limítrofe | **504** | casos que exigem avaliação adicional |
| sem prioridade | **235** | publicações excluídas nesta primeira passagem |

Os níveis são prioridade de trabalho, não escala de qualidade metodológica nem força de evidência.

## 9. Distribuição por base

A classificação final após a primeira triagem foi:

| Base no corpus deduplicado | `include` | `maybe` | `exclude` | Total |
|---|---:|---:|---:|---:|
| PubMed | 410 | 293 | 124 | 827 |
| ERIC exclusivo | 322 | 211 | 111 | 644 |
| **Total** | **732** | **504** | **235** | **1.471** |

Essa tabela usa os 644 registros exclusivos do ERIC após a deduplicação entre bases, e não os 728 registros ERIC brutos.

## 10. Razões de triagem

As decisões foram acompanhadas por razões estruturadas. Entre as exclusões, as categorias mais frequentes incluíram:

- termo incidental ou tópico fora do recorte;
- intervenção clínica ou de reabilitação sem finalidade educacional pertinente;
- neurociência básica, memória motora ou mecanismo biológico fora da pergunta educacional;
- metodologia de recuperação da informação ou busca sem relação com o mecanismo investigado;
- recurso genérico sem contribuição substantiva para a pergunta.

Entre as inclusões, as categorias principais distinguiram:

- aplicação ou revisão diretamente relacionada;
- estudo de mecanismo de aprendizagem diretamente relacionado;
- mecanismo central explicitamente identificado no resumo;
- revisão com relevância direta.

Os casos `maybe` preservaram principalmente intervenções educacionais relacionadas, menções precoces ao mecanismo, contextos clínicos adjacentes, mecanismos cognitivos básicos, recuperação induzida de esquecimento e fontes de contexto sobre retenção.

A classificação por razão serve para auditoria e recuperação. Ela não substitui a leitura crítica da fonte.

## 11. Auditoria manual

Foi realizada auditoria manual estratificada de **90 registros**, com **15 registros por base e por estado inicial**.

Resultados registrados:

- 80 decisões mantidas;
- 10 decisões alteradas dentro da amostra auditada;
- **14 overrides manuais** registrados no conjunto da triagem.

Os overrides demonstram que as regras determinísticas eram auxiliares, não autoridade final. Houve correções em diferentes direções:

- casos inicialmente classificados como `maybe` foram promovidos a `include` quando o mecanismo-alvo era central;
- outros `maybe` foram excluídos quando a relação era apenas incidental ou o domínio estava fora do recorte;
- alguns casos inicialmente excluídos foram reabertos como `maybe` por relevância para mecanismos de retenção ou esquecimento.

O registro não atribui os quatro overrides adicionais à amostra de 90 e, portanto, nenhuma explicação adicional é inferida aqui.

## 12. Resumos ausentes ou insuficientes

Foram registrados **18 casos com resumo ausente ou reduzido**.

Essa limitação impede tratar a primeira triagem como decisão definitiva. Fontes sem informação suficiente podem exigir recuperação de texto completo, verificação bibliográfica adicional ou decisão posterior baseada em informação mais completa.

## 13. O que esta etapa demonstra

A rodada demonstra que:

- os resultados oficiais das duas bases foram conferidos antes da deduplicação;
- a deduplicação foi determinística no nível de publicação e não apagou automaticamente versões ou publicações relacionadas;
- o corpus deduplicado contém 1.471 publicações;
- toda publicação recebeu uma decisão de primeira passagem por título e resumo;
- a triagem foi assistida por regras, mas corrigida por auditoria humana;
- razões de decisão foram preservadas;
- há uma estrutura explícita para priorizar recuperação e análise posteriores.

Ela não demonstra que:

- 732 publicações serão incluídas em uma revisão final;
- 504 casos `maybe` possuem menor qualidade metodológica;
- 235 exclusões permanecerão necessariamente excluídas sob outra pergunta de pesquisa;
- a triagem seja equivalente a dupla revisão independente;
- as 1.471 publicações representem 1.471 estudos independentes;
- a primeira rodada cubra toda a literatura relevante;
- a evidência recuperada demonstre efetividade de qualquer mecanismo ou produto.

## 14. Relação com o programa de pesquisa

Esta evidência confirma que o levantamento bibliográfico já possui, para pelo menos uma rodada formal:

- pergunta e estratégia de busca documentadas;
- resultados oficiais preservados;
- deduplicação interna e entre bases;
- registro de publicações relacionadas;
- corpus bibliográfico único;
- primeira triagem por título e resumo;
- razões estruturadas;
- auditoria manual e overrides;
- níveis de prioridade para recuperação posterior.

O trabalho acadêmico restante não deve reiniciar essas etapas. Ele precisa auditar e consolidar bibliografias, famílias de estudo, textos recuperados, extrações, sínteses e lacunas, além de definir protocolos futuros adequados às perguntas concretas.

A organização por procedência e estabilidade temporal continua necessária: registros bibliográficos, literatura acadêmica, documentação oficial, normas, informações comerciais e observações de sistemas não possuem a mesma autoridade nem a mesma estabilidade.

## 15. Não autorizações

Este documento não:

- encerra o programa de levantamento bibliográfico;
- transforma a primeira rodada em revisão sistemática concluída;
- declara inclusão final de qualquer publicação;
- aprova uma ferramenta de triagem ou um classificador automático;
- aprova dupla triagem quando ela não ocorreu;
- estabelece um protocolo universal de deduplicação ou seleção;
- declara completude da literatura;
- converte relevância bibliográfica em evidência de efetividade;
- cria requisito, decisão de produto ou autorização de implementação.

A contribuição preservada é a evidência de execução da primeira triagem e a distinção explícita entre registros, publicações, famílias de estudo, relevância preliminar e inclusão acadêmica final.
