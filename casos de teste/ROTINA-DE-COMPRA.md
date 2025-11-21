-------------------------------------------
## ✅ CENÁRIO 02 – PROCESSAMENTO DE VENDA (PDV)
-------------------------------------------

### Caso de Teste 01: Venda com múltiplas formas de pagamento
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT01	 | Sistema deve registrar venda paga com duas formas de pagamento distintas.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Cliente, funcionário e produtos cadastrados.|
|Formas de pagamento múltiplas habilitadas no sistema.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário clica em “Novo” na tela de vendas  
E seleciona cliente, funcionário e data  
E adiciona produtos à venda  
QUANDO escolher duas formas de pagamento (ex.: dinheiro + cartão)  
E finalizar a venda  
ENTÃO o sistema deve registrar corretamente os valores separados no Livro Caixa.|

| **Critérios de Aceitação**                                         |
| :------------------------------------------------------------ |
|Valores distribuídos corretamente entre as duas formas de pagamento.|
|Registro completo no Livro Caixa.|
|Comprovante exibindo as duas formas de pagamento.|
|Venda salva sem inconsistências.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 02: Produto sem estoque
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT02	 | Sistema deve permitir venda sem estoque.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Produto com quantidade = 0.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário tenta incluir o produto  
QUANDO selecionar quantidade  
O sistema deve permitir proceguir a venda.  
Deve estar no Livro caixa

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Produto deve entrar na venda.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 03: Falha ao finalizar venda sem selecionar tipo de pagamento
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT03	 | Sistema deve bloquear venda quando nenhum tipo de pagamento é selecionado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Venda pronta para finalizar.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário adicionou produtos à venda  
E não seleciona nenhuma forma de pagamento  
QUANDO tentar finalizar a venda  
ENTÃO o sistema deve exibir alerta e impedir a conclusão.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Venda não é registrada sem tipo de pagamento.|
|Mensagem de erro clara exibida ao usuário.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 04: Calcular valor total da venda com múltiplos itens
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT04	 | Sistema deve calcular corretamente o valor total considerando produtos e quantidades diferentes.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Produtos cadastrados com preço definido.|
|Venda em andamento com pelo menos dois itens.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário adiciona múltiplos produtos à venda  
E informa quantidades diferentes para cada item  
QUANDO o sistema recalcular o total  
ENTÃO o valor final deve refletir a soma correta de todos os produtos e suas quantidades.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Total calculado corretamente.|
|Atualização automática do valor final ao alterar quantidade.|
|Resumo da venda exibindo valores por item e total geral.|
|Nenhuma diferença entre o valor exibido e o valor registrado no caixa.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

-------------------------------------------
## ✅ CENÁRIO 04 – GESTÃO DE CLIENTES
-------------------------------------------

### Caso de Teste 01: Cadastro de cliente PF com sucesso
| ID       | Descrição
