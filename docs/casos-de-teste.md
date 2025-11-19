# 💻 Casos de Teste – Projeto Demoblaze

Este documento reúne todos os casos de teste manuais aplicados ao site [Demoblaze](https://www.demoblaze.com/), organizados por tipo de teste.

---

## 🔹 Testes Funcionais

### TC001 – Realizar cadastro de usuário
- **Pré-condições:** Acesso ao cadastro
- **Passos:**
  1. Acessar a página inicial
  2. Clicar em "sign-up"
  3. Preencher os campos "user" e "password"
  4. Clicar em "sign-up"
- **Resultado Esperado:** Usuário cadastrado
- **Resultado Obtido:** Mensagem de erro: "This user already exist."
  - **Observação:** O sistema retorna "This user already exist." mesmo para usuários nunca cadastrados, indicando possível bug no backend.
  - ![Erro de cadastro](../images/tc001-cadastro-erro.jpeg)
- **Status:** Reprovado

### TC002 – Adicionar produtos ao carrinho
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Acessar a página inicial
  2. Selecionar um produto
  3. Clicar em "add to cart"
- **Resultado Esperado:** Produto adicionado ao carrinho 
- **Resultado Obtido:** Produto adicionado ao carrinho
    ![Produto adicionado](../images/tc002-carrinho-sucesso.jpeg)
- **Status:** Aprovado

### TC003 – Finalizar compra com dados válidos
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Acessar a página inicial
  2. Selecionar um produto
  3. Clicar em "add to cart"
  4. Clicar em "cart"
  5. Clicar em "place order"
  6. Preencher os dados dos campos
  7. Clicar em "purchase"
- **Resultado Esperado:** Compra/pedido realizado(a)
- **Resultado Obtido:** Compra realizada
    ![Compra efetuada](../images/tc003-compra-sucesso.jpeg)
- **Status:** Aprovado

### TC004 – Remover produto do carrinho
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Acessar a página inicial
  2. Selecionar um produto
  3. Clicar em "add to cart"
  4. Clicar em "cart"
  5. Clicar em "delete"
- **Resultado Esperado:** Produto deletado do carrinho
- **Resultado Obtido:** Produto deletado do carrinho
- **Status:** Aprovado

### TC005 – Testar botões da barra superior de navegação do site
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Clicar em cada funcionalidade por vez: "home"; "contact"; "about us"; "cart"; "login" e "sign-up"
- **Resultado Esperado:** Abrir cada modal sem erros
- **Resultado Obtido:** Cada modal abriu sem erros
- **Status:** Aprovado

### TC006 – Testar botões das categorias
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Clicar em cada funcionalidade por vez: "phones"; "laptops" e "monitors"
- **Resultado Esperado:** Filtrar cada categoria selecionada
- **Resultado Obtido:** Cada categoria foi filtrada corretamente
- **Status:** Aprovado  

---

## 🔹 Testes de Validação de Campo

### TC007 – Finalizar cadastro com campos vazios
- **Pré-condições:** Acesso a página de cadastro
- **Passos:**
  1. Clicar em "sign-up" na barra superior
  2. Deixar um ou os dois campos em branco
  3. Clicar em "sign-up"
- **Resultado Esperado:** Mensagem de erro
- **Resultado Obtido:** Mensagem de erro:"Please fill out Username and Password." 
- **Status:** Aprovado

### TC008 – Finalizar compra com campos vazios
- **Pré-condições:** Produto no carrinho
- **Passos:**
  1. Clicar em "place order"
  2. Deixar os campos de "name" ou "credit card" vazios
  3. Clicar em "purchase"
- **Resultado Esperado:** Mensagem de erro
- **Resultado Obtido:** Mensagem de erro:"Please fill out Name and Creditcard." 
- **Status:** Aprovado

---

## 🔹 Testes Exploratórios

### TC009 – Navegação livre pelo site
- **Pré-condições:** Site disponível
- **Passos:**
  1. Acessar o site
  2. Clicar em botões de navegação e de seleção
  3. Abrir e fechar modais da barra superior de navegação
- **Resultado Esperado:** Funcionalidades sem quebras e erros
- **Resultado Obtido:** Todas as funcionalidades funcionaram corretamente
- **Status:** Aprovado

### TC010 – Testar Fluxo de contato
- **Pré-condições:** Acessar o site
- **Passos:**
  1. Clicar em contact
  2. Preencher campos de validação
  3. Clicar em send message
- **Resultado Esperado:** Mensagem enviada
- **Resultado Obtido:** Mensagem enviada com sucesso: "Thanks for the message!!"
     ![Contato com sucesso](../images/tc010-contato-sucesso.jpeg)
- **Status:** Aprovado

## 🔹 Testes de Usabilidade

### TC011 – Testar em dispositivo mobile
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Acessar o site em tela reduzida ou em um dispositivo mobile
  2. Navegar pelo site
- **Resultado Esperado:** Layout e funcionalidades adaptadas
- **Resultado Obtido:** Layout e funcionalidades foram adaptados
- **Status:** Aprovado

### TC012 – Testar tempo de resposta do site
- **Pré-condições:** Acesso ao site
- **Passos:**
  1. Acessar a página inicial
  2. Navegar entre categorias e produtos
  3. Realizar ações como login, cadastro e compra
- **Resultado Esperado:** Resposta rápida (até 2 segundos por ação)
- **Resultado Obtido:** Resposta lenta em alguns momentos (5–10 segundos), mas não constante
- **Observações:** Lentidão perceptível, porém variável conforme o momento de acesso
- **Status:** ⚠️ Observação


## 📊 Resumo dos Casos de Teste

| ID     | Descrição                               | Tipo               | Status     |
|--------|-----------------------------------------|--------------------|------------|
| TC001  | Realizar cadastro de usuário            | Funcional          | ❌ Reprovado |
| TC002  | Adicionar produtos ao carrinho          | Funcional          | ✅ Aprovado  |
| TC003  | Finalizar compra com dados válidos      | Funcional          | ✅ Aprovado  |
| TC004  | Remover produto do carrinho             | Funcional          | ✅ Aprovado  |
| TC005  | Testar botões da barra superior         | Funcional          | ✅ Aprovado  |
| TC006  | Testar botões das categorias            | Funcional          | ✅ Aprovado  |
| TC007  | Finalizar cadastro com campos vazios    | Validação de Campo | ✅ Aprovado  |
| TC008  | Finalizar compra com campos vazios      | Validação de Campo | ✅ Aprovado  |
| TC009  | Navegação livre pelo site               | Exploratórios      | ✅ Aprovado  |
| TC010  | Fluxo de contato                        | Exploratórios      | ✅ Aprovado  |
| TC011  | Testar em dispositivo mobile            | Usabilidade        | ✅ Aprovado  |
| TC012  | Testar tempo de resposta do site        | Usabilidade        | ⚠️ Observação|
