# User Stories – SauceDemo

**Site:** https://www.saucedemo.com

---

## Épico 1: Autenticação

### US01 – Login com sucesso
**Como** usuário cadastrado,
**quero** fazer login com usuário e senha válidos,
**para** acessar a página de produtos.

**Critérios de aceite:**
- Dado que estou na tela de login, quando informo `standard_user` / `secret_sauce` e clico em "Login", então sou redirecionado para a página de inventário (`/inventory.html`).

### US02 – Bloqueio de usuário
**Como** usuário do sistema,
**quero** receber uma mensagem de erro ao tentar logar com um usuário bloqueado,
**para** entender que não tenho acesso.

**Critérios de aceite:**
- Dado que informo `locked_out_user` / `secret_sauce`, quando clico em "Login", então o sistema exibe a mensagem "Epic sadface: Sorry, this user has been locked out." e permaneço na tela de login.

### US03 – Campos obrigatórios
**Como** usuário do sistema,
**quero** ser avisado quando deixo usuário ou senha em branco,
**para** corrigir antes de tentar novamente.

**Critérios de aceite:**
- Dado que deixo o campo "Username" ou "Password" vazio, quando clico em "Login", então é exibida a mensagem de erro correspondente ("Username is required" ou "Password is required").

---

## Épico 2: Catálogo de Produtos

### US04 – Visualizar lista de produtos
**Como** usuário logado,
**quero** visualizar a lista de produtos disponíveis,
**para** escolher o que desejo comprar.

**Critérios de aceite:**
- Dado que estou logado, quando acesso a página de inventário, então vejo nome, imagem, descrição e preço de cada um dos 6 produtos.

### US05 – Ordenar produtos
**Como** usuário logado,
**quero** ordenar os produtos por nome (A-Z, Z-A) ou preço (menor-maior, maior-menor),
**para** encontrar itens mais facilmente.

**Critérios de aceite:**
- Dado que estou na página de inventário, quando seleciono uma opção no dropdown de ordenação, então a lista é reordenada de acordo com o critério escolhido.

### US06 – Ver detalhes do produto
**Como** usuário logado,
**quero** clicar em um produto para ver seus detalhes,
**para** conhecer melhor o item antes de comprar.

**Critérios de aceite:**
- Dado que clico no nome ou imagem de um produto, então sou direcionado à página de detalhes com descrição completa, preço e botão de adicionar ao carrinho.

---

## Épico 3: Carrinho de Compras

### US07 – Adicionar produto ao carrinho
**Como** usuário logado,
**quero** adicionar um produto ao carrinho,
**para** comprá-lo posteriormente.

**Critérios de aceite:**
- Dado que estou na página de inventário, quando clico em "Add to cart", então o botão muda para "Remove" e o ícone do carrinho exibe a quantidade de itens.

### US08 – Remover produto do carrinho
**Como** usuário logado,
**quero** remover um produto do carrinho,
**para** ajustar minha compra.

**Critérios de aceite:**
- Dado que um produto está no carrinho, quando clico em "Remove" (na listagem ou na página do carrinho), então o item é removido e o contador do carrinho é atualizado.

### US09 – Visualizar carrinho
**Como** usuário logado,
**quero** visualizar os itens adicionados ao carrinho,
**para** conferir minha seleção antes de finalizar a compra.

**Critérios de aceite:**
- Dado que clico no ícone do carrinho, então sou direcionado à página do carrinho, onde vejo nome, descrição, quantidade e preço de cada item.

---

## Épico 4: Checkout

### US10 – Preencher informações de checkout
**Como** usuário logado com itens no carrinho,
**quero** informar meus dados pessoais (nome, sobrenome, CEP),
**para** prosseguir com a compra.

**Critérios de aceite:**
- Dado que estou na página do carrinho, quando clico em "Checkout" e preencho os campos obrigatórios, então avanço para a tela de resumo do pedido.
- Se algum campo estiver vazio, o sistema exibe mensagem de erro e não avança.

### US11 – Revisar resumo do pedido
**Como** usuário logado,
**quero** visualizar o resumo do pedido (itens, subtotal, taxa e total),
**para** confirmar antes de finalizar.

**Critérios de aceite:**
- Dado que preenchi os dados de checkout, quando avanço, então vejo a lista de itens, "Item total", "Tax" e "Total" corretamente calculados.

### US12 – Finalizar compra
**Como** usuário logado,
**quero** finalizar minha compra,
**para** concluir o processo e receber a confirmação do pedido.

**Critérios de aceite:**
- Dado que estou na tela de resumo do pedido, quando clico em "Finish", então sou direcionado à página de confirmação com a mensagem "Thank you for your order!".

### US13 – Cancelar checkout
**Como** usuário logado,
**quero** cancelar o processo de checkout,
**para** voltar à página de produtos sem finalizar a compra.

**Critérios de aceite:**
- Dado que estou em qualquer etapa do checkout, quando clico em "Cancel", então retorno à página de inventário mantendo os itens no carrinho.

---

## Épico 5: Sessão e Menu

### US14 – Logout
**Como** usuário logado,
**quero** sair da aplicação,
**para** encerrar minha sessão com segurança.

**Critérios de aceite:**
- Dado que abro o menu (ícone hambúrguer), quando clico em "Logout", então sou redirecionado à tela de login e minha sessão é encerrada.

### US15 – Resetar estado da aplicação
**Como** usuário logado,
**quero** resetar o estado da aplicação,
**para** limpar carrinho e voltar às configurações iniciais.

**Critérios de aceite:**
- Dado que abro o menu, quando clico em "Reset App State", então o carrinho é esvaziado e os botões de "Add to cart" retornam ao estado inicial.
