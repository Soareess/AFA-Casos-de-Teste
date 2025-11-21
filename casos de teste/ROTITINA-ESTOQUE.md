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
| **Vídeo**                                                      |
| :------------------------------------------------------------ |
|[Video](https://drive.google.com/file/d/1TSYa0T1xm04MjW6nLMgT1f64l45Fy5x4/view?usp=drive_link)
|[Video](https://drive.google.com/file/d/1cKWzb71qUj69GDhc7RUPnJkm0AXoCk5B/view?usp=drive_link)


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
| **Vídeo**                                                      |
| :------------------------------------------------------------ |
|[Video](https://drive.google.com/file/d/13s_GplCUONXv9g08sVEXh-_kv_96PBzM/view?usp=drive_link)


### Caso de Teste 03: Importação com campos obrigatórios preenchidos
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C01-CT03 | Sistema permite importação de XML quando CFOP e Grupo são preenchidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma.                                                      |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário está na tela de importação  
E preenche CFOP e Grupo corretamente  
QUANDO tentar importar o XML  
ENTÃO a importação deve ser realizada com sucesso.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| XML é importado corretamente.                                  |
| Campos obrigatórios validados e aceitos pelo sistema.          |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
| [Video](https://drive.google.com/file/d/1ILPGg9tRvf3ivtWt1ylchJKs5OGocl5E/view?usp=drive_link)

### Caso de Teste 04: Gerar compra sem informar tipo de documento
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C01-CT04 | Compra permanece pendente quando o tipo de documento não é informado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| XML válido já importado.                                       |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário gera a compra e clica em **Finalizar**  
QUANDO for direcionado para a tela **Confirmar Compra**  
E não informar o **Tipo de Documento**  
ENTÃO deve ser exibida uma mensagem de erro e a compra não pode ser confirmada.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| Sistema impede a confirmação da compra sem o tipo de documento.|
| Estoque permanece inalterado.                                   |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
|[Video](https://drive.google.com/file/d/13gpaZLDdDZ2cmriAJna8DTUvEUbT56cU/view?usp=drive_link)
