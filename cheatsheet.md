============================================================
           CONCEITOS BÁSICOS DO GIT (CHEATSHEET)
============================================================

1. O QUE É O GIT?
   Um sistema de controle de versão distribuído que rastreia 
   mudanças no código ao longo do tempo através de snapshots.

2. OS 3 ESTADOS DO ARQUIVO:
   - Modified (Modificado): Você alterou o arquivo, mas não salvou.
   - Staged (Preparado): Você marcou o arquivo para ir no próximo commit.
   - Committed (Confirmado): Os dados estão salvos no seu banco de dados local.



3. COMANDOS DE INICIALIZAÇÃO:
```sh
$ git init                  # Inicia um repositório na pasta atual
```
```sh
$ git clone <url>           # Baixa um projeto pronto do servidor
```

4. COMANDOS DE SALVAMENTO (LOCAL):
```sh
git status                # Verifica o que mudou
$ git add <arquivo>         # Adiciona um arquivo específico ao Stage
$ git add .                 # Adiciona TODOS os arquivos ao Stage
$ git commit -m "Mensagem"  # Cria um checkpoint (foto do código)
```

5. COMANDOS DE CONEXÃO (REMOTO):
```
   $ git remote add origin <url> # Conecta sua pasta local ao GitHub
   $ git push origin main        # Envia seu código para a nuvem
   $ git pull origin main        # Baixa as novidades da nuvem
```
6. COMANDOS DE HISTÓRICO:
```
   $ git log --oneline         # Mostra o histórico de forma resumida
   $ git show <commit_id>      # Mostra o que foi alterado em um commit específico
```
============================================================
DICA: Use 'git commit' para salvar pequenas tarefas concluídas.
============================================================