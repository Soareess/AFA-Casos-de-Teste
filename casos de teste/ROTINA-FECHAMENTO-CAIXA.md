-------------------------------------------
## ✅ CENÁRIO 05 – FECHAMENTO DE CAIXA
-------------------------------------------

### Caso de Teste 01: Fechar caixa com sucesso
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C05-CT01 | Caixa do dia fechado e registrado.                                |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Haver pelo menos uma venda registrada no dia.                 |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário abre o **Livro Caixa**  
QUANDO clicar em **Fechar Caixa**  
ENTÃO o caixa deve ser finalizado corretamente.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| O dia fica bloqueado para novas movimentações.                 |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
|  [Video](https://drive.google.com/file/d/1r1jnXmuGFv8yZB3oqqeEJDQsd1mNOG6-/view?usp=drive_link)

---

### Caso de Teste 02: Tentar fechar caixa sem vendas no dia
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C05-CT02 | Sistema deve permitir fechamento mesmo sem vendas registradas.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma venda registrada no dia.                               |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário tenta fechar o caixa  
QUANDO clicar em **Fechar**  
ENTÃO o sistema deve permitir o fechamento do caixa.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| O fechamento é permitido mesmo sem movimentações.             |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
| [Video](https://drive.google.com/file/d/19ZU38Dq5c5MmA-ryporugMA4kCFgFAlC/view?usp=drive_link)

---

### Caso de Teste 03: Retirada de valores maior que o disponível
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C05-CT03 | Retirada de valor maior que o disponível no caixa deve retornar erro. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Caixa do dia aberto com saldo disponível.                     |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário acessa **Retirar Valores**  
E clica em **Novo**  
QUANDO preencher **Valor** maior que o saldo disponível  
ENTÃO o sistema deve exibir uma mensagem de erro e não permitir a retirada.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| Retirada não registrada.                                        |
| Mensagem clara de erro exibida.                                 |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
| [Video](https://drive.google.com/file/d/1dlRWMVg0sUTdAQVmKAdM15u7hy4mYJj0/view?usp=drive_link)

---

### Caso de Teste 04: Retirada sem preencher campos obrigatórios
| ID       | Descrição                                                        |
| -------- | ---------------------------------------------------------------- |
| C05-CT04 | Sistema deve bloquear retirada quando campos obrigatórios não forem preenchidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma.                                                      |

| **Passos**                                                    |
| :------------------------------------------------------------ |
DADO que o usuário deixa o **Histórico** em branco  
QUANDO tentar salvar a retirada  
ENTÃO deve ser exibida uma mensagem de alerta sobre campos obrigatórios.  

| **Critérios de Aceitação**                                      |
| :------------------------------------------------------------ |
| Retirada não é registrada no sistema.                         |

| **Vídeo**                                                      |
| :------------------------------------------------------------ |
| [Video](https://drive.google.com/file/d/18mOT65QOK7wQJIWJ3JeBXm35Nh56AYe9/view?usp=drive_link)
