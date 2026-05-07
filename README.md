# PBIRepoTest

## Estrutura

- `src/`: projetos Power BI em formato PBIP
- `notebooks/`: análises exploratórias
- `docs/`: documentação de modelagem, DAX e publicação

## Como abrir e trabalhar no projeto

Siga este fluxo sempre que for realizar alterações no relatório ou no modelo semântico.

### 1. Atualizar a branch `develop`

Antes de iniciar qualquer alteração, atualize sua branch `develop` local:

```bash
git switch develop
git pull origin develop
```

### 2. Criar uma branch de trabalho

Crie uma nova branch a partir da `develop`:

```bash
git switch -c feature/nome-da-alteracao
```

Exemplos de nomes de branch:

```text
feature/ajuste-layout-dashboard
feature/nova-medida-dax
feature/correcao-modelagem
```

### 3. Abrir o projeto no Power BI Desktop

Abra o arquivo `.pbip` no Power BI Desktop.

### 4. Realizar as modificações

Faça as alterações necessárias no relatório, como:

- criação ou ajuste de páginas;
- alterações em visuais;
- criação ou alteração de medidas DAX;
- ajustes no modelo semântico;
- alterações em relacionamentos, tabelas ou configurações.

### 5. Salvar o projeto

Após finalizar as alterações, salve o projeto no formato `.pbip`.

### 6. Verificar as mudanças

Verifique as alterações no VS Code ou pelo terminal:

```bash
git status
git diff
```

### 7. Fazer o commit das alterações

Adicione os arquivos modificados e crie um commit com uma descrição objetiva:

```bash
git add .
git commit -m "Descrição objetiva da alteração"
```

Exemplo:

```bash
git commit -m "Update Amazon dashboard visuals"
```

Também é possível fazer o commit pela interface do VS Code.

### 8. Atualizar sua branch com a `develop`

Antes de finalizar sua entrega, atualize novamente a `develop` e faça o merge dela na sua branch:

```bash
git switch develop
git pull origin develop
git switch feature/nome-da-alteracao
git merge develop
```

Caso existam conflitos, resolva os conflitos, salve os arquivos corrigidos e faça um novo commit:

```bash
git add .
git commit -m "Resolve merge conflicts with develop"
```

Depois disso, abra novamente o arquivo `.pbip` no Power BI Desktop e valide se o projeto está funcionando corretamente.

### 9. Enviar sua branch para o GitHub

Envie sua branch para o repositório remoto:

```bash
git push origin feature/nome-da-alteracao
```

Também é possível fazer o push pela interface do VS Code.

### 10. Abrir um Pull Request

No GitHub, abra um Pull Request da sua branch para a `develop`:

```text
base: develop
compare: feature/nome-da-alteracao
```

### 11. Fazer o merge na `develop`

Após revisão e validação das alterações, faça o merge da sua branch na `develop`.

> A branch `main` deve conter apenas versões estáveis e validadas do projeto. Todas as alterações devem passar primeiro pela branch `develop`.

## Padrão de branches

- `main`: versão publicada, estável e final.
- `develop`: branch de integração.
- `feature/nome-da-alteracao`: novas páginas, medidas, ajustes de modelo ou melhorias.
- `hotfix/nome-do-ajuste`: correções urgentes.

## Boas práticas

- Criar Pull Request para alterações em medidas, modelo ou páginas principais.
- Descrever mudanças visuais com prints quando necessário.
- Evitar versionar dados reais.
- Documentar medidas DAX relevantes em `docs/medidas-dax.md`.