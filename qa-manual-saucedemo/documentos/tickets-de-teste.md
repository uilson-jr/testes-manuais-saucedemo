# Tickets de Teste

## 1. Validar funcionalidade de login
**Tipo:** Tarefa  
**Prioridade:** Alta  

**Objetivo:**  
Verificar se a funcionalidade de login da aplicação permite autenticação com credenciais válidas e trata corretamente cenários de erro.

**Pré-condição:**  
Usuário deve estar na tela inicial de login da aplicação.

**Cenários de teste:**
- login com credenciais válidas
- login com senha incorreta
- login com campos vazios
- login com usuário bloqueado

**Dados de teste:**
- Usuário válido: `standard_user`
- Usuário bloqueado: `locked_out_user`
- Senha válida: `secret_sauce`

**Passos para teste:**
1. Acessar `https://www.saucedemo.com`
2. Validar login com usuário `standard_user` e senha `secret_sauce`
3. Validar login com usuário `standard_user` e senha incorreta
4. Validar tentativa de login com campos vazios
5. Validar login com usuário `locked_out_user` e senha `secret_sauce`

**Resultado esperado:**
- o sistema deve permitir acesso com credenciais válidas
- o sistema deve exibir mensagem de erro para senha incorreta
- o sistema deve exibir mensagem de erro para campos obrigatórios vazios
- o sistema deve impedir o acesso do usuário bloqueado e informar a restrição

**Resultado obtido:**  
Os cenários executados apresentaram o comportamento esperado durante a validação.

**Comentário de conclusão:**  
Teste executado com sucesso.  
Foram validados os cenários de login com credenciais válidas, senha incorreta, campos vazios e usuário bloqueado.  
O sistema apresentou o comportamento esperado em todos os cenários testados.  
Nenhum defeito foi identificado.

---

## 2. Validar exibição de produtos após o login
**Tipo:** Tarefa  
**Prioridade:** Média  

**Objetivo:**  
Verificar se a aplicação exibe corretamente a lista de produtos após a autenticação do usuário.

**Pré-condição:**  
Usuário deve estar autenticado com sucesso no sistema.

**Passos para teste:**
1. Acessar `https://www.saucedemo.com`
2. Realizar login com usuário válido
3. Acessar a página de produtos
4. Validar os elementos exibidos na listagem

**Verificações:**
- nome dos produtos
- descrição dos produtos
- preço dos produtos
- imagem dos produtos
- botão de adicionar ao carrinho

**Resultado esperado:**  
A aplicação deve apresentar a listagem de produtos corretamente, exibindo nome, descrição, preço, imagem e ações disponíveis para cada item.

**Resultado obtido:**  
A listagem de produtos foi exibida corretamente durante a execução do teste.

**Comentário de conclusão:**  
Validação concluída com sucesso.  
A listagem de produtos foi exibida corretamente após a autenticação, com nome, descrição, preço, imagem e ações disponíveis conforme esperado.  
Nenhuma inconsistência foi observada durante a execução.

---

## 3. Validar carrinho de compras
**Tipo:** Tarefa  
**Prioridade:** Alta  

**Objetivo:**  
Verificar se a funcionalidade de carrinho permite adicionar e remover produtos corretamente, além de atualizar o contador de itens.

**Pré-condição:**  
Usuário deve estar logado no sistema e na página de produtos.

**Cenários de teste:**
- adicionar produto ao carrinho
- remover produto do carrinho
- validar atualização do contador de itens

**Passos para teste:**
1. Realizar login com usuário válido
2. Selecionar um produto e clicar em Add to Cart
3. Validar atualização do contador do carrinho
4. Acessar o carrinho
5. Remover o produto adicionado
6. Validar se o item foi removido corretamente
7. Validar atualização do contador após remoção

**Resultado esperado:**
- o sistema deve adicionar o produto ao carrinho com sucesso
- o contador do carrinho deve refletir a quantidade correta de itens
- o sistema deve remover o produto corretamente
- o contador deve ser atualizado após a remoção

**Resultado obtido:**  
As ações de adicionar e remover produtos funcionaram corretamente, com atualização adequada do contador de itens.

**Comentário de conclusão:**  
Teste finalizado com resultado satisfatório.  
Foram validadas as ações de adição e remoção de produtos no carrinho, bem como a atualização do contador de itens.  
O fluxo funcionou conforme esperado.

---

## 4. Validar fluxo de checkout
**Tipo:** Tarefa  
**Prioridade:** Alta  

**Objetivo:**  
Verificar se o usuário consegue concluir o processo de compra com sucesso, desde o início do checkout até a confirmação final do pedido.

**Pré-condição:**  
Usuário deve estar logado e com pelo menos um produto adicionado ao carrinho.

**Cenários de teste:**
- iniciar checkout
- preencher dados obrigatórios
- concluir pedido

**Dados de teste:**
- First Name: `Uilson`
- Last Name: `Junior`
- Postal Code: `00000`

**Passos para teste:**
1. Realizar login com usuário válido
2. Adicionar pelo menos um produto ao carrinho
3. Acessar o carrinho
4. Clicar em Checkout
5. Preencher os campos First Name, Last Name e Postal Code
6. Clicar em Continue
7. Revisar as informações da compra
8. Clicar em Finish

**Resultado esperado:**
- o sistema deve permitir o início do checkout
- os dados obrigatórios devem ser aceitos corretamente
- a navegação para a etapa de revisão deve ocorrer sem erro
- o pedido deve ser finalizado com sucesso
- a aplicação deve exibir mensagem de confirmação da compra

**Resultado obtido:**  
O fluxo de checkout foi executado com sucesso até a confirmação final do pedido.

**Comentário de conclusão:**  
Fluxo validado com sucesso.  
O processo de checkout foi executado desde o início da compra até a confirmação final do pedido.  
Nenhum erro foi encontrado nos cenários realizados.
