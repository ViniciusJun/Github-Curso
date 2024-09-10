Aqui está o conteúdo para o arquivo `.md` explicando como configurar o nome de usuário e o e-mail de forma global no Git usando o Git Bash:

---

# Configurando Nome de Usuário e E-mail no Git Bash

Para começar a versionar seus projetos com Git, é necessário configurar o seu nome de usuário e e-mail. Essas informações são importantes porque ficam associadas a cada commit que você fizer no repositório. 

Aqui está o passo a passo para configurar o nome de usuário e o e-mail de forma global, ou seja, essas configurações serão aplicadas para todos os repositórios em seu computador.

## 1. Abrir o Git Bash

Primeiramente, abra o **Git Bash** em seu computador. Você pode fazer isso clicando com o botão direito do mouse na área de trabalho ou em uma pasta e selecionando _Git Bash Here_, ou procurando diretamente pelo Git Bash no seu sistema.

## 2. Definir o Nome de Usuário

Use o comando abaixo para configurar seu nome de usuário globalmente. Substitua `"Seu Nome"` pelo nome que deseja usar:

```bash
git config --global user.name "Seu Nome"
```

Exemplo:

```bash
git config --global user.name "João Silva"
```

Esse comando define o nome que será exibido em todos os commits que você fizer.

## 3. Definir o E-mail

Agora, configure seu e-mail utilizando o comando abaixo. Substitua `"seu-email@example.com"` pelo e-mail que você deseja usar:

```bash
git config --global user.email "seu-email@example.com"
```

Exemplo:

```bash
git config --global user.email "joao.silva@example.com"
```

Este e-mail também ficará associado a todos os commits que você fizer.

## 4. Verificar Configurações

Para verificar se as configurações foram aplicadas corretamente, você pode rodar o seguinte comando no Git Bash:

```bash
git config --global --list
```

Esse comando exibirá o nome de usuário e o e-mail que foram configurados, além de outras configurações globais do Git.

## Considerações Finais

As configurações de nome e e-mail feitas de forma global serão aplicadas a todos os repositórios no seu computador. Se você quiser configurar um nome e e-mail diferentes para um repositório específico, basta rodar os comandos **sem a opção `--global`** dentro da pasta do repositório.

Exemplo para repositório específico:

```bash
git config user.name "Outro Nome"
git config user.email "outro-email@example.com"
```

Agora seu Git está configurado corretamente e pronto para ser usado!
