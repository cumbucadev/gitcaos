# Tarefa 2

1. [Dê uma Estrela no Repositório ⭐](#1-dê-uma-estrela-no-repositório-)
2. [Encontre uma Issue para Trabalhar 🔍](#2-encontre-uma-issue-para-trabalhar-)
3. [Volte para o Branch Main 🎋](#3-volte-para-o-branch-main-)
4. [Atualize o Branch Main 🎋](#4-atualize-o-branch-main-)
5. [Crie um Novo Branch 🎋](#5-crie-um-novo-branch-)
6. [Faça suas Alterações 🔨](#6-faça-suas-alterações-)
7. [Adicione suas Alterações ➕](#7-adicione-suas-alterações-)
8. [Faça um Commit de suas Alterações ✅](#8-faça-um-commit-de-suas-alterações-)
9. [Faça um Push de suas Alterações 🤞](#9-faça-um-push-de-suas-alterações-)
10. [Crie um Pull Request (PR) no GitHub 💬](#10-crie-um-pull-request-pr-no-github-)

## 1. Dê uma Estrela no Repositório ⭐

Antes de começar a trabalhar na sua segunda tarefa, é necessário dar uma estrela no repositório do GitHub. 
Dar uma estrela não apenas demonstra seu apoio ao projeto, mas também cria uma notificação para você sempre que houver atualizações ou atividades. Veja como fazer isso:

1. Acesse o Repositório: Navegue até a página principal do projeto no GitHub: <https://github.com/cumbucadev/gitcaos>
1. Clique no Botão de Estrela: Procure o botão Estrela localizado no canto superior direito da página, logo abaixo do nome do repositório. Clique nele!

## 2. Encontre uma Issue para Trabalhar 🔍

Agora é hora de encontrar uma issue (tarefa ou problema) para trabalhar. Esse é um passo importante e comum no mundo do open source, onde colaboramos para melhorar projetos e aprender juntos. No GitCaos 🔥, usamos as issues para organizar as atividades do projeto. Isso pode incluir corrigir bugs, adicionar novas funcionalidades e melhorar a documentação.

Siga estas etapas simples para encontrar sua primeira issue:

1. Acesse o Repositório: Navegue até a página principal do projeto no GitHub: <https://github.com/cumbucadev/gitcaos>
2. Na parte superior da página do repositório principal, você verá várias abas. Clique na aba chamada Issues. Aqui, você encontrará uma lista de tarefas disponíveis que precisam de ajuda. 
3. Procure pela issue específica: Agora, você precisa encontrar uma issue com o título: # Tarefa 2: O Jogo do Tigrinho me deu (seu-username). Essa tarefa foi criada especialmente para você, e é uma ótima oportunidade para praticar. 
4. Verifique se a issue já está designada para alguém: Olhe ao lado do título da issue para ver se ela já tem alguém designado (chamado de assignee). Se o seu nome já estiver lá, ótimo! Isso significa que você está pronto para trabalhar na tarefa. Se não estiver, você pode pedir para ser designado. Para isso, deixe um comentário na issue dizendo algo como: "Oi, eu gostaria de trabalhar nessa tarefa! Você pode me designar?". Isso garante que nunca mais de uma pessoa trabalhe na mesma issue, evitando conflitos e confusões no desenvolvimento. 
5. Leia atentamente as instruções: Antes de começar a trabalhar, é fundamental ler todas as instruções que estão na issue. Isso vai garantir que você entenda o que é solicitado e que siga as diretrizes corretamente. Preste atenção a detalhes como formato de arquivo, informações que devem ser incluídas e qualquer outro requisito.

Importante: Quando você deu uma estrela no repositório, isso criou automaticamente uma issue para você. Essa é uma forma didática de ajudar novos colaboradores a encontrar uma tarefa prática e se familiarizar com o processo. Normalmente, você encontrará outras tarefas disponíveis que também precisarão de ajuda.

## 3. Volte para o Branch Main 🎋

```sh
git checkout main
```

## 4. Atualize o Branch Main 🎋

```sh
git pull
```

## 5. Crie um Novo Branch 🎋

Antes de começar a trabalhar nas suas alterações, você precisa criar um novo branch. Um branch é uma linha de desenvolvimento independente, onde você pode fazer mudanças sem afetar o código que está na branch principal (geralmente chamada de `main` ou `master`).

1. **Abra o terminal** no seu computador.
2. **Navegue até a pasta do seu projeto GitCaos**. Use o comando `cd caminho/do/seu/projeto` para acessar a pasta correta.
3. **Verifique o estado atual do seu repositório** com o comando:

   ```bash
   git status
   ```

   Você verá algo como:

   ```bash
   On branch main
   Your branch is up to date with 'origin/main'.

   nothing to commit, working tree clean
   ```

4. **Identifique o número da issue**. Como você já tem o link da issue, o número estará no final da URL. Por exemplo, se a URL da issue for `https://github.com/cumbucadev/gitcaos/issues/12`, o número da issue é **12**.
5. **Crie um novo branch** usando apenas o número da issue:

   ```bash
   git checkout -b 12
   ```

6. **Verifique o estado do repositório** após a criação do branch com:

   ```bash
   git status
   ```

   O resultado deve ser semelhante a:

   ```bash
   On branch 12
   Switched to a new branch '12'

   nothing to commit, working tree clean
   ```

## 6. Faça suas Alterações 🔨

Agora que você está no seu novo branch, é hora de fazer as alterações necessárias no código ou na documentação. **As alterações devem ser feitas seguindo as instruções que estão especificadas na issue que você está resolvendo**.

1. **Abra o projeto em um editor de texto ou IDE**.
2. **Siga as instruções da issue**.

Após realizar as modificações, você pode continuar para o próximo passo.

## 7. Adicione suas Alterações ➕

Depois de fazer as alterações, você precisa adicioná-las ao seu branch. Isso informa ao Git quais alterações você deseja incluir no próximo commit.

1. **Verifique o estado do seu repositório** com:

   ```bash
   git status
   ```

   O resultado mostrará que o arquivo foi modificado, algo como:

   ```bash
   On branch 12
   Changes not staged for commit:
   modified:   seu-username.txt
   ```

2. **Adicione suas alterações** usando o comando:

   ```bash
   git add .
   ```

3. **Verifique novamente o estado do repositório** com:

   ```bash
   git status
   ```

   O resultado agora mostrará que o arquivo foi adicionado:

   ```bash
   On branch 12
   Changes to be committed:
   new file:   seu-username.txt
   ```

## 8. Faça um Commit de suas Alterações ✅

Agora é hora de salvar suas alterações no histórico do Git. Para isso, você deve "commitar" suas alterações.

1. **Realize o commit** com o seguinte comando:
   (Substitua `seu-username` pelo seu nome de usuário do GitHub. Essa mensagem ajuda outros a entenderem rapidamente o que foi alterado.)

   ```bash
   git commit -m "Novo arquivo: seu-username.txt"
   ```

Depois de realizar o commit, suas alterações estão salvas no histórico do Git, prontas para serem enviadas para o seu repositório no GitHub.

## 9. Faça um Push de suas Alterações 🤞

Depois de realizar o **commit** das suas alterações, é hora de enviá-las para o repositório remoto no GitHub. Esse processo é chamado de **push**.

1. **Abra o terminal** (ou o prompt de comando).
2. **Navegue até o diretório do seu projeto** se você ainda não estiver lá:

   ```bash
   cd caminho/para/seu/projeto
   ```

3. **Execute o comando de push** para o branch específico (substitua `12` pelo nome do branch que você criou):

   ```bash
   git push origin 12
   ```

## 10. Crie um Pull Request (PR) no GitHub 💬

Após fazer o commit, você precisa criar um Pull Request (PR) para que suas alterações possam ser revisadas e eventualmente mescladas à branch principal. **Lembre-se de que você deve fazer isso no seu fork do repositório GitCaos.**

1. **Acesse o GitHub** e vá até o seu repositório forkado do GitCaos.
2. **Localize o branch que você acabou de criar**. Você verá uma opção para criar um Pull Request.
3. **Clique em "Compare & pull request"**.
4. **Preencha o título e a descrição do PR**:
   - **Título**: "Tarefa 2: Tarefa2: Jogo do tigrinho - seu-username" (substitua `seu-username` pelo seu nome de usuário).
   - **Descrição**:
     (Substitua `15` pelo número da issue que você está resolvendo, que pode ser encontrado no final da URL da issue.)

     ```bash
     Tarefa 2:
     - Tarefa 2: Tarefa2: Jogo do tigrinho - seu-username adicionado

     Closes #15
     ```

5. **Clique em "Create pull request" para finalizar.**

Pronto! Agora sua contribuição será revisada por outros colaboradores do projeto GitCaos.

Ações:

- [< Voltar para Tarefa 1](/docs/tarefa1.md)
