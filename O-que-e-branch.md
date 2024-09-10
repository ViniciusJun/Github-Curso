# Trabalhando com Branches no Git

No Git, **branches** (ramificações) são uma das ferramentas mais importantes para controlar diferentes versões do seu projeto. Elas permitem que você trabalhe em novas funcionalidades, correções de bugs ou qualquer outro tipo de desenvolvimento sem interferir no código principal.

## 1. O que é uma Branch?

Uma **branch** é uma linha separada de desenvolvimento. Por padrão, todo repositório Git tem uma branch principal chamada `master` ou `main`. Quando você cria uma nova branch, ela é uma cópia da branch atual, e todo o trabalho feito nela não afetará as outras branches.

Isso é útil quando você deseja:

- Testar uma nova funcionalidade sem afetar o código principal.
- Trabalhar em paralelo com outros desenvolvedores.
- Manter o histórico do projeto mais organizado.

## 2. Criando uma Nova Branch

Para criar uma nova branch no Git, use o seguinte comando:

```bash
git branch nome-da-branch
```

Exemplo:

```bash
git branch feature-nova
```

Isso criará uma nova branch chamada `feature-nova`, mas você ainda estará na branch atual (geralmente `main` ou `master`).

## 3. Trocando para Outra Branch

Depois de criar uma nova branch, você pode alternar para ela com o comando `checkout`:

```bash
git checkout nome-da-branch
```

Exemplo:

```bash
git checkout feature-nova
```

Agora, você estará na branch `feature-nova`, e todo o trabalho que fizer (commits) será separado da branch principal.

### Dica: Criar e Alternar para uma Nova Branch em Um Comando

Você pode criar e alternar para uma nova branch ao mesmo tempo usando o seguinte comando:

```bash
git checkout -b nome-da-branch
```

Exemplo:

```bash
git checkout -b correção-bug
```

## 4. Listando Branches

Para ver todas as branches existentes no repositório e qual você está usando no momento, execute:

```bash
git branch
```

A branch atual será marcada com um `*`.

Exemplo de saída:

```bash
* main
  feature-nova
  correção-bug
```

## 5. Unindo Branches (Merge)

Depois de trabalhar em uma branch, você pode querer unir seu trabalho de volta à branch principal. Para fazer isso, siga os passos:

1. Primeiro, troque para a branch principal (`main` ou `master`):

   ```bash
   git checkout main
   ```

2. Em seguida, faça o **merge** (união) da branch que você deseja unir:

   ```bash
   git merge nome-da-branch
   ```

Exemplo:

```bash
git merge feature-nova
```

Isso irá mesclar o trabalho da branch `feature-nova` na branch principal.

## 6. Excluindo uma Branch

Após mesclar uma branch, você pode querer excluí-la, pois o trabalho nela já foi concluído. Para excluir uma branch localmente, use:

```bash
git branch -d nome-da-branch
```

Exemplo:

```bash
git branch -d feature-nova
```

Se a branch ainda não foi mesclada, e você deseja forçar a exclusão, use:

```bash
git branch -D nome-da-branch
```

## 7. Exemplo Completo de Workflow com Branches

Aqui está um exemplo de fluxo de trabalho comum usando branches:

1. Crie uma nova branch para uma nova funcionalidade:

   ```bash
   git checkout -b nova-funcionalidade
   ```

2. Faça suas alterações e commits na nova branch:

   ```bash
   git add .
   git commit -m "Adiciona nova funcionalidade"
   ```

3. Troque para a branch principal:

   ```bash
   git checkout main
   ```

4. Faça o merge da branch nova-funcionalidade na branch principal:

   ```bash
   git merge nova-funcionalidade
   ```

5. Exclua a branch antiga:

   ```bash
   git branch -d nova-funcionalidade
   ```

## Conclusão

Branches são uma maneira poderosa de organizar seu fluxo de trabalho, especialmente em projetos colaborativos. Elas permitem que você trabalhe em múltiplas funcionalidades simultaneamente sem causar conflitos no código principal.

---

Esse arquivo oferece uma introdução clara e objetiva ao uso de branches no Git.