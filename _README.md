### Versionamento de software

Exemplo para descrição de versionamento de software.

+ X.Y.Z

    + X: (VERSÃO) número da versão principal
    + Y: (RECURSO) número que indicará um novo recurso adicionado a versão principal
    + Z: (CORREÇÃO) número que indicará as correções de bugs

+ Exemplo
    + Novo aplicativo irá começa com 1.0.0
    + Caso ocorra apenas correções, deverá ser incrementado o valor de correção, ou seja, 1.0.1
    + Se a nova versão contiver novos RECURSOS com ou sem CORREÇÕES de bugs, aumente o número do recurso e redefica o número de CORREÇÃO para ZERO, ou seja, 1.1.0
    + Incrementando o número de VERSÃO
        + Caso o valor do RECURSO seja 9, incremente o número da VERSÃO e redefina o RECURSO e CORREÇÃO para ZERO, ou seja, 2.0.0
        + Uma outra abordagem é quando ocorrem grandes mudanças na aplicação 


### Utilizando o GIT com tags 

#### Inicializando projeto com o Git
```shell
# Iniciando com o GIT
git init

# Definindo URL remota 'origin'
git remote add origin  https://github.com/alexandresvloja/TagGit

# Adicionando todos os arquivos alterados
git add *

# Commit com comentário
git commit -m "Primeiro commit"

# Push
git push origin master

# Definindo Tag inicial
git tag -a v1.0.0 -m "Primeira versão"
```

#### Nova branch para correção de Bug 1
```shell
# Criando nova branch a partir da atual (master)
git checkout -b DEV_Correcao1

# Após alterado o arquivo, será adicionado para o próximo commit
git add *

# Commit com comentário
git commit -m "Corração 1"

# Push
git push origin DEV_Correcao1

# Definindo Tag de correção
git tag -a v1.0.1 -m "Correção referente ao novo do arquivo (exemplo)"
```

#### Nova branch para correção de Bug 2
```shell
# Retornando para branch principal
git checkout master

# Criando nova branch a partir da atual (master)
git checkout -b DEV_Correcao2

# Após alterado o arquivo, será adicionado para o próximo commit
git add *

# Commit com comentário
git commit -m "Corração 2"

# Push
git push origin DEV_Correcao2

# Definindo Tag de correção
git tag -a v1.0.1 -m "Correção referente ao novo do arquivo (exemplo) 2"
```

### Efetuando MERGE com a versão v1.0.1