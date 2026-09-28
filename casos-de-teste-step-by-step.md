# Casos de Teste – Step-by-Step – SauceDemo

**Site:** https://www.saucedemo.com

---

## CT01 – Login com credenciais válidas

| Campo | Valor |
|---|---|
| **ID** | CT01 |
| **User Story relacionada** | US01 |
| **Título** | Login com credenciais válidas |
| **Pré-condição** | Estar na página https://www.saucedemo.com |
| **Prioridade** | Alta |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Preencher o campo "Username" com `standard_user`
3. Preencher o campo "Password" com `secret_sauce`
4. Clicar no botão "Login"

**Resultado esperado:**
Usuário é autenticado com sucesso e redirecionado para a página de inventário (`/inventory.html`), exibindo a lista de produtos.

---

## CT02 – Login com usuário bloqueado

| Campo | Valor |
|---|---|
| **ID** | CT02 |
| **User Story relacionada** | US02 |
| **Título** | Login com usuário bloqueado (locked_out_user) |
| **Pré-condição** | Estar na página https://www.saucedemo.com |
| **Prioridade** | Alta |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Preencher o campo "Username" com `locked_out_user`
3. Preencher o campo "Password" com `secret_sauce`
4. Clicar no botão "Login"

**Resultado esperado:**
Sistema exibe a mensagem de erro "Epic sadface: Sorry, this user has been locked out." e o usuário permanece na tela de login.

---

## CT03 – Login com campos obrigatórios vazios

| Campo | Valor |
|---|---|
| **ID** | CT03 |
| **User Story relacionada** | US03 |
| **Título** | Login sem preencher usuário e senha |
| **Pré-condição** | Estar na página https://www.saucedemo.com |
| **Prioridade** | Média |

**Passos:**
1. Acessar https://www.saucedemo.com
2. Deixar os campos "Username" e "Password" em branco
3. Clicar no botão "Login"

**Resultado esperado:**
Sistema exibe a mensagem de erro "Epic sadface: Username is required" e o usuário permanece na tela de login.
