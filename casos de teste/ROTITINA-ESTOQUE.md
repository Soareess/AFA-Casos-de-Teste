-------------------------------------------
## ✅ CENÁRIO 01 – INVENTÁRIO DE ESTOQUE
-------------------------------------------

### Caso de Teste 01: Importação de XML válido e geração de compra
| ID       | Descrição                                                       |
| -------- | ---------------------------------------------------------------- |
| C01-CT01 | Importação de XML válido atualiza o estoque corretamente.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| - Possuir XML válido.                                         |
| - Produtos contidos na nota já cadastrados no sistema.        |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário acessa **Pedidos > Importar XML de Compra**  
E preenche CFOP, Grupo e ST Entrada  
E importa um XML válido  
QUANDO clicar em **Gerar Compra** e em seguida **Finalizar**  
ENTÃO o estoque deve ser atualizado e a compra exibida como **CONFIRMADA**.  

| **Critérios de aceitação**                                      |
| :------------------------------------------------------------ |
| Compra confirmada.                                               |
| Produtos lançados corretamente no estoque.                     |

---

### Caso de Teste 02: Importação de XML inválido
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C01-CT02 | Sistema deve recusar XML com estrutura inválida.                 |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| - XML com estrutura incorreta ou corrompido.                   |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário acessa a tela de importação  
E seleciona um XML corrompido  
QUANDO clicar em **Importar XML**  
ENTÃO deve ser exibida uma mensagem de erro, bloqueando a ação.  

| **Critérios de aceitação**                                      |
| :------------------------------------------------------------ |
| Mensagem clara de erro apresentada.                             |
| Não é permitido gerar compra a partir do XML inválido.         |

---

### Caso de Teste 03: Falta de preenchimento obrigatório
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C01-CT03 | Sistema bloqueia importação quando CFOP ou Grupo não são preenchidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| - Nenhuma.                                                     |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário está na tela de importação  
E deixa CFOP ou Grupo em branco  
QUANDO tentar importar o XML  
ENTÃO devem ser exibidas mensagens indicando os campos obrigatórios.  

| **Critérios de aceitação**                                      |
| :------------------------------------------------------------ |
| Validação de campos obrigatórios realizada corretamente.       |

---

### Caso de Teste 04: Gerar compra sem confirmar entrada
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C01-CT04 | Compra permanece pendente sem confirmação de entrada.            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| - XML válido já importado.                                     |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário gera a compra  
QUANDO sair da tela sem alterar o status para **CONFIRMADA**  
ENTÃO a compra deve permanecer com status **PENDENTE**  
E o estoque não deve ser alterado.  

| **Critérios de aceitação**                                      |
| :------------------------------------------------------------ |
| Estoque permanece inalterado.                                   |
