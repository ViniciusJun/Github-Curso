# Autenticando no GitHub via Token

Com o fim do suporte a autenticação via nome de usuário e senha no GitHub para operações realizadas via Git (como push, pull e clone), agora é necessário utilizar **tokens de acesso pessoal** (Personal Access Tokens - PAT) para realizar a autenticação. Este guia explica como criar um token e usá-lo para autenticar no GitHub.

## 1. Criando um Token de Acesso Pessoal

### Passo 1: Acessar as Configurações do GitHub

1. Faça login em sua conta do GitHub.
2. No canto superior direito, clique no ícone do seu perfil e selecione **Settings** (Configurações).

### Passo 2: Acessar a Configuração de Tokens

1. No menu à esquerda, clique em **Developer settings** (Configurações de desenvolvedor).
2. Na próxima página, selecione **Personal access tokens** (Tokens de acesso pessoal).
3. Clique em **Tokens (classic)** e, em seguida, no botão **Generate new token** (Gerar novo token).

### Passo 3: Gerar o Token

1. Dê um nome ao seu token no campo **Note** para que você saiba para que ele serve.
2. Defina a **data de expiração**. Tokens com expiração são mais seguros.
3. Marque os escopos de permissão que o token terá. Para operações básicas com repositórios, selecione **repo**.
4. Clique no botão **Generate token** para gerar seu token.

### Passo 4: Copiar o Token

1. Assim que o token for gerado, copie-o imediatamente, pois ele não será exibido novamente.
2. Guarde o token em um local seguro, como um gerenciador de senhas.

## 2. Usando o Token no Git

Agora que você criou seu token de acesso pessoal, pode usá-lo no lugar da senha ao se autenticar no Git via Git Bash ou qualquer outra interface Git.

### Autenticando com o Token no Git Bash

Quando você executar um comando que requer autenticação, como `git push` ou `git pull`, o Git pedirá suas credenciais.

1. No campo de **usuário**, insira seu **nome de usuário do GitHub**.
2. No campo de **senha**, insira o **token de acesso pessoal** que você criou (não sua senha de GitHub).

Exemplo:

```bash
git push origin main
Username: seu-usuario
Password: seu-token-aqui
```

### Salvando as Credenciais Localmente

Para não precisar inserir o token em toda operação Git, você pode configurar o Git para salvar suas credenciais em cache localmente. Isso pode ser feito com o seguinte comando:

```bash
git config --global credential.helper cache
```

Esse comando salva as credenciais em cache temporariamente. Para configurar o cache de forma permanente, use:

```bash
git config --global credential.helper store
```

Dessa forma, suas credenciais serão armazenadas permanentemente no sistema.

## 3. Atualizando um Token Expirado

Se seu token expirar ou você precisar de um novo por outro motivo, basta seguir os mesmos passos da seção [Criando um Token de Acesso Pessoal](#1-criando-um-token-de-acesso-pessoal) para gerar um novo token e substituí-lo em suas configurações de autenticação.

## 4. Revogando um Token

Se por algum motivo você precisar revogar um token, siga estes passos:

1. Acesse as configurações de **Developer settings** no GitHub.
2. Vá para **Personal access tokens**.
3. Encontre o token que deseja revogar e clique em **Revoke** (Revogar).

Isso remove o token imediatamente e ele não poderá mais ser usado para autenticação.

## Conclusão

Autenticar no GitHub via token de acesso pessoal é uma maneira segura e eficiente de realizar operações Git. Certifique-se de manter seus tokens seguros e de renovar ou revogar os tokens quando necessário.
