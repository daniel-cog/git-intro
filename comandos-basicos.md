# Comandos básicos

1. **`git config`**: Configura sua identidade de usuário para uso em cada commit. Por exemplo:
    ```bash
    $ git config --global user.name "Seu Nome"
    $ git config --global user.email "seu@email.com"
    ```

2. **`git init`**: Cria um novo repositório Git. Por exemplo:
    ```bash
    $ git init
    ```

3. **`git clone`**: Cria uma cópia exata de um repositório existente. Por exemplo:
    ```bash
    $ git clone <URL_do_seu_projeto>
    ```

4. **`git add`**: Adiciona arquivos ao repositório. Você pode adicionar arquivos específicos ou todos os arquivos modificados. Exemplos:
    ```bash
    $ git add seu_arquivo  # Adiciona um arquivo específico
    $ git add *            # Adiciona todos os arquivos novos e/ou modificados
    ```

5. **`git commit`**: Registra as alterações no repositório. Primeiro, use `git add` para adicionar os arquivos à fila de commits e, em seguida, execute o commit. Exemplo:
    ```bash
    $ git commit -m "Mensagem sobre as alterações"
    ```

6. **`git status`**: Exibe o estado atual do repositório.

7. **`git branch`**: Gerencia ramificações (branches). Exemplos:
    ```bash
    $ git branch            # Lista todas as ramificações
    $ git branch <nome_do_branch>  # Cria um novo branch
    $ git branch -d <nome_do_branch>  # Deleta um branch
    ```

8. **`git checkout`**: Troca de uma ramificação para outra. Exemplo:
    ```bash
    $ git checkout <nome_do_branch>
    ```

9. **`git push`**: Envia as alterações locais para o repositório remoto. Exemplo:
    ```bash
    $ git push origin main
    ```

10. **`git log`**: Exibe o histórico de commits. Por exemplo:
    ```bash
    $ git log
    ```

11. **`git pull`**: Atualiza seu repositório local com as alterações do repositório remoto. Exemplo:
    ```bash
    $ git pull origin main
    ```

12. **`git merge`**: Combina alterações de uma ramificação para outra. Por exemplo:
    ```bash
    $ git checkout main  # Troque para a ramificação principal
    $ git merge <nome_do_branch>  # Mescla as alterações do branch especificado
    ```

13. **`git reset`**: Desfaz alterações no repositório. Exemplo:
    ```bash
    $ git reset HEAD seu_arquivo  # Remove o arquivo da fila de commits
    ```

14. **`git stash`**: Armazena alterações temporariamente. Útil quando você deseja alternar de ramificação sem fazer commit das alterações atuais. Exemplo:
    ```bash
    $ git stash save "Minhas alterações"
    ```

15. **`git remote`**: Gerencia repositórios remotos. Exemplos:
    ```bash
    $ git remote -v  # Lista os repositórios remotos configurados
    $ git remote add <nome_do_repositorio> <URL_do_repositorio>  # Adiciona um novo repositório remoto
    ```
