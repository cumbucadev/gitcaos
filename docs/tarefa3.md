# É sobre issue e tá tudo bem
## Objetivo 
Destacar a importância das issues e aprender como escreve-las
## Criando a issue

Agora é hora de encontrar uma issue (tarefa ou problema) para trabalhar. Esse é um passo importante e comum no mundo do open source, onde colaboramos para melhorar projetos e aprender juntos. No GitCaos 🔥, usamos as issues para organizar as atividades do projeto. Isso pode incluir corrigir bugs, adicionar novas funcionalidades e melhorar a documentação.

Siga estas etapas simples para encontrar sua primeira issue:

1. Acesse o Repositório: Navegue até a página principal do projeto no GitHub: <https://github.com/cumbucadev/gitcaos>
2. Na parte superior da página do repositório principal, você verá várias abas. Clique na aba chamada Issues. Aqui, você encontrará uma lista de tarefas disponíveis que precisam de ajuda.
3. Clique em New issue

No titulo insira:
 "Tarefa 4: Errei, fui moleque! (username)" 

E, na descrição insira a seguinte tarefa para poder ser atribuída a outro colaborador:
## Tarefa:
Agora é hora de corrigir aquele erro e aprender a reverter um commit. Vamos lá!

## Passo 1: Abra o arquivo

A primeira coisa que você vai fazer é abrir o arquivo que está localizado em
`caos/@username/username.txt`. Esse arquivo foi criado na tarefa 1. Abra-o com o editor de sua preferência (VSCode, PyCharm, Notepad, ou qualquer outro editor).

## Passo 2: Adicionar a primeira linha

Adicione uma linha ao final do arquivo dizendo que você voltou. Alguns exemplos:

- Voltei!
- Vocês não imaginam o prazer que é estar de volta

**Não se esqueça de salvar o arquivo** após adicionar a linha.

## Passo 3: Commit da alteração

Depois de salvar o arquivo, é hora de **commitar** a alteração que você fez. Execute os seguintes
comandos no seu terminal:

- git add caos/@username/username  
- git commit -m "Adicionando mensagem de que voltei ao arquivo username.txt"

Isso vai criar um commit com a mensagem de que você voltou.

## Passo 4: Adicionar título ao arquivo

Agora, vamos adicionar um título em maiúsculas como sendo a primeira linha do arquivo e pulando uma 
linha após ele. Exemplo:

\`\`\`md
MEU ARQUIVO DE SAUDAÇÕES

olar
tchau
voltei
\`\`\`

**Salve o arquivo** após adicionar essa nova linha.

## Passo 5: Commit da nova alteração

Agora que você adicionou o título, **commite** essa alteração também.

Execute os comandos:

- git add caos/@username/username.txt  
- git commit -m "Adicionando título ao arquivo username.txt"

Agora, você tem dois commits: um dizendo que voltou e outro com o título.

## Passo 6: Entendendo histórico e hash de commits

O **hash** é uma identificação única de cada commit no Git. Cada vez que você faz um commit,
o Git gera um hash único para ele. Esse hash é uma sequência de caracteres alfanuméricos que
representa aquele commit específico.

Para ver o histórico de commits e os hashes, execute o seguinte comando:

git log --oneline

A saída será algo assim:

\`\`\`sh
a06e4d4 Adicionando título ao arquivo username.txt
2b5034d Adicionando mensagem de que voltei ao arquivo username.txt
\`\`\`

O hash de um commit é a parte antes da mensagem (por exemplo, \`a06e4d4\` ou \`2b5034d\`).

## Passo 7: Reverter o commit anterior

Agora, imagine que você se arrependeu da ideia de adicionar um título ao seu arquivo e você precisa
desfazer esse commit. Vamos usar o comando `git revert` para desfazer o commit onde você adicionou
o título.

Primeiro, localize o hash do commit onde você adicionou o título (será o commit mais recente).
Exemplo: `a06e4d4`

Agora, vamos **reverter o commit**:

\`\`\`sh
git revert <hash_do_commit>
\`\`\`

Exemplo:

\`\`\`sh
git revert a06e4d4
\`\`\`

O Git abrirá um editor de texto (geralmente o vim ou o editor configurado para seu sistema)
dentro do seu terminal para você editar a mensagem do commit de reversão.

No editor de texto, você verá algo assim:

\`\`\`vim
Revert "Adicionando título ao arquivo username.txt"

This reverts commit a06e4d4b6bec227152096bb98f4a99f2b2d117e9.

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Changes to be committed:
#       deleted:    .DS_Store
#       modified:   arara.txt
#
~
~
~
~
~
~
\`\`\`

Aqui, o Git já preencheu a mensagem para você, dizendo que está revertendo o commit.
Não altere essa mensagem a menos que tenha uma boa razão para isso. O que você precisa fazer é sair
do editor de texto.

Para sair do editor vim, siga esses passos:

1. Aperte Esc (para garantir que você não está no modo de inserção).
1. Digite :q (q vem da palavra "quit", que significa sair em inglês).
1. Aperte Enter.

Isso vai concluir o processo de reversão e criar um novo commit de reversão.

## Passo 8: Verifique seu histórico de commits

Antes de dar o push, vamos verificar como ficou o seu histórico de commits. Execute o seguinte 
comando novamente:

\`\`\`sh
git log --oneline
\`\`\`

A saída deve mostrar algo como:

\`\`\`sh
d8b8a75 Revert "Adicionando título ao arquivo username.txt"
a06e4d4 Adicionando título ao arquivo username.txt
2b5034d Adicionando mensagem de que voltei ao arquivo username.txt
\`\`\`

O commit de reversão terá um novo hash (\`d8b8a75\`), e ele desfaz o commit anterior (\`a06e4d4\`).

## Passo 9: Push para o repositório

Agora que você fez todas as alterações, é hora de enviar para o repositório remoto. Faça isso com:

\`\`\`sh
git push origin seu-branch
\`\`\`

Agora, o seu PR será atualizado com o commit original e a reversão do título.

---

- O comando `git revert` cria um novo commit para desfazer alterações feitas em um commit anterior.
Isso é muito útil quando você não quer alterar o histórico de commits e precisa desfazer alguma
modificação de maneira segura.
