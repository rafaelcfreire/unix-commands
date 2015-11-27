<img
  src="../img/bash-shellshock.png"
  width="100"
  align="right"
/>

# Comandos Unix Úteis
Você também pode ler a versão em [Inglês](../README.md).

## Sobre
> Caso você esteja iniciando com comandos bash e não é tão familiar com alguns destes comandos, este repositório tem o objetivo de lhe ajudar. Caso saiba de algum comando que não esteja aqui ou de algo que possa ser melhor explicado fique à vontade para fazer um <i>fork</i> e um <i>pull request</i>. *

## Tabela de Conteúdo
* [Atalho para o Diretório Home (~)](#atalho-para-o-diretório-home)
* [Diretório Corrente de Trabalho (pwd)](#diretório-corrente-de-trabalho)
* [Listando Arquivos (ls)](#listando-arquivos)
* [Link (ln)](#link)

#### Atalho para o Diretório Home (~)
Em sistemas Unix, você pode referenciar seu diretório a partir de qualquer pasta que esteja apenas digitando o caracter til(~). Caso você teste digitar ~ no seu terminal, você terá a seguinte mensagem:

```sh
$ ~
-bash: /Users/rafaelcfreire: is a directory
```

#### Diretório Corrente de Trabalho (pwd)
Este comando imprime o local aonde você está em qualquer momento no seu sistema de arquivos. Vá para um diretório específico e digite <i>pwd</i> em seu terminal:

```sh
$ pwd
/Users/rafaelcfreire/github/unix-commands
```

#### Listando Arquivos (ls)
O comando <i>ls</i> mostra os arquivos e diretórios que estão abaixo do diretório corrente por padrão, caso queira ver de diretórios diferentes apenas especifique tal endereço como mostrado a seguir.

Lista o diretório corrente
```sh
$ ls
```

Lista o diretório <i>files</i>
```sh
$ ls /home/personal/files
```

A sintaxe do comando <i>ls</i> é:
```sh
ls [options] [names]
```

E caso queira compreender melhor os parametros para <i>options</i>, uma lista está disponível [aqui](http://www.techonthenet.com/unix/basic/ls.php)

#### Link (ln)
Cria links para arquivos ou pastas de forma a evitar duplicação de recursos no sistema de arquivos. Existem dois tipos de links: Hard Links e links simbolicos

##### Hard Links
<i>Hard link</i> é a opção padrão para o comando <i>ln</i> e funciona apenas para arquivos, não para diretórios. Ele cria uma cópia física e idêntica do recurso referenciado no disco. Toda vez que a fonte muda, sua cópia muda tambem.
Note que em caso de apagar a fonte, a cópia permanece viva como um arquivo independente. No exemplo seguinte, um arquivo chamado <i>localReadMe.md</i> é criado na pasta corrente com o mesmo conteúdo de <i>bin/resources/README.md</i>.

```sh
$ ln bin/resources/README.md localReadMe.md
```
##### Link Simbólico

#### Creating Directories (mkdir)

#### Copying files and directories (cp)