# React Auth0 Login App

Este é um projeto simples de autenticação utilizando **Auth0** em um aplicativo React criado com Vite.

## 📌 Funcionalidades
- Login e logout com Auth0
- Exibição do perfil do usuário autenticado
- Proteção de rotas com autenticação

## 🚀 Tecnologias Utilizadas
- React
- Vite
- Auth0 React SDK

## 📂 Estrutura do Projeto
```
📁 src
 ┣ 📂 components
 ┃ ┣ 📜 LoginButton.jsx
 ┃ ┣ 📜 LogoutButton.jsx
 ┃ ┗ 📜 Profile.jsx
 ┣ 📜 App.jsx
 ┣ 📜 index.css
 ┣ 📜 main.jsx
 ┗ 📜 App.css
```

## ⚡ Como Rodar o Projeto

### 1️⃣ **Clone o repositório**
```sh
  git clone https://github.com/mandis-ncs/login-react-0auth.git
 cd login-react-0auth
```

### 2️⃣ **Instale as dependências**
```sh
 npm install
```

### 3️⃣ **Criar uma conta no Auth0**
Se ainda não possui uma conta, acesse [Auth0](https://auth0.com/) e crie uma conta gratuita.

### 4️⃣ **Criar uma nova aplicação no Auth0**
1. Acesse o painel do Auth0.
2. Vá para **Applications > Create Application**.
3. Defina um nome para sua aplicação.
4. Selecione **Single Page Application**.
5. Escolha **React** como tecnologia principal.
6. Clique em **Create**.

### 5️⃣ **Adicionar métodos de login adicionais**
1. No menu lateral, vá para **Authentication > Social**.
2. Adicione novas conexões como **LinkedIn** e **GitHub**.
3. Ative as conexões na aplicação criada.

### 6️⃣ **Configuração do Auth0**
Crie um arquivo **.env** na raiz do projeto e adicione as variáveis de ambiente:

```sh
VITE_AUTH0_DOMAIN=seu_dominio_auth0
VITE_AUTH0_CLIENT_ID=seu_client_id_auth0
```

Substitua `seu_dominio_auth0` e `seu_client_id_auth0` pelos valores obtidos no [Auth0 Dashboard](https://auth0.com/).

### 7️⃣ **Configurar URLs no Auth0**
1. Vá para a **aplicação criada** no Auth0.
2. Acesse a aba **Settings**.
3. Adicione `http://localhost:5173/` nos seguintes campos:
   - **Allowed Callback URLs**
   - **Allowed Logout URLs**
   - **Allowed Web Origins**
4. Clique em **Save Changes**.

### 8️⃣ **Execute o projeto**
```sh
 npm run dev
```

## 🛠 Componentes

### 🔹 `LoginButton.jsx`
Componente que exibe um botão para login com **Auth0**.

### 🔹 `LogoutButton.jsx`
Componente que exibe um botão para logout.

### 🔹 `Profile.jsx`
Exibe os detalhes do usuário autenticado, incluindo a foto de perfil, nome e outras informações retornadas pelo Auth0.

## 📜 Licença
Este projeto é distribuído sob a licença MIT.

---
💡 **Dica:** Caso queira proteger rotas, utilize o hook `useAuth0` e valide a autenticação antes de renderizar componentes.

```jsx
const { isAuthenticated } = useAuth0();

return isAuthenticated ? <ProtectedComponent /> : <LoginButton />;
```

