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
| [Video](https://drive.google.com/file/d/1crQDVs6hcyxm4sOz9qBGRqFtFUz78f9f/view?usp=drive_link)

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
| [Videos](https://drive.google.com/file/d/18l5vwQMqFEqkQlzINHVA32kdKcnLA_L2/view?usp=drive_link)

### Caso de Teste 03: Calcular valor total da venda com múltiplos itens
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT03	 | Sistema deve calcular corretamente o valor total considerando produtos e quantidades diferentes.|

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
| [Video](https://drive.google.com/file/d/1sLNRrGBfC8hKxqbyhgCpbOFn0CQmHrD3/view?usp=drive_link)

### Caso de Teste 04: Finalizar venda sem selecionar tipo de documento
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C02-CT04	 | Sistema deve impedir finalização sem forma de pagamento.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Venda pronta para finalizar.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário está na tela final  
QUANDO clicar em “Salvar” sem escolher tipo de documento  
ENTÃO deve exibir erro.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Finalização bloqueada.|

| **Video**                                         |
| :------------------------------------------------------------ |
| [Video](https://drive.google.com/file/d/17DxeeWmGmYK4h3ED7QwBqfGpvKPbRUfS/view?usp=drive_link)
