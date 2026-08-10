# Evidências da investigação sobre taxonomia de configuração

**Categoria:** evidência de pesquisa e análise de configuração  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva resultados relevantes de uma investigação integrada sobre como o ARA poderia representar variações pedagógicas, de acessibilidade, autoria, governança, pesquisa e assistência por inteligência artificial sem reduzir a configuração a um conjunto plano de opções.

O material é evidência de concepção. Ele não aprova identificadores, namespaces, valores, perfis, defaults, ordem de precedência, schema, interface, mecanismo adaptativo, arquitetura ou implementação. As pendências vigentes relacionadas à parametrização estão registradas em `PARAM-001` e `PARAM-002` no [`BACKLOG.yaml`](../../BACKLOG.yaml).

## 1. Escopo e cobertura histórica

A integração examinada reuniu 205 dimensões candidatas de configuração, organizadas originalmente em cinco frentes temáticas. O processo também registrou:

- 205 registros integrados, sem duplicação literal de identificadores;
- 18 aliases usados apenas para desambiguar namespaces históricos;
- 43 ocorrências de perfis, consolidadas em 38 perfis históricos;
- 36 candidatos adiados;
- 41 princípios rejeitados ou não recomendados no recorte analisado;
- 15 cenários de coerência conceitual.

Essas quantidades descrevem o recorte histórico. Não constituem catálogo aprovado nem obrigação de representar todas as dimensões no produto.

## 2. Separação entre tipos de efeito

A investigação propôs distinguir seis camadas de incidência. Essa decomposição permanece hipótese útil para `PARAM-001` e `PARAM-002`, não contrato de domínio.

| Camada analítica | Problema que procura separar |
|---|---|
| Configuração efetiva em tempo de uso | comportamento de estudo, avaliação, retorno, ritmo, revisão, acessibilidade e assistência sem exigir necessariamente alteração do conteúdo autoral |
| Materialização de conteúdo | alterações que modificam teoria, prática, exemplos, segmentação, apoio, tradução, adaptação, geração ou reparo de conteúdo |
| Composição e dependências | ordem, pré-requisitos, relações, reutilização, ramificação, posicionamento e composição entre unidades e cursos |
| Ciclo de vida e governança | autoria, revisão, reparo, versionamento, publicação, acesso, licenciamento, retenção, retirada e papéis |
| Condição de pesquisa | protocolo, condição, instrumentos, eventos autorizados, medidas, construtos, análise, proveniência e interpretação |
| Direitos e acessibilidade | restrições e acomodações transversais que podem limitar ou modificar escolhas das demais camadas |

Uma consequência analítica importante é que uma alteração de configuração pode ter efeitos diferentes conforme a camada. Uma mudança de runtime não é automaticamente uma nova redação do conteúdo; uma transformação de conteúdo não deve ser tratada apenas como opção de renderização; uma alteração de composição pode exigir uma nova versão da composição mesmo sem modificar as unidades referenciadas.

## 3. Maturidade e autoridade dos parâmetros

O levantamento tratou descoberta, definição conceitual, evidência, candidatura, recomendação e aprovação como estados diferentes. Essa separação é compatível com o método canônico atual, mas os estados históricos e seus rótulos não possuem autoridade decisória própria.

Para investigação futura, um parâmetro candidato pode precisar registrar, conforme a relevância:

- finalidade e definição;
- escopo de aplicação;
- relação com a configuração funcional de referência;
- alternativas ou intervalos possíveis;
- fontes e estado da evidência;
- autoridade capaz de definir ou alterar o valor;
- dependências e incompatibilidades;
- riscos e interpretações proibidas;
- efeitos sobre acessibilidade, privacidade, funcionamento offline e pesquisa;
- situação decisória explícita.

O levantamento também reforça que a referência funcional anterior é um perfil de contraste, não limite da taxonomia nem default universal.

## 4. Perfis e sobreposições

Os 38 perfis históricos foram organizados em dez famílias analíticas:

1. assistência por inteligência artificial;
2. acessibilidade e direitos;
3. autoria, publicação e governança;
4. ensino formal e avaliação;
5. contexto institucional confidencial;
6. funcionamento offline e uso móvel;
7. perfil funcional de referência;
8. condições de pesquisa;
9. aprendizagem autodirigida;
10. apoio segundo experiência e necessidade de suporte.

A regra histórica de composição propunha um perfil-base versionado, zero ou mais sobreposições compatíveis e exceções esparsas por escopo. Como restrições candidatas, o levantamento registrou que:

- uma sobreposição não deveria remover direitos ou requisitos de acessibilidade;
- um bloqueio de pesquisa deveria afetar somente dimensões declaradas;
- política institucional não deveria se propagar automaticamente para um espaço pessoal;
- perfis relacionados a capacidades ou funcionamento offline deveriam tornar indisponibilidade e fallback explícitos;
- aplicar um perfil deveria produzir uma diferença inspecionável e um snapshot efetivo;
- conflitos não deveriam ser resolvidos por ordem implícita de carregamento.

Nenhuma dessas regras, nem qualquer dos 38 perfis, está aprovada como modelo vigente.

## 5. Precedência e configuração efetiva

A investigação comparou uma resolução em camadas na qual direitos, consentimento, protocolos de pesquisa, políticas institucionais, revisão qualificada, políticas de curso, escolha do estudante, perfis, adaptação, assistência por IA e disponibilidade técnica podem entrar em conflito.

O resultado histórico ordenava onze níveis. A consolidação atual não adota essa ordem. Preserva apenas os problemas que precisam ser resolvidos antes de uma decisão:

- distinguir autoridade normativa de disponibilidade técnica;
- tornar bloqueios e exceções explícitos;
- registrar origem, escopo e autoridade de valores efetivos;
- não permitir que assistência por IA adquira autoridade apenas por produzir uma recomendação;
- não degradar silenciosamente uma condição quando uma capacidade estiver indisponível;
- produzir um estado efetivo reproduzível, com conflitos e combinações não suportadas visíveis.

O modelo de snapshot investigado incluía perfil-base, sobreposições, valores efetivos com origem e escopo, bloqueios, exceções, políticas institucionais, referências a acomodações, capacidades disponíveis, versões de conteúdo e composição, instrumentos autorizados, proveniência, avisos e estado de resolução. Esse conjunto é referência analítica, não schema aprovado.

## 6. Candidatos adiados

Foram consolidados 36 candidatos adiados. As principais famílias foram:

- modelos de estudante, estimadores de domínio, schedulers e ramificação adaptativa;
- detecção automática de dificuldade, expertise, emoção ou neurotipo;
- personalização generativa em tempo de uso;
- pontuação autoritativa de respostas abertas por IA;
- geração automática de acomodações;
- inferência causal automatizada e transferência automática de domínio entre cursos;
- coleta de participantes sem protocolo futuro aprovado;
- schema de eventos, catálogo de métricas, early warning e dashboard universal;
- verificação automática de fontes e compatibilidade de licenças;
- reparo entre cursos, propagação automática e merge semântico;
- mecanismos técnicos de proveniência ou credenciais ainda sem necessidade demonstrada;
- marketplace e reputação pública;
- armazenamento endereçado por conteúdo e outros mecanismos físicos dependentes de decisões de infraestrutura.

O adiamento histórico não equivale a rejeição permanente. Cada tema deve permanecer no domínio canônico pertinente e ser reavaliado somente quando houver decisão, evidência ou dependência que justifique retomá-lo.

## 7. Princípios rejeitados ou não recomendados no levantamento

O recorte consolidou 41 princípios rejeitados ou não recomendados. Entre os mais recorrentes estavam:

- configuração monolítica que colapsa dimensões independentes;
- defaults universais para tentativas, revelação, feedback, domínio, espaçamento, intercalação ou controle do estudante;
- inferir aprendizagem, esforço, atenção, dificuldade, motivação ou expertise diretamente de rastros brutos de interação;
- ranking público como padrão;
- usar IA probabilística como autoridade final de pontuação, aprovação ou publicação;
- adaptação invisível sem alvo, razão, registro de estado, reversão e contestação;
- acessibilidade tratada como opção desativável ou condicionada a exposição pública desnecessária;
- coleta de todos os eventos tecnicamente disponíveis;
- um único dashboard e uma única política de visibilidade para todos os papéis;
- retenção identificável indefinida para finalidades não especificadas;
- reutilizar logs operacionais como dados educacionais sem finalidade e autorização;
- mutação silenciosa de artefatos publicados ou ligados a pesquisa e propagação automática para consumidores;
- tags livres como único mecanismo de dependência, proveniência ou anotação;
- exclusão rígida sem análise de referências, retenção e impacto;
- uma única licença de pacote ocultando materiais de terceiros incompatíveis ou excluídos;
- um único papel de superadministrador global;
- conceitos de banco e armazenamento como vocabulário principal para usuários não técnicos.

Essas rejeições históricas são evidência de análise. Elas não criam, por si só, decisões públicas adicionais. Quando coincidem com decisões ou pendências vigentes, a autoridade vem das fontes canônicas correspondentes.

## 8. Cenários de coerência conceitual

Quinze cenários foram usados para testar se o modelo histórico conseguia tornar conflitos e efeitos explícitos. O estado registrado como aprovado nos artefatos de origem significa apenas que o cenário encontrou uma resolução conceitualmente coerente no modelo analisado.

| Cenário | Questão examinada |
|---|---|
| Estudo pessoal offline no perfil funcional de referência | funcionamento sem IA ou instrumentação de pesquisa e persistência apenas do estado funcional necessário |
| Estudo reflexivo com analytics opcionais | opt-in em escopo pessoal sem inferir compartilhamento institucional ou de pesquisa |
| Curso formal formativo | política autoral combinada com escolhas do estudante dentro de limites explícitos |
| Curso com critério de domínio e pré-requisitos flexíveis | separação entre conclusão estrutural, evidência de domínio, remediação, exceção e rechecagem |
| Avaliação somativa institucional | consequências explícitas, acessibilidade, contestação e autoridade de avaliação |
| Estudo entre participantes com variantes de curso | bloqueios de condição, diferenças de conteúdo/configuração/composição e proveniência |
| Estudo intraparticipante em ordens diferentes | versionamento de assignment, sequência, instrumentos e plano de análise |
| Acomodação em conflito com condição de pesquisa | precedência de direitos e documentação do impacto sobre construto e comparabilidade |
| Autoria assistida e reparo situado | alvo explícito, nova revisão para reparo semântico, separação entre auditoria e reparo e publicação humana |
| Atualização de unidade reutilizada | ausência de propagação silenciosa e necessidade de impacto, diferença e escolha explícita do consumidor |
| Publicação de recurso educacional aberto | licenciamento e atribuição por escopo e bloqueio diante de incompatibilidade não resolvida |
| Autoria institucional confidencial | autorização de contexto independente de memória de chat ou conveniência técnica |
| Capacidade conectada indisponível durante uso offline | estado indisponível ou fallback previamente autorizado, sem substituição silenciosa |
| Retirada, exclusão e retenção de pesquisa | resolução separada de direitos do participante, ciclo de vida do conteúdo e retenção autorizada |
| Publicação institucional com separação de deveres | auditoria por IA insuficiente para substituir revisões qualificadas exigidas |

Esses cenários não constituem critérios de aceite atuais. Eles são candidatos úteis para futuros testes de `PARAM-001`, `PARAM-002`, `VAL-001` e `VAL-002` e para os domínios de dados, autoria, acesso, publicação e funcionamento offline.

## 9. Limitações

A auditoria histórica do pacote verificou consistência interna, contagens, preservação dos registros de origem, desambiguação de namespaces, composição de perfis e cobertura dos quinze cenários. Isso não demonstrou:

- efetividade educacional;
- usabilidade ou compreensão por usuários;
- conformidade de acessibilidade com participantes e tecnologias assistivas;
- factibilidade técnica;
- desempenho, segurança ou confiabilidade de uma implementação;
- validade de instrumentos e medidas específicos;
- adequação de qualquer ordem de precedência ao produto final.

Também não houve autorização para schema, banco de dados, armazenamento, IndexedDB, MCP, interface, event store, analytics implementados, coleta de participantes, modelo adaptativo, scheduler, arquitetura, stack, código ou migração.

## 10. Destino atual

Na orientação vigente:

- `PARAM-001` mantém aberta a definição da taxonomia, maturidade e governança de parâmetros;
- `PARAM-002` mantém aberta a definição de perfis, sobreposições, precedência e configuração efetiva reproduzível;
- parâmetros pedagógicos permanecem nas pendências `PED-*`;
- autoria, revisão, reparo e publicação permanecem em `AUTH-*`, `CUR-*` e `PUB-001`;
- acesso permanece em `ACCESS-001` e `ACCESS-002`;
- dados, instrumentação e pesquisa devem ser consolidados no domínio próprio;
- estrutura de conteúdo e composição permanece subordinada às decisões `MODEL-001` a `MODEL-005` ainda pendentes de aprovação;
- infraestrutura, funcionamento offline e mecanismos físicos permanecem sem seleção técnica.
