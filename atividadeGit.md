# Git Assignment

**INDIVIDUAL**

**Entrega**: 18-Mar-21

## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

### Entenda o repositorio
Baixe o arquivo [handson.zip] (handson.zip) e descompacte-o
A pasta handson é um repositório git. Usando a linha de comando, altere o diretório para "handson/"

As caixas vazias
```

```
representam o conteúdo que você precisa preencher e postar em seu repositório privado

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
git branch - lista todas as ramificações no repositório local e mostra qual a ramificação atual que está sendo utilizada.
git checkout BRANCH_NAME - troca para ramificação escolhida.
git log --decorate - mostra o histórico de alterações da branch atual.

```

2. Tente usar `git log --graph --all`. O que acontece?
```
Mostra o histórico de alterações de todas as branches

```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
Na branch master e feature-foo existem dois arquivos chamado A.java e B.java, o comando acima mostra:
-ambos tem a classe A, porém somente na branch feature-foo tem conteúdo dentro dessa classe.
-somente a branch master tem a classe B.

```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
git checkout master
git merge feature-foo

```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
(i) git branch math
(ii) git checkout math

```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
git add B.java
git commit -m "comentario"

```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git checkout master
git merge math
Resultado: Aviso de conflito de mesclagem em B.java

```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort

```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
- abrir o arquivo B.java com o comando nano B.java e editei o arquivo mantendo as alterações de ambas as branches, apagando as linhas geradas pelo git. 

```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
- git add B.java
- git commit