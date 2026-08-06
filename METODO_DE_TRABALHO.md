# Método de trabalho do projeto ARA

## 1. Finalidade

Este documento estabelece o método usado para pesquisar, discutir, decidir, especificar e desenvolver o ARA de forma coerente, rastreável e compreensível.

## 2. Princípios

1. O repositório deve ser compreensível sem acesso a conversas externas.
2. Ideia, problema, evidência, hipótese, alternativa, recomendação, decisão, requisito, implementação e validação são categorias distintas.
3. Ideias relevantes devem ser preservadas, mas não podem ser tratadas como requisitos aprovados sem decisão explícita.
4. Decisões aprovadas substituem formulações incompatíveis e deixam de aparecer como questões abertas.
5. A documentação deve combinar rigor técnico e clareza didática.
6. A factibilidade deve ser considerada continuamente, sem reduzir prematuramente a visão integral do produto.
7. Visão de produto, recorte de implementação, avaliação acadêmica e adoção institucional são escopos distintos.

## 3. Fontes canônicas

- `README.md`: apresentação e navegação geral;
- `METODO_DE_TRABALHO.md`: regras do processo;
- `BACKLOG.yaml`: única lista canônica de itens;
- `DECISOES.md`: decisões aprovadas e suas consequências.

Novos documentos só devem ser criados quando houver uma responsabilidade documental estável que não caiba nessas fontes.

## 4. Fluxo de trabalho

```text
ideia, problema ou dúvida
→ registro no backlog
→ investigação bibliográfica, técnica ou empírica, quando necessária
→ explicitação de alternativas, critérios, consequências e restrições
→ decisão
→ atualização das fontes canônicas afetadas
→ auditoria de consistência
→ encerramento do tópico
```

## 5. Estados do backlog

- `captured`: item registrado, ainda não investigado;
- `pending_research`: depende de pesquisa;
- `under_review`: em análise;
- `pending_owner_approval`: pronto para decisão;
- `approved`: aprovado como parte da orientação vigente;
- `rejected`: rejeitado;
- `deferred`: adiado;
- `superseded`: substituído por decisão posterior;
- `implementation_ready`: pronto para implementação;
- `implemented`: implementado;
- `validated`: verificado segundo critérios definidos.

## 6. Pesquisa e rastreabilidade

Quando uma decisão depender de conhecimento externo, devem ser preservados, conforme a relevância:

- pergunta investigada;
- bases, fontes e estratégia de busca;
- datas, filtros e critérios de seleção;
- corpus recuperado e analisado;
- síntese e limitações;
- alternativas identificadas;
- implicações para o ARA;
- decisão resultante;
- itens do backlog afetados.

A cadeia de rastreabilidade desejada é:

```text
questão → evidências → alternativas → critérios → decisão → requisito → critério de aceite
```

## 7. Alterações no repositório

Antes de qualquer alteração:

1. ler as fontes canônicas afetadas;
2. localizar o item ou decisão correspondente;
3. identificar complementação, conflito ou substituição;
4. escolher o local canônico correto.

Depois da alteração:

1. atualizar todos os registros afetados;
2. remover contradições e questões encerradas;
3. atualizar critérios de aceite e termos pertinentes;
4. verificar a consistência entre as fontes canônicas;
5. registrar objetivamente o que foi materializado.

## 8. Telas e fluxos

Uma tela ou comportamento aprovado deve ser registrado no backlog com referência ao artefato visual, à decisão correspondente e aos critérios de aceite. Alternativas incompatíveis deixam de orientar o produto.

## 9. Preparação para implementação

Itens de implementação só devem ser abertos quando estiverem suficientemente definidos, com:

- comportamento aprovado;
- dependências;
- cenários;
- invariantes;
- critérios de aceite;
- referências às decisões, evidências e telas necessárias.

## 10. Regra de encerramento

Antes de mudar de assunto, deve-se verificar se:

- ideias novas foram capturadas;
- evidências foram vinculadas;
- decisões foram registradas;
- pendências continuam visíveis;
- contradições foram removidas;
- o backlog foi atualizado;
- o tópico recebeu o estado correto.
