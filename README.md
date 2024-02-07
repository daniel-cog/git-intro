# Configurando o Git

1. **Instale o Git**:
   - Baixe e instale a última versão do Git através do Winget pelo Powershell do Windows:
     ```
     winget install --id Git.Git -e --source winget
     ```

2. **Defina seu nome de usuário e endereço de e-mail no Git**:
   - Abra o terminal Git Bash (que você instalou com o Git).
   - Execute os seguintes comandos, substituindo “Seu Nome” e “seu@email.com” pelos seus dados:
     ```
     git config --global user.name "Seu Nome"
     git config --global user.email “seu@email.com”
     ```

3. **Criar e adicionar sua chave SSH ao ssh-agent**:
   - Cole o texto abaixo, substituindo o email usado no exemplo pelo seu endereço de email GitHub:
     ```
     ssh-keygen -t ed25519 -C “seu@email.com”
     ```
   - Quando for solicitado a inserir um arquivo para salvar a chave, pressione Enter para aceitar o local padrão do arquivo.
     ```
     Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM): [Pressione enter]
     ```

4. No prompt, digite uma frase secreta segura ou pressione Enter para manter sem frase secreta.

5. Execute o seguinte comando para iniciar o ssh-agent em segundo plano:
   ```
   eval "$(ssh-agent -s)"
   ```

6. Adicione sua chave privada SSH ao agente ssh:
   ```
   ssh-add c:/Users/YOU/.ssh/id_ed25519
   ```

7. **Adicionar a chave SSH ao Github**:
   - Exiba sua chave pública com o seguinte comando e a copie:
     ```
     cat c:/Users/YOU/.ssh/id_ed25519.pub
     ```
   - Acesse suas configurações no GitHub:
     ```
     Settings > SSH and GPG keys > “New SSH key”
     ```

8. Teste a conexão com o Github com o seguinte comando:
   ```
   ssh -T git@github.com
   ```
