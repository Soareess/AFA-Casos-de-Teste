-------------------------------------------
## ✅ CENÁRIO 03 – COMPRA POR FORNECEDOR
-------------------------------------------

### Caso de Teste 01: Compra concluída com sucesso
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT01	 | Compra lançada, estoque atualizado e caixa alimentado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Fornecedor cadastrado.|
|Produto cadastrado.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário cria nova compra  
E adiciona produtos  
QUANDO finalizar compra  

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Compra CONFIRMADA.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 02: Falha ao criar compra sem fornecedor
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT02	 | Sistema deve impedir finalização de compra quando nenhum fornecedor é selecionado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Nenhum fornecedor selecionado.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário tenta criar compra sem fornecedor  
QUANDO clicar em “Salvar”  
ENTÃO sistema deve bloquear a finalização e exibir alerta.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Compra não é registrada sem fornecedor.|
|Mensagem de erro “Fornecedor obrigatório” exibida.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 03: Falha ao finalizar compra sem tipo de pagamento
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT03	 | Sistema deve impedir finalização de compra quando nenhum tipo de pagamento é selecionado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Fornecedor e produtos cadastrados.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário adiciona produtos à compra  
E não seleciona nenhum tipo de pagamento  
QUANDO tentar finalizar a compra  
ENTÃO o sistema deve exibir alerta e bloquear a finalização.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Compra não é registrada sem tipo de pagamento.|
|Mensagem de erro clara exibida ao usuário.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 04: Compra parcial concluída com sucesso
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT04	 | Sistema registra compra parcial e atualiza estoque apenas para itens recebidos.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Fornecedor e produtos cadastrados.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário adiciona produtos à compra  
E nem todos os itens estão disponíveis para entrega imediata  
QUANDO finalizar a compra  
ENTÃO sistema registra apenas os itens recebidos e atualiza estoque parcial.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Estoque atualizado apenas para itens recebidos.|
|Compra parcial registrada corretamente.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |
