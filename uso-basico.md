# GUIA PRATICO: USO BASICO DO GIT

O Git é um sistema de controle de versao que funciona como uma "maquina do tempo" para o seu codigo. Abaixo estão os comandos essenciais para o dia a dia.

---

## 1. CONFIGURAÇÃO INICIAL:
Execute estes comandos apenas uma vez ao instalar o Git no seu computador.

```sh
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

## 2. COMEÇANDO UM PROJETO:
- git init: Cria um novo repositório Git na pasta atual.
- git clone <url-do-repositorio>: Clona um projeto existente do GitHub para a sua maquina.

---

## 3. O CICLO DE TRABALHO (WORKFLOW):

Passo 1: Verificar o que mudou
```sh
git status
```

Passo 2: Preparar os arquivos (Stage)
```sh
git add .  # Adiciona todas as mudancas$ git add nome-do-arquivo.js # Adiciona apenas um arquivo especifico
```

Passo 3: Salvar a versao (Commit)

```sh
git commit -m "Explicacao curta da alteracao feita"
```
---

## 4. TRABALHANDO COM BRANCHES (RAMOS)
- **git checkout -b nome-da-branch:** Cria uma nova branch e entra nela.
- **git branch:** Lista todas as branches e mostra em qual voce esta.
- **git checkout main:** Volta para a branch principal.
- **git merge nome-da-branch:** Une as alteracoes de uma branch a branch atual.

---

## 5. SINCRONIZANDO COM O SERVIDOR (NUVEM)
- **git push origin main:** Envia seus commits locais para o servidor remoto.
- **git pull:** Puxa as atualizacoes do servidor para o seu computador.

---

## 6. COMANDOS DE CONSULTA
- **git log:** Mostra o historico de commits.
- **git diff:** Mostra as alteracoes exatas dentro das linhas de codigo.

---
Dica: Commit sempre que terminar uma pequena tarefa logica.