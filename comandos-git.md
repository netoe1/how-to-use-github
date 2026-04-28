# Comandos Git: Clonando um Repositório

Para clonar um repositório do GitHub para sua máquina local, use o comando git clone:

```sh
git clone https://github.com/usuario/repositorio.git
```

Substitua https://github.com/usuario/repositorio.git pelo URL do repositório que deseja clonar.
Quando se clona um repositório e ele seja de sua própria autoria, você consegue modificar seu conteúdo e atualizá-lo ao repositório remoto. Se é de outra pessoa, você pode ter uma cópia para você, através do Fork.




# Comandos Git: Sincronizando com o Repositório Remoto

Para garantir que seu repositório local esteja atualizado com as mudanças do repositório remoto, execute:

```sh
git pull
```

_Este comando irá buscar e integrar as mudanças do repositório remoto no seu repositório local._

# Comandos Git: Adicionando e Confirmando Arquivos

Após fazer alterações nos arquivos, você precisa adicioná-los à área de preparação e confirmar essas alterações.

## Comandos Git: Adicionando Arquivos

Para adicionar todos os arquivos modificados, use:

```sh
git add --all
```

Ou, se quiser adicionar arquivos específicos, substitua nome_do_arquivo pelo caminho do arquivo:
Quando você usar --all, o Git é inteligente e consegue saber quais arquivos foram modificados...

```sh
git add nome_do_arquivo
Confirmando as Alterações

```

Para confirmar as mudanças adicionadas, use o comando git commit com uma mensagem descritiva:

```sh

git commit -m "Descrição clara do que foi alterado"
```

# Comandos Git: Enviando Mudanças para o Repositório Remoto

Depois de confirmar suas alterações, envie-as para o repositório remoto com o comando git push:

```sh
git push origin main
```

Substitua main pelo nome da branch que você está atualizando, se for diferente.

## Comandos Git: Resolução de Problemas

Se você encontrar erros durante git pull ou git push, as mensagens de erro geralmente fornecem informações úteis. Verifique o log de erros e consulte a documentação oficial do Git ou busque ajuda online se necessário.

# Comandos principais para git

# Comandos Git:  Adicionar arquivos para versionamento

```sh
git add <nome_do_arquivo>
```

Normalmente adicionamos todos os arquivos; o git é inteligente e consegue saber quais arquivos mudaram e quais permanecem os mesmos.

## Uso Comum do git add

```sh
git add --all ou git add .
```

# Comandos Git: Trocar de branch para desenvolvimento

```sh
git checkout <nome_da_branch>
```

Este comando permite que você troque entre branch's.

## Comandos Git:  Limpar arquivos do repositório que não estão sendo versionados

```sh
git clean
```

## Comandos Git:  Verificar versões anteriores do projeto

```sh
git log
```

Para sair do log, você deve pressionar _q_ no teclado. O log demonstra muitos aspectos avançados sobre o repositório.

## Comandos Git:  Resetar todas as alterações que não foram "commitadas"

```sh
git reset
```

Use apenas se você cometeu algum erro muito grotesco. Você também usar o git revert para reverter um commit já feito.

## Comandos Git:  Reverter um commit problemático

```sh
git revert
```

## Comandos Git:  Enviar alterações ao repositório remoto

```sh
git push
```

## Comandos Git:  Sincroniza repositório local baixando os dados do remoto.

```sh
git pull
```

Busca os problemas de sincronia, aplicando diretamente no seu repositório. Caso haja algum erro, o git tentará utilizar o processo de Rebase.

## Comandos Git:  Misturar duas branchs diferentes em um só

```sh
git merge
```

## Comandos Git:  Sincronizar repositório local pelo remoto

```sh
git fetch
```

A diferença entre o git fetch e pull, é que o fetch permite ver o histórico do repositório local, enquanto o git pull já altera diretamente.
