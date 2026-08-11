# Evidências sobre sincronização e funcionamento offline

**Categoria:** análise de sistema e restrições técnicas  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva uma investigação histórica sobre continuidade offline, atualização segura, sincronização e conflitos no ARA. O material reúne critérios e alternativas produzidos antes do retorno do projeto ao pré-desenvolvimento.

Ele não aprova protocolo de sincronização, banco local, cache, formato de pacote, schema de fila ou recibo, API de compare-and-set, CRDT, mecanismo de merge, provedor, transporte, interface de conflitos ou implementação. As decisões vigentes permanecem em `DECISOES.md`, e as questões abertas permanecem no `BACKLOG.yaml`.

## 1. Problemas distintos

A investigação separou pelo menos dois problemas que não devem ser confundidos:

1. manter uma cópia local utilizável e recuperável diante de interrupção, atualização, corrupção ou pressão de armazenamento;
2. reconciliar trabalho local e estado conectado sem perda oculta nem fusão semântica indevida.

Uma solução para armazenamento local não determina, por si só, o protocolo de sincronização. Da mesma forma, um mecanismo de replicação não resolve sozinho ativação segura de uma nova versão no dispositivo.

## 2. Materialização e atualização offline

Um plano histórico de implementação propunha que uma pessoa pudesse adicionar ou importar um pacote de curso, inspecionar versão, perfil, capacidades e tamanho, materializá-lo localmente e continuar usando-o sem conexão.

O plano foi posteriormente encerrado sem implementação. Seus critérios residuais, porém, identificam problemas úteis para investigação futura:

- uma atualização interrompida ou corrompida não deveria destruir a última versão local válida;
- ativação de uma nova versão deveria ocorrer somente depois de verificações pertinentes;
- recarregar a aplicação sem conexão deveria preservar o estado funcional necessário ao uso previsto;
- pressão ou insuficiência de armazenamento deveria produzir estado explícito, não perda silenciosa;
- remover uma cópia local deveria distinguir consequências para dados locais, origem do conteúdo e eventual publicação;
- importação, exportação e diagnóstico deveriam permitir compreender o que está disponível localmente e o que depende de outra origem.

Esses pontos são critérios de investigação. Eles não aprovam IndexedDB, Cache API, OPFS, Service Worker, formato de pacote, política de cache ou algoritmo de ativação.

## 3. Sincronização sem perda oculta

Outro plano histórico tratava sincronização de:

- pacotes e objetos imutáveis;
- estado funcional pessoal;
- operações de autoria previamente autorizadas.

O objetivo declarado era permitir reconexão e uso em múltiplos dispositivos sem perda oculta nem merge semântico automático.

O plano mencionava como mecanismos candidatos:

- fila local de saída;
- recibos de aplicação;
- envio e aplicação idempotentes;
- identificação da revisão esperada;
- comparação entre revisão-base e estado conectado;
- download de objetos ou manifests imutáveis;
- retry e backoff;
- diagnóstico de operações pendentes ou falhas.

Esses mecanismos pertencem ao desenho histórico e não constituem contrato vigente.

## 4. Idempotência e repetição

A investigação considerou importante que duplicação, reordenação ou repetição de uma mesma operação não provoquem aplicação dupla silenciosa.

Esse problema permanece relevante independentemente do mecanismo técnico escolhido. Uma solução futura precisa explicitar:

- identidade ou equivalência de uma operação quando necessário;
- efeito de retries após falha parcial;
- garantias de ordenação realmente exigidas por cada classe de dado;
- comportamento diante de resposta perdida ou estado remoto desconhecido;
- forma de tornar pendências e falhas observáveis.

Request IDs, receipts e compare-and-set são alternativas históricas para atender a essas necessidades, não requisitos aprovados.

## 5. Conflitos e preservação da intenção local

O registro arquitetural histórico distinguia diferentes respostas a conflitos:

- reconhecer uma operação já aplicada;
- reaplicar uma intenção sobre uma revisão mais recente quando sua semântica continuar válida;
- criar uma derivação explícita quando houver revisões semanticamente concorrentes;
- solicitar escolha humana diante de conflito estrutural ou semântico.

O plano de implementação acrescentava possibilidades como manter a versão remota ou exportar o estado local para recuperação.

O conteúdo residual não é essa lista concreta de comandos. O princípio de investigação é que divergência relevante precisa permanecer visível e recuperável, sem apagar silenciosamente trabalho local nem fingir convergência semântica.

## 6. Merge determinístico e merge semântico

O material histórico aceitava merge determinístico somente para campos de estado funcional cuja semântica estivesse explicitamente definida. Também registrava, para aquele primeiro recorte, a decisão de não usar CRDTs nem merge semântico automático.

Na orientação atual, essa proibição não é uma decisão universal sobre CRDTs ou qualquer família de algoritmos. O que permanece sustentado pelas fontes é mais limitado:

- não há autorização para merge semântico silencioso de conteúdo educacional, configuração ou outras estruturas cujo conflito tenha significado relevante;
- uma política de merge precisa ser definida por classe de dado e por semântica, não escolhida apenas pela capacidade técnica de convergência;
- alternativas como CRDTs, logs de operações, sincronização por estado ou mecanismos especializados continuam abertas para comparação futura.

## 7. Revogação, retirada e estado offline

A sincronização também foi relacionada historicamente a mudanças de autoridade e disponibilidade, incluindo:

- revogação de permissão;
- retirada ou substituição de publicação;
- versões já materializadas no dispositivo;
- operações locais ainda não enviadas.

As fontes não definem uma política vigente para esses casos. Elas apenas demonstram que sincronização não pode ser modelada isoladamente de acesso, publicação, retenção e cópias offline.

Questões como bloqueio, preservação local, exportação, exclusão, reativação e uso de versões já baixadas permanecem dependentes das decisões futuras de colaboração, acesso, publicação e licenciamento.

## 8. Observabilidade e recuperação

A investigação tratava filas offline como potencialmente:

- inspecionáveis;
- repetíveis;
- exportáveis.

Também exigia que operações perdidas não fossem ocultadas.

A formulação atual deve ser mais aberta: uma solução futura precisa tornar estados relevantes compreensíveis e recuperáveis, mas a representação técnica e a interface continuam por definir.

`UX-003` já mantém aberta a investigação de estados offline, sincronização, conflito, permissão, capacidade indisponível e falha. O presente material não aprova mensagens, telas ou fluxos de resolução.

## 9. Relação com versionamento e proveniência

Sincronização depende do significado das revisões e do histórico, mas não deve redefini-los.

Na orientação atual:

- `VER-002` mantém abertas as escalas de histórico, checkpoints, restauração e sua relação com edição local e sincronização;
- `PROV-004` mantém aberta a definição dos fatos operacionais mínimos e sua retenção;
- `PROV-001` e `DEC-005` distinguem histórico deliberativo de histórico materializado.

Uma fila técnica, um receipt ou um evento de transporte não deve ser confundido automaticamente com revisão de curso, decisão humana ou evidência de pesquisa.

## 10. Relação com acesso, infraestrutura e validação

A investigação também se conecta a:

- `ACCESS-001`, porque revogações e cópias offline podem alterar disponibilidade sem apagar a trajetória;
- `ACCESS-002`, porque ações conectadas dependem de autenticação e autorização ainda não definidas;
- `INF-001`, porque armazenamento local, transporte, disponibilidade e custo permanecem questões de factibilidade;
- `VAL-001`, que prevê casos de interrupção, conflito, capacidade indisponível e falha recuperável;
- `VAL-002`, que exige separar disponibilidade, autoridade, validade e evidência.

Nenhum desses itens seleciona mecanismo de sincronização.

## 11. Planos de implementação superados

As duas issues históricas que detalhavam biblioteca offline e sincronização conectada foram encerradas como não planejadas quando o projeto retornou ao pré-desenvolvimento.

Por isso, não permanecem vigentes:

- releases e dependências daquele programa;
- telas e identificadores de estados daquele plano;
- critérios executáveis de implementação;
- escolha de IndexedDB ou cache local;
- estrutura concreta de outbox e receipts;
- compare-and-set como API definida;
- engine de sincronização;
- política de merge;
- fluxo de resolução de conflitos.

Somente os problemas, invariantes candidatos e cenários de falha continuam úteis como evidência.

## 12. Questões para investigação futura

A consolidação deste material deixa abertas, entre outras, as seguintes perguntas:

- quais classes de estado precisam estar disponíveis sem conexão;
- quais garantias tornam atualização e materialização recuperáveis;
- como representar estado local válido, atualização pendente, falha e recuperação;
- quais operações exigem idempotência e quais garantias de ordenação;
- como preservar intenção local diante de revisão remota divergente;
- quando uma divergência pode ser resolvida deterministicamente e quando exige escolha explícita;
- como revogação, retirada de publicação e versões offline interagem;
- quais estados e evidências precisam ser inspecionáveis ou exportáveis;
- quais alternativas oferecem a menor complexidade compatível com os cenários aprovados.

A recomendação residual é metodológica: definir primeiro semântica, estados de falha e garantias observáveis; somente depois comparar protocolos, engines e mecanismos físicos.
