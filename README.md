# Guia Rápido de Uso do Git e GitHub

Este guia fornece uma visão geral das etapas essenciais para configurar e utilizar o Git e o GitHub. Siga estas instruções para clonar repositórios, fazer alterações e sincronizar suas mudanças.

## Configuração da Conta

Antes de começar, é necessário configurar o Git com seu nome de usuário e e-mail. Estes serão utilizados em seus commits.

### Configurando o Nome de Usuário e o E-mail

```sh
git config --global user.name "Seu Nome de Usuário"
git config --global user.email "seu-email@example.com"
````
> Nota: Utilize --global para aplicar essas configurações a todos os repositórios no seu computador. Se não utilizar --global, a configuração será específica para o repositório atual.

### Clonando um Repositório
Para clonar um repositório do GitHub para sua máquina local, use o comando git clone:

```sh
git clone https://github.com/usuario/repositorio.git
```
Substitua https://github.com/usuario/repositorio.git pelo URL do repositório que deseja clonar.

### Sincronizando com o Repositório Remoto
Para garantir que seu repositório local esteja atualizado com as mudanças do repositório remoto, execute:

```sh
git pull
```
*Este comando irá buscar e integrar as mudanças do repositório remoto no seu repositório local.*

### Adicionando e Confirmando Arquivos
Após fazer alterações nos arquivos, você precisa adicioná-los à área de preparação e confirmar essas alterações.

### Adicionando Arquivos
Para adicionar todos os arquivos modificados, use:

```sh
git add --all
```

> Ou, se quiser adicionar arquivos específicos, substitua nome_do_arquivo pelo caminho do arquivo:

```sh
git add nome_do_arquivo
Confirmando as Alterações

```
> Para confirmar as mudanças adicionadas, use o comando git commit com uma mensagem descritiva:

```sh

git commit -m "Descrição clara do que foi alterado"
```
### Enviando Mudanças para o Repositório Remoto
Depois de confirmar suas alterações, envie-as para o repositório remoto com o comando git push:
```sh
git push origin main
```
> Substitua main pelo nome da branch que você está atualizando, se for diferente.

### Resolução de Problemas
Se você encontrar erros durante git pull ou git push, as mensagens de erro geralmente fornecem informações úteis. Verifique o log de erros e consulte a documentação oficial do Git ou busque ajuda online se necessário.


