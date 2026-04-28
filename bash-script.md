
# Você está em bash-script.sh

Neste arquivo.md, você vai ter acesso ao conteúdos sobre bash script.

## 🚀 Começando
* [Menu Principal](README.md)
* [Git/GitHub](README.md) 
* [Seção sobre Bash Script](docs/bash-script.md)
* [Installation Guide](docs/INSTALLATION.md)
* [Environment Setup](docs/SETUP.md)

## 📖 Guia de uso
* [User Manual](docs/USER_GUIDE.md)
* [Practical Examples](examples/README.md)
* [Frequently Asked Questions (FAQ)](docs/FAQ.md)

## ⚖️ Licenças e uso legal
* [Licença de uso MIT custom](LICENSE.md)

---



# Bash Script / Shell Script

Caso você seja novato em computação ou ainda não está familirizado, irei introduzir o que é um Shell para você; o Shell é um programa e está relacionado diretamente a arquitetura de computadores. O shell comunica, o kernel de um computador (núcleo), responsável por todo o cuidado do hardware, com o software, que se comunica com o ser humano.

## O que podemos retirar de conclusão disso?

> **O Shell é uma ponte entre, o que você instruir o computador, com o que a máquina deve fazer para chegar no que você quer.**

Para isso, as linguagens de Shell Script são geralmente mais abstratas, ou seja, mais parecidas com a linguagem humana, pulando algumas etapas importantes que o programador, se quisesse acesso direto ao Kernel, deveria executar. O Shell permite navegar entre o sistema de arquivos da máquina, podendo realizar configurações do Sistema Operacional e executando funções previamente criadas pelos seus desenvolvedores, onde até, os programas criados possam utilizar (caso queiram).


# Comandos mais usados:

## Bash Script: Como criar uma pasta

Para criar uma pasta, utilizamos o comando mkdir acrescido do nome que você quer utilizar.
```sh
mkdir minhaPasta
```

## Bash Script: Remover Pasta

Para remover, você deve utilizar o comando **rm**.
Cuidado, que o comando rm é **perigoso**, pois, se utilizado de forma errada, pode apagar arquivos que você não deseja.

```sh
rm -rf minhaPasta
```
## Bash Script: Navegar entre pastas
Você pode entrar e sair de pastas. Para isso, existe o comando *cd*.
Quando quiser entrar em uma pasta, digite:

```sh
cd nome_da_pasta
```

-/-/-

Para sair da pasta que você entrou, digite:

```sh
cd ..
```

-/-/-

## Bash Script: Mostrar se o que tem no diretório atual
Você pode digitar **ls**, para mostrar o diretório


```sh
ls
```



Para ordenar o que foi mostrado em uma lista:

```sh
ls -l
```

Para ordenar em ordem alfabética e em lista :
```sh
ls -al
```