# Evidências sobre execução de código não confiável

**Categoria:** análise técnica de execução, validação e isolamento  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação técnica sobre atividades educacionais que executam código produzido pelo estudante. O resultado principal da investigação é uma separação de responsabilidades e riscos, não uma escolha de runtime, sandbox ou infraestrutura.

A evidência não aprova Web Worker, Node `vm`, container, microVM, Pyodide, Papyros, runtime de navegador, serviço remoto, linguagem, imagem, pacote, limite de recursos, schema, API ou perfil de implantação. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Execução funcional não equivale a isolamento

Uma prova funcional anterior demonstrou operações como parsing, execução, testes, timeout, interrupção, limitação de saída e separação entre testes públicos e protegidos. Essa demonstração não comprovou que o ambiente fosse seguro contra código hostil nem adequado a avaliação protegida.

A investigação distinguiu sete responsabilidades:

1. resposta de código do estudante;
2. validação pública;
3. validação protegida;
4. serviço de execução;
5. garantia de isolamento;
6. política de recursos;
7. evidência diagnóstica.

A separação evita duas inferências indevidas:

- um editor ou renderer capaz de manipular código não recebe autoridade implícita para executá-lo;
- um runtime capaz de executar corretamente não recebe autoridade implícita para proteger o host.

## 2. Validação pública e validação protegida

A investigação tratou como situações distintas a execução local para estudo de baixo risco e a validação que precisa proteger testes, recursos ou infraestrutura.

### Execução local e testes públicos

Uma capacidade local pode ser útil para retorno rápido, estudo sem conexão, visualização, experimentação e testes públicos. Isso não demonstra:

- segredo de testes;
- isolamento contra código hostil;
- equivalência com avaliação protegida;
- limites uniformes de memória ou recursos entre navegadores e dispositivos.

Uma interface futura precisa evitar apresentar um resultado local de alcance limitado como se fosse avaliação completa ou autoritativa quando a condição necessária não estiver disponível.

### Validação protegida

A investigação formulou como hipótese que testes protegidos ou execução hostil exigem uma fronteira de confiança diferente do cliente comum. Foram citadas como propriedades candidatas de um ambiente desse tipo:

- execução efêmera;
- isolamento revisto;
- runtime e dependências versionados;
- rede desativada por padrão quando compatível com a tarefa;
- base somente leitura;
- armazenamento temporário limitado;
- limites explícitos de CPU, tempo, memória e saída;
- cancelamento confiável;
- material protegido fora do conteúdo distribuído ao estudante;
- diagnósticos que não reconstruam segredos;
- logs mínimos e governados.

Essas propriedades são critérios de investigação. Não constituem requisitos aprovados nem autorizam construir um serviço de execução.

## 3. Testes protegidos e evidência

Uma alternativa histórica representava testes protegidos por uma referência opaca ao ambiente responsável pela avaliação, em vez de incluir no curso o código, as entradas ou as respostas esperadas.

O princípio residual é separar:

- material que pode ser distribuído ao estudante;
- material cuja confidencialidade é necessária à avaliação;
- evidência que pode ser devolvida para orientar aprendizagem ou contestação.

A forma do identificador, o contrato entre cliente e host e a política de divulgação de diagnósticos permanecem questões abertas.

## 4. Reprodutibilidade da execução

A investigação registrou como candidatos para reproduzir uma execução autoritativa:

- linguagem e versão;
- versão ou digest do runtime;
- bibliotecas permitidas;
- limites efetivamente aplicados;
- localização da validação;
- versão da suíte de testes;
- política de evidência.

Esses campos são exemplos de informação necessária à reprodutibilidade e auditoria. Eles não definem schema ou formato de receipt aprovado.

A resposta do estudante deve continuar distinguível do ambiente que a executou. Trocar runtime ou infraestrutura não deve alterar silenciosamente a identidade da resposta submetida.

## 5. Limites dos mecanismos examinados

Na rodada histórica, Web Worker e Node `vm` foram considerados inadequados **como fronteira produtiva contra código hostil**. Esse resultado é preservado como conclusão situada daquele ensaio, não como proibição universal de uso dessas ferramentas para outras finalidades.

Web Workers podem continuar úteis para isolamento de responsividade, execução local ou tarefas de baixo risco. Node `vm` pode ter usos legítimos fora de uma fronteira de segurança hostil. O que não foi sustentado pela investigação é tratá-los, isoladamente, como sandbox de segurança de produção.

Containers e microVMs foram mencionados apenas como famílias de mecanismos a estudar. Nenhuma delas foi selecionada, e sua segurança dependeria de configuração, operação, atualização, políticas de recursos e modelo de ameaça.

Runtimes de navegador, incluindo alternativas para Python ou computação científica local, também foram tratados como possíveis capacidades educacionais. Sua eventual utilidade não resolve automaticamente segredo de testes, isolamento hostil, limites rígidos de recursos, abuso ou equivalência entre dispositivos.

## 6. Separação de contextos de confiança

A investigação também distinguiu a execução de código produzido por estudante da execução de ferramentas locais usadas por um autor ou administrador confiável.

Mesmo quando ambos executam código, os contextos não devem compartilhar automaticamente:

- credenciais;
- permissões;
- segredos;
- infraestrutura de avaliação;
- políticas de rede e armazenamento.

A identidade do ator e o contexto de confiança não podem ser inferidos apenas pelo fato de o mesmo runtime ou linguagem estar envolvido.

## 7. Relação com as pendências vigentes

O conteúdo residual está distribuído sem necessidade de um novo item de backlog:

- `MODEL-003` mantém aberta a separação entre representação, prática, resposta, validação e retorno pedagógico;
- `VAL-002` mantém separadas validade, satisfação de critérios, disponibilidade da capacidade, autoridade e evidência da validação;
- `EXP-009` investiga governança, segurança, isolamento e atualização de capacidades instaladas;
- `INF-001` mantém aberta a factibilidade de infraestrutura, desempenho, custo, portabilidade e funcionamento offline;
- `PED-004` exige que formas de interação e retorno sejam avaliadas também por acessibilidade;
- `DEC-007` impede converter esta investigação em autorização para implementação.

Aspectos de implantação, conformidade entre ambientes, operação autogerenciada e eventual serviço protegido devem ser confrontados com o domínio de implantação e interoperabilidade antes de qualquer decisão.

## 8. Pendências preservadas

Antes de qualquer escolha futura, ainda será necessário:

- definir um modelo de ameaça específico para execução de código não confiável;
- delimitar quais atividades realmente precisam de execução e quais precisam de validação protegida;
- definir autoridade de avaliação e comportamento quando a capacidade protegida estiver indisponível;
- comparar execução local, remota e híbrida por finalidade educacional e risco;
- avaliar isolamento, rede, filesystem, pacotes, segredos, limites de CPU, memória, tempo e saída;
- definir evidências e diagnósticos úteis sem vazar material protegido;
- medir latência, custo, consumo de recursos, funcionamento offline e impacto em dispositivos modestos;
- avaliar acessibilidade, recuperação de falhas, cancelamento, abuso e operação institucional;
- definir reprodutibilidade, retenção de logs e governança de dados;
- comparar tecnologias de isolamento somente depois desses requisitos.

A investigação sustenta uma regra metodológica: **capacidade de executar não demonstra capacidade de isolar, e capacidade de validar localmente não demonstra autoridade para uma avaliação protegida**. A tecnologia concreta permanece aberta.