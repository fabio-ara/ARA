# Adapters descartáveis do ARA - rodada 01

**Estado:** artefato histórico de pesquisa, não produtivo

Este diretório preserva quatro adapters de referência usados para testar uma fronteira estreita entre estado canônico, interação, validação e detalhes descartáveis de renderer ou runtime.

Os adapters não são componentes de produção, não selecionam a stack final e não constituem contratos aprovados do ARA.

## Famílias

- `semantic-mathematics`: entrada infix, prévia de interpretação, validade e critérios de propriedade;
- `relational-construction`: estado semântico de nós e arestas, histórico de operações, layout SVG derivado e alternativa linear sem arraste;
- `executable-programming`: resposta JavaScript, testes públicos no navegador e testes protegidos injetados pelo host no ensaio Node;
- `source-argument`: fonte por digest, seletor re-resolúvel, vínculo de evidência e passagem para revisão humana.

## Lifecycle ensaiado

```text
load(instance)
start()
importResponse(response)
exportResponse()
validate(options)
produceFeedback(validation)
dispose()
```

`exportResponse()` é a fronteira canônica experimental desta rodada. Geometria, layout, estado interno de workers e testes protegidos ficam fora da resposta exportada.

## Ambiente registrado

A execução histórica registrou:

- Node.js 22.16.0;
- Python 3.13.5 com Playwright;
- Chromium 144.0.7559.96.

O pacote Node não possui dependências JavaScript externas. A versão de Playwright não foi fixada em arquivo de dependências deste artefato, portanto a reprodução do walkthrough de navegador depende de um ambiente externo compatível.

## Reprodução

```bash
npm test
node scripts/build-standalone.mjs
python tests/browser_walkthrough.py
npm run measure
```

`standalone.html` é gerado localmente pelo script e não é preservado como fonte independente.

## Resultados registrados

- testes Node: 6 de 6 aprovados;
- walkthrough Chromium: 15 de 15 verificações aprovadas;
- inspeção da árvore de acessibilidade: controles nomeados, regiões de status e hierarquia de headings presentes;
- demonstração standalone: 46.023 bytes na execução registrada, sem solicitações externas de rede.

Esses resultados descrevem somente os ensaios executados. Não constituem validação do produto, conformidade de acessibilidade, segurança de produção, efetividade educacional ou garantia de desempenho.

## Limites de segurança

O JavaScript Worker e o uso de Node `vm` demonstram lifecycle, timeout, limite de saída e separação de testes protegidos. Nenhum dos dois é tratado como sandbox produtiva contra código hostil.

Remover APIs de rede do Worker não cria, por si só, uma fronteira de segurança. Uma arquitetura futura de execução protegida precisará de threat model, isolamento, limites de recursos, tratamento de rede e filesystem, reprodutibilidade e evidência diagnóstica próprios.

## Limites de acessibilidade

A rodada exercitou navegação por teclado, foco, regiões `aria-live`, alternativa linear ao grafo e reflow em 320 CSS pixels. Não houve estudo com usuários de tecnologias assistivas nem avaliação completa de conformidade.

## Licenciamento

O código deste artefato segue `AGPL-3.0-or-later`. A documentação original do projeto segue o regime indicado para documentação no repositório público, salvo indicação diferente.