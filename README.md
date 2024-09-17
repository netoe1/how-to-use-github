<style>
*{
box-sizing: border-box;
}

.photo-square{
width: 50%;
height: auto;
max-width: fit-content;
max-height: fit-content;
object-fit: cover;
aspect-ratio:1/1;
}

.photo-square-small{
width: 0.8em;
align-self: center;
height: auto;
max-width: fit-content;
max-height: fit-content;
object-fit: cover;
aspect-ratio:1/1;
}

.container-img{
 width: 100%;
    flex-direction:row;
    display:flex;
    align-items:center;
    justify-content: space-evenly;
    gap:5em;
    padding: 2em;

}

.h-with-logo{
display: flex;
align-items:center;
gap: 0.5em;
}
.rounded{
border-radius: 50%;
}

</style>

# Guia Rápido de Uso do Git e GitHub

Este guia fornece uma visão geral das etapas essenciais para configurar e utilizar o Git e o GitHub. Siga estas instruções para clonar repositórios, fazer alterações e sincronizar suas mudanças. Normalmente, para facilitar o uso, o GitHub possui uma versão com interface gráfica, o que auxilia iniciantes a utilizarem da ferramenta.
A intenção deste curso é desenvolver a aptidão do aluno a utilizar o terminal; quando desenvolvida essa aptidão, o estudante pode ter a liberdade de escolher entre uso via CLI ou UI.

**CLI:** Programa de linha de comando, uso em terminal.

**UI:** Programa que utiliza interface gráfica para interagir com o usuário.

# Git x GitHub

Ao primeiro momento, você precisa entender qual é a diferença entre Git e Github.
Primeiramente, **Git** foi uma ferramenta criada pelo criador do Linux, **Linus Torvalds**; é **open source**, e é uma ferramenta de versionamento de software, permitindo ao desenvolvedor, gestoriar, de forma mais efetiva seus projetos.
O Git foi uma ferramenta 100% desenvolvida por Linus, devido aos problemas em gestoriar uma aplicação como o Projeto Linux, possuindo muitos contribuidores.

Porém, já o GitHub, é tipo uma "rede social" onde você armazena esse código remotamente, consegue baixar e modificar o código remoto, utilizando a ferramenta Git. O GitHub é um complemento a tecnologia de versionamento Git, possuindo algumas outras funções.

<h1 class = "h-with-logo">Características do Git <img src = "./img/git.png" class = "photo-square-small"></h1>

- Ferramenta que possibilita versionamento de acesso local;
- É open-source, código livre e considerada uma ferramenta madura no mercado de Tecnologias de Versionamento;
- Permite o gerenciamento das versões, reversão e toda a manipulação necessária para o desenvolvedor.
- É um app seguro, utiliza o protocolo de criptografia SHA-1.
- Tem seu uso variado, dependo do fluxo de trabalho do utilizador.
- Permite que várias pessoas versionem o mesmo software, trabalhando ao mesmo tempo.

# Características do GitHub

- Hospeda os códigos fontes das aplicações versionadas com o Git.
- Parece com uma rede social, possuindo varios modos de integração e compartilhamento de ideias e projetos, entre desenvolvedores.
- Os projetos possuem uma área de discussão, capaz de reportar problemas, pull requests e outras funções.

Com isso dito, podemos afirmar que o Git é uma tecnologia acoplada a plataforma GitHub.

# Linus Torwalds e Git Imagem.

<div class = "container-img">
<img src  = "./img/git.png" class = "photo-square"/> 
<img src  = "./img/linus.webp" class = "photo-square rounded"/> 
</div>

# Conhecimentos Necessários

Para compreender o uso do Git no terminal, primeiro você deve conhecer alguns comandos básicos de Terminal; normalmente, utilizamos Linux como referência; o linguagem Shell padrão para shells no Linux é Bash Script, baseada em linguagem shell, com alguns detalhes. Recomendo fortemente que você tenha a consciência de uso desta ferramenta, pois ela é requisito para entender e executar os passos do git.

# Git Flow

## Configuração da Conta

Antes de começar, é necessário configurar o Git com seu nome de usuário e e-mail. Estes serão utilizados em seus commits.

## Configurando o Nome de Usuário e o E-mail

```sh
git config --global user.name "Seu Nome de Usuário"
git config --global user.email "seu-email@example.com"
```

Nota: Utilize --global para aplicar essas configurações a todos os repositórios no seu computador. Se não utilizar --global, a configuração será específica para o repositório atual. Isso só vai funcionar se você já tiver clonado o repositório.

# Segurança do git

O Git/GitHub utiliza SSH, protocolo que protege o uso do terminal via acesso remoto, além de outras políticas que protegem a conta do usuário. Hoje, o GitHub utiliza Tokens como "chaves mestras". Você pode criá-los para serem absolutos, sem data de validade; ou com data de validade.

Os tokens são requeridos para alterações mais sensíveis em relação aos dados do usuário, quando você quer alterar pelo terminal. Todo o token também possui camadas de permissão; você pode criar um token de permissão para um desenvolvedor do seu projeto, onde ele é apenas capaz de fazer commit, sem atualizar o repositório.

# Configuração de um repositório, sem cloná-lo

```sh
echo "# 23322" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:netoe1/23322.git
git push -u origin main

```

Não recomendo esse método aos iniciantes. Prefiro que você utilize o método de clonagem.

# Estrutura de repositório básico, recomendado pelo próprio git:

Um repositório deve ter um arquivo README.md, escrito na linguagem de hypertexto Markdown, como este arquivo que você está lendo; o arquivo serve para informar aos usuários, o que você está tentando fazer, explicando passo a passo do projeto.
Outra coisa que normalmente você vai criar, é uma pasta chamada _src_, com o seu código fonte.
Lembrando que, depedendo da linguagem e com o que você vai trabalhar, a estrutura de pastas deve mudar.

## Estrutura de repositório: .gitignore

O .gitignore é um arquivo que permite ao programador, informar ao git arquivos que devem ser ignorados, que não vão passar por versionamento.

# Clonando um Repositório

Para clonar um repositório do GitHub para sua máquina local, use o comando git clone:

```sh
git clone https://github.com/usuario/repositorio.git
```

Substitua https://github.com/usuario/repositorio.git pelo URL do repositório que deseja clonar.
Quando se clona um repositório e ele seja de sua própria autoria, você consegue modificar seu conteúdo e atualizá-lo ao repositório remoto. Se é de outra pessoa, você pode ter uma cópia para você, através do Fork.

# Biblioteca de Comandos

### Sincronizando com o Repositório Remoto

Para garantir que seu repositório local esteja atualizado com as mudanças do repositório remoto, execute:

```sh
git pull
```

_Este comando irá buscar e integrar as mudanças do repositório remoto no seu repositório local._

# Adicionando e Confirmando Arquivos

Após fazer alterações nos arquivos, você precisa adicioná-los à área de preparação e confirmar essas alterações.

## Adicionando Arquivos

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

## Enviando Mudanças para o Repositório Remoto

Depois de confirmar suas alterações, envie-as para o repositório remoto com o comando git push:

```sh
git push origin main
```

Substitua main pelo nome da branch que você está atualizando, se for diferente.

## Resolução de Problemas

Se você encontrar erros durante git pull ou git push, as mensagens de erro geralmente fornecem informações úteis. Verifique o log de erros e consulte a documentação oficial do Git ou busque ajuda online se necessário.

# Comandos principais para git

## Adicionar arquivos para versionamento

```sh
git add <nome_do_arquivo>
```

Normalmente adicionamos todos os arquivos; o git é inteligente e consegue saber quais arquivos mudaram e quais permanecem os mesmos.

## Uso Comum do git add

```sh
git add --all ou git add .
```

## Trocar de branch para desenvolvimento

```sh
git checkout <nome_da_branch>
```

Este comando permite que você troque entre branch's.

## Limpar arquivos do repositório que não estão sendo versionados

```sh
git clean
```

## Verificar versões anteriores do projeto

```sh
git log
```

Para sair do log, você deve pressionar _q_ no teclado. O log demonstra muitos aspectos avançados sobre o repositório.

## Resetar todas as alterações que não foram "commitadas"

```sh
git reset
```

Use apenas se você cometeu algum erro muito grotesco. Você também usar o git revert para reverter um commit já feito.

## Reverter um commit problemático

```sh
git revert
```

## Enviar alterações ao repositório remoto

```sh
git push
```

## Sincroniza repositório local baixando os dados do remoto.

```sh
git pull
```

Busca os problemas de sincronia, aplicando diretamente no seu repositório. Caso haja algum erro, o git tentará utilizar o processo de Rebase.

## Misturar duas branchs diferentes em um só

```sh
git merge
```

## Sincronizar repositório local pelo remoto

```sh
git fetch
```

A diferença entre o git fetch e pull, é que o fetch permite ver o histórico do repositório local, enquanto o git pull já altera diretamente.

# Possíveis Problemas com versionamento: Repo local e remoto

No desenvolvimento, é comum ocorrer conflitos entre repositórios. O git oferece ferramentas para você conseguir amenizar o estrago feito.
Caso você já tenha _clonado_ o repositório e esqueça de sincronizá-lo com o remoto, você pode fazer com que o repositório local e remoto fiquem desincronizados. Para evitar este problema, que é bem complicado de resolver nos meios padrões, recomendamos que:

_Toda a vez que você entrar para desenvolver código, procure sincronizar o repositório, com o comando git pull. Após realizar o processo de desenvolvimento, use git push para sincronizar o local com o remoto._

Caso você não tenha feito isso, existe a ferramenta rebase, que permite, de forma interativa, recuperar os estragos.

## Abrir processo de recuperação interativo

```sh
git rebase -i
```

# Sincronização de conta com IDE's

Caso você utilize alguma IDE para programar, como VSCode, Visual Studio Communnity, ou qualquer outra compatível com a tecnologia do Git, você pode sincronizar sua conta, guardando ssuas preferências de usuário; também, sincronizar a conta permite ao usuário não precisar realizar sempre as questões de segurança relacionadas aos uso de tokens.

_Dica de segurança digital:_ Sincronize contas apenas em computadores pessoais, os quais, só você utiliza.

# Documentação original do Git

https://git-scm.com/doc

Na _documentação_, existem todos os detalhes sobre o uso, porém, a quem inicia, pode causar um efeito de excesso de informação.

# Questões autorais

Este repositório aceita contribuições, desde que sejam válidas e verificadas. Em caso de contribuição, é necessário se autoreferenciar e expor o nome do autor principal.
A licensa de uso MIT, se refere ao uso livre à atividades educacionais, porém, caso você queira usar para outros propósitos, use e referencie o dono do repositório.

**Este repositório está em constante construção, podendo haver acréscimo ou decremento de informações.**

## Enjoy, by NEWCORP.team
