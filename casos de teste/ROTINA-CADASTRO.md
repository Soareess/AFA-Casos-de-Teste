-------------------------------------------
## ✅ CENÁRIO 04 – GESTÃO DE CLIENTES
-------------------------------------------

### Caso de Teste 01: Cadastro de cliente PF com sucesso
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT01	 | Cadastro básico deve ser salvo corretamente.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Nenhum cadastro pendente.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário seleciona “Novo” na tela de clientes  
E preenche todos os campos obrigatórios corretamente  
QUANDO clicar no botão Salvar  
ENTÃO o cliente deve ser listado entre os registros.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|O cadastro é salvo com sucesso e aparece na lista.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 02: Cadastro com campos não obrigatórios vazios
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
| C04-CT02 | Sistema deve permitir salvar cadastro mesmo quando CEP, Rua, Bairro, UF/Estado e Cidade não forem preenchidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma.                                                      |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário deixa em branco os campos **CEP, Rua, Bairro, UF/Estado e Cidade**  
QUANDO tentar salvar o cadastro  
ENTÃO o sistema deve permitir o cadastro sem apresentar erros.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| Cadastro é salvo corretamente.                                 |
| Nenhuma mensagem de erro é exibida relacionada a esses campos. |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |


### Caso de Teste 03: Limite de crédito controlado dinamicamente
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT03	 | Sistema deve alertar apenas quando a venda ultrapassa limite ajustado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Cliente com limite de crédito definido dinamicamente.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o cliente tem limite de R$100  
QUANDO a venda ultrapassar R$150  
ENTÃO o sistema exibe alerta e abre fluxo de contas a receber.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Alerta exibido somente se venda ultrapassar limite atualizado.|
|Venda permitida após confirmação do usuário.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |

### Caso de Teste 04: Cadastrar dependente corretamente
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT04	 | Dependente deve ser vinculado ao cliente.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Cliente principal já cadastrado.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário acessa a aba Dependentes  
E clica no botão “Novo”  
QUANDO selecionar o cliente dependente  
ENTÃO o registro do dependente deve ser vinculado corretamente ao cliente principal.|

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Dependente aparece listado na aba do cliente principal.|

| **Video**                                         |
| :------------------------------------------------------------ |
| |
