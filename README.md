# PBIRepoTest

## Estrutura

- `src/`: projetos Power BI em formato PBIP
- `notebooks/`: análises exploratórias
- `docs/`: documentação de modelagem, DAX e publicação

## Como abrir o projeto

1. Criar uma branch com base na develop
2. Abrir o arquivo `.pbip` no Power BI Desktop.
3. Fazer as modificações
4. Salvar em .pbip
5. Verificar as mudanças no vscode
6. Fazer o commit
7. Quando finalizar suas mudanças fazer o pull para develop

## Padrão de branches

- `main`: versão publicada ou estável. final.
- `develop`: integração
- `feature/nome-da-alteracao`: novas páginas, medidas, ajustes de modelo
- `hotfix/nome-do-ajuste`: correções urgentes

## Boas práticas

- Criar PR para alterações em medidas, modelo ou páginas principais.
- Descrever mudanças visuais com prints quando necessário.
- Evitar versionar dados reais.
- Documentar medidas DAX relevantes em `docs/medidas-dax.md`.