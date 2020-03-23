# Gerenciamento de versões com Git
Este curso basea-se pelo livro “Learn Git in 3 Hours” por Ross Conyers.


![Git Illustration](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/04/Como-Usar-Um-Git-Branch.png)

# O que vamos aprender?
1. [Controle de versão:](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=990555315340698927896613&h2=1.-Controle-de-Vers%C3%A3o)
    1. Panorama do Curso;
    2. Versão de Controle;
2. [O Terminal:](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=990555315340698927896613&h2=1.-Controle-de-Vers%C3%A3o)
    1. Instalando e Configurando o Git;
    2. Introdução ao Terminal;
    3. Comandos básicos;
    4. Usando VI como editor;
![Resultado de imagem para summary illustration](https://img.freepik.com/free-vector/notes-concept-illustration_114360-689.jpg?size=338&ext=jpg)

3. [Aprendendo o básico:](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=416672180182243193901392&h2=3.-Aprendendo-o-b%C3%A1sico)
    1. Configurando e inicializando um repositório;
    2. Rastreando Arquivos;
    3. Visualizando mudanças;
    4. Commit
    5. Arquivos de SetUp e Git Ignore;
    6. Histórico do Projeto;
    7. Desfazendo erros;
    8. Clonando um repositório;
    9. Usando repositórios remotos;
4. [Branches e Workflow:](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=175946464537728044108229&h2=4.-Branches-e-Workflow:)
    1. O que é uma brach?
    2. Criando novas branches;
    3. Merge;
    4. Resolvendo conflitos;
    5. Branches remotas;
5. [Workflow avançado:](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=420462459154843077702432&h2=5.-Workflow-avan%C3%A7ado:)
    1. GitHub;
    2. Fork;
    3. Commits;
    4. Merge Request;
    5. Aliasing Commands;
6. [Git com Visual Studio e Git Kraken;](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=263256488206729706351850&h2=6.-Git-com-Visual-Studio-e-Git)
# 1. Controle de Versão
![Resultado de imagem para google docs](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/Google_Docs_logo.svg/1200px-Google_Docs_logo.svg.png)

## O que é um sistema de controle de versão?
- Um sistema que grava a mudanças de arquivos, salvando qualquer informação extra como data, autoria e possíveis mensagens explicando a mudança.
- Qualquer tipo de arquivo pode ter esse rastreamento, porém ele é mais comumente utilizado para projetos de desenvolvimento.
- Um exemplo muito utilizado e com características semelhantes é o Google Documentos. Nele você pode recuperar as versões anteriores e o arquivo pode ser modificado tanto localmente na sua máquina, como de maneira colaborativa de forma remota.


![Linus Torvalds like](https://www.linuxjournal.com/files/linuxjournal.com/linuxjournal/articles/036/3655/3655f1.jpg)






## Por que Git?
- Git é um dos sistemas mais utilizados tanto em projetos open source quanto em grandes empresas. Além disso, disponibiliza suporte da comunidade e um grande número de recursos.
- Simples, rápido e permite desenvolvimento não linear;
- Ele foi desenvolvido pela comunidade Linux em conjunto com Linus Torvalds;






## Principais características
![](https://paper-attachments.dropbox.com/s_0B211155733E79F7595411CCB612405E9E19952930641DB06E51BDDB76B83AB7_1581771304053_git.png)

- Armazenamento: as mudança são guardadas instantaneamente. Diferente de outros sistemas que salvam as informações continuamente. Os arquivos modificados serão salvos de imediato, aqueles sem alteração terão um link salvo apontando para a versão anterior. Assim, o Git funciona como um pequeno sistema de arquivos com ponteiros.
- Branches: possibilita desenvolvimento não linear. Permite também que os membros de uma equipe trabalhem de forma independente em qualquer parte do projeto.
- Operações locais e remotas: tudo na nuvem e tudo na máquina. Você pode baixar ter todo o seu projeto e trabalhar nele mesmo sem conexão e ao simultaneamente utilizar remotamente na nuvem.


# 2. O Terminal
## Hands-on: Instalando e Configurando o Git
![download git](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584933279758_Screen+Shot+2020-03-23+at+00.14.05.png)


Se você utiliza Windows ou MacOs, entre no [site oficial](https://git-scm.com/downloads) e acesse a aba “Downloads”. Baixe a última versão do programa, espere a instalação terminar e abra o terminal bash do seu computador.

![terminal logo](https://upload.wikimedia.org/wikipedia/commons/0/01/Windows_Terminal_Logo_256x256.png)


Para usuários Linux com distribuição Ubuntu basta usar o seguinte comando:


    $ sudo apt-get install git-all

Para verificar se o Git foi instalado corretamente basta digitar o comando:


    $ git --version

Com o terminal aberto você precisará “se cadastrar” no git. Para isso iremos utilizar o comando abaixo:


    $ git config --global user.name "Pedro Arthur"

Este comando adiciona um atributo “username” ao arquivo Git de configuração. O comando “--global” aplica essa configuração a todos os nossos projetos na máquina. Configure também o seu email:


    $ git config --global user.email "pedroarthur@nca.ufma.br"

A configuração é necessária para que o sistema rastreie os autores de cada alteração. Além disso, o email é útil para notificar os desenvolvedores caso necessário.

## Introdução ao terminal
![bash terminal](https://i2.wp.com/sempreupdate.com.br/wp-content/uploads/2016/06/Ubuntu-Debian-Fedora-openSUSE-em-qualquer-distribui%C3%A7%C3%A3o-Linux.png?fit=1684%2C1142&ssl=1)

- Nem todas as máquinas possuirão as mesmas interfaces, por isso, aprender o terminal é poder trabalhar em qualquer local;
- Alguns comandos utilizados não podem ser feitos através da interface;
- Você pode fazer tudo que é feito pela interface de forma mais veloz;
- Além disso, você pode escrever seus scripts e programas completos no terminal. 
## Comandos básicos

Por padrão, todos os comandos terão o nome do computador, o diretório e o nome do usuário:


    computer@Desktop nomeDoUsuário $


- **P**rint **W**orking **D**irectory: imprime o diretório atual


    computer@Desktop nomeDoUsuário $ pwd
    /home/runner/PeruFrizzyProgram


- **L**ist **F**iles: lista os arquivos do diretório atual


    $ ls
    main.sh


- **C**hange **D**irectory: muda o diretório

Vá para a raiz (“/”) e insira os comandos abaixo:


    $ cd /
    $ ls
    bin dev  home  lib32  mnt   root     sbin  tmp
    boot    etc  io    lib64  opt   run  srv   usr
    config  hom  lib   media  proc  run_dir  sys   var
    $ cd bin
    $ pwd
    /bin
    $ cd ..
    $ cd root
    $ cd /lib
    $ pwd
    /lib

Observação : A tecla “tab” pode ser utilizada para completar o nome de arquivos e diretórios de forma automática.


- **Man**ual: o manual pode ser visualizado

Caso você tenha dúvida sobre qualquer comando basta escrever “man” seguido pelo nome do comando.


    $ man ls

Observação: Aperte a tecla “q” para sair.


- **M**ake **Dir**ectory 

Crie duas pastas. Uma chamada “PeruFrizzyProgram” e outra “Nothing”. 


    $ mkdir Nothing
    $ mkdir PeruFrizzyProgram
    $ ls
    Nothing  PeruFrizzyProgram


- >fileName

Na pasta “PeruFrizzyProgram” crie um arquivo “myHidenTruth.txt”.


    $ cd PeruFrizzyProgram/
    $ >myHidenTruth.txt
    $ ls
    main.sh    myHidenTruth.txt


- **M**o**v**e: 

Agora mova o arquivo “myHidenTruth.txt” para a pasta “Nothing”.


    $ ls
    main.sh  myHidenTruth.txt
    $ mv myHidenTruth.txt /home/runner/Nothing

Observação: Utilize “clear” para remover os comandos da tela.

- **C**o**p**y:

Copie o arquivo “myHidenTrunth.txt”.


    $ cp myHidenTruth.txt myTears.txt ls
    myHidenTruth.txt  myTears.txt 


- **R**e**m**ove:

Remova o arquivo “myHidenTrunth.txt”.


    $ rm myHidenTruth.txt
    $ ls
    myTears.txt


- O ponto (“.”):

Vá para a pasta “PeruFrizzyProgram/” e mova o arquivo “myTears.txt” para o diretório atual usando o comando “.”, o qual indica o diretório atual.


    $ mv /home/runner/Nothing/myTears.txt . ls
    main.sh  myTears.txt

Por fim, apague o diretório “Nothing”:


    $ rm -r Nothing
    $ ls
    PeruFrizzyProgram
## Usando VI como editor


![vi editor](https://www.cyberciti.biz/media/new/faq/2011/02/Show-lines-in-vi-or-vim-text-editor.png)

- Usando para editar a mensagem do commit na linha de comando;
- Um editor de texto poderoso, leve, quase onipresente nos computadores;
- Não exige ambiente gráfico;
- Seu editor faz [isso](https://www.youtube.com/watch?v=UUzW46SeLhg)? 


Para abrir o editor de texto basta escrever o comando:


    $ vi "ViFile"


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584939216631_Screen+Shot+2020-03-23+at+01.51.50.png)


VI tem dois modos principais:  *insert* e *command*. No primeiro toda tecla apertada é interpretada como comando,  já a segunda permite você o texto é inserido no arquivo. 

Para entrar no modo de inserção basta aperta a tecla “i”. Assim, você já pode escrever.

Para sair do modo interativo e entrar no modo de comando basta apertar “Esc”.

Para salvar o arquivo aperte “:”. O seu cursor ira para a parte inferior da tela, assim escreva “w” - vem de “write” - para escreve o seu arquivo no disco. Depois escreva “q” para sair do editor.  Os comandos podem ser combinados da seguinte forma:


    Meu primeiro Vi.
    ~
    ~
    :wq

Observação: Um padrão utilizado é o das flags. São letras que podem ser usadas juntamente com outros comandos “-p”, “-x”.  Por exemplo a flag “-a” (all):


    $ ls -a

Existem muitos comandos neste editor, porém neste curso trataremos apenas o básico necessário para escrever as mensagens dos commits. Se você deseja saber mais sobre o editor, recomendo este [vídeo](https://www.youtube.com/watch?v=UUzW46SeLhg) sobre VIM (VI Improved).

# 3. Aprendendo o básico
![Resultado de imagem para abc basics](https://www.ymcasv.org/sites/default/files/styles/media_full/public/2019-06/2019%20PC%20-%20Website%20Icons-01_0.png?itok=VV7ZcjSL)

## Configurando e inicializando um repositório
- Inicializar um repositório na sua máquina transforma uma pasta num repositório git
- O commando git init cria uma pasta .git, a qual possui todos os arquivos necessários para registrar as versões;

Na pasta “PeruFrizzyProgram” use o comando git init. Um mensagem aparecerá dizendo que um repositório vazio foi iniciado. A pasta .git pode ser visualizada com o comando “ls -a”, o qual exibe todos os arquivos, inclusive os ocultos:


    $ git init
    Initialized empty Git repository in /home/runner/PeruFrizzyProgram/.git/
## Rastreando Arquivos


![Resultado de imagem para git](https://miro.medium.com/max/383/1*co_1qORNdM0PI1nvCp7Iig.png)

- Para que o git comece a buscar por alterações nos arquivos, é preciso adiciona-los ao repositório.
- Assim que um arquivo é adicionado ao repositório ele pode estar em um de três estágios diferentes: *unmodified*, *modified ou staged*. **
- Unmodifed: nenhuma mudança foi feita desde o ultimo commit;
- Modifed: o arquivo foi modificado, mas não foi adcionado ao commit atual;
- Staged: o arquivo foi modificado e adcionados à mudanças do commit;


![Resultado de imagem para git files](https://git-scm.com/book/en/v2/images/lifecycle.png)


Um arquivo não rastreado pode ser adicionado a fase de preparação para assim passar pelo *commit*. Já um arquivo que não foi modificado por ou ser editado, ou removido. Arquivos modificados podem ser preparados para o commit. Assim, todos os arquivos no estágio de preparação podem adicionados ao repositório.

Para saber o status atual dos arquivos do seu repositório basta escrever “git status”.

## Hands-on

No repositório criado anteriormente crie um arquivo utilizando o editor VI. E escreva “echo Hello PetComp” no arquivo. Logo depois utilize o comando git status note a mensagem exibida no terminal.


    $ git status
    On branch master
    No commits yet
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
        main.sh
    nothing added to commit but untracked files present (use "git add" to track)

Para adicionar o arquivo ao repositório use o comando git add seguido pelo nome o arquivo e logo depois utilize git status para ver o que é exibido na tela.


    $ git add main.sh

Nem todos os arquivos vão automaticamente são preparados para o *commit,* pois existem arquivos que talvez o desenvolvedor não queira adicionar ao repositório como arquivos gerados durante o tempo de execução.

Observação: “git add .” adiciona todos os arquivos não rastreados. 

Caso um arquivo que está na fase *staged* seja modificado, o mesmo arquivo está em dois estágios diferentes. Somente serão salvas as modificações que estão sendo rastreadas!  Observe o exemplo abaixo:



    $ vi main.sh
![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584946963475_Screen+Shot+2020-03-23+at+04.01.42.png)

    $ git status
    On branch master
    
    No commits yet
    
    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
    
        new file:   main.sh
    
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
    
        modified:   main.sh

Para adicionar as modificações basta utilizar o comando git add novamente. Assim, podemos ver que o comando git add não adiciona o arquivo em si à área *staged.* O comando, na verdade, adiciona o conteúdo do arquivo naquele exato momento à fase de preparação. 

## Visualizando mudanças
- Aprendemos até agora como ver os nomes dos arquivos modificados, porém para visualizarmos as modificações nos arquivos vamos utilizar o comando git diff. 

Faça alguma modifição 


    $ git diff
    diff --git a/main.sh b/main.sh
    index 77eae01..47adf46 100644
    --- a/main.sh
    +++ b/main.sh
    @@ -1,2 +1,2 @@ 
    echo Hello World
    -echo Não vou ser rastreado!!!
    +echo <<<Serei rastreado rastreado>>>

Após isso, adicione todos os arquivos ao próximo estágio. Neste caso o comando git diff não não exibirá nada, por isso devemos utilizar git diff —staged


    $ git diff --staged
    diff --git a/main.sh b/main.sh
    new file mode 100644
    index 0000000..5d34be4
    --- /dev/null
    +++ b/main.sh
    @@ -0,0 +1,2 @@
    +echo Hello World
    +<<<Serei rastreado rastreado>>>


## Commit
- Quando todos os arquivos que você deseja que sejam salvos no repositório já foram adicionados, o próximo passo a ser dado é usar o comando git commit;
- Para isso, mais uma vez iremos utilizar o editor VI ou qualquer outro editor especificado na variável de ambiente do seu computador.


    $ git commit

Para informações mais detalhadas daquilo que está sendo salvo você pode adrcionar a flag -v


    $ git commit -v

Para já enviar a mensagem do commit você também pode utilizar


    git commit -m "First Commit"

Observação: Só serão salvos os arquivos que foram adicionados na fase “*staged*”. Da mesma forma que utilizada no git add, a flag -a pode ser usada para adicionar todas as mudanças feitas simultaneamente.

## Arquivos de SetUp e Git Ignore
![Resultado de imagem para ignore](https://cdn.onlinewebfonts.com/svg/img_174097.png)




- Ignore arquivos! Estes não serão rastreados;
- Útil para ignorar arquivos de build e artefados de tempo de execução (arquivos binários ou de log);
- .gitignore




Crie dois novos arquivos “example.log” e “.gitignore”. Antes de adcionar o arquivo “.log” no arquivo “.gitignore” escreva o comando git status. Logo em seguida, usando o editor, escreva no arquivo “.gitignore”.


    *.log
    ~
    ~


Os arquivos .gitignore geralmente são escritos seguindo os padrões abaixo:

- Asterisco significa zero ou mais caracteres: *
- A barra no inicio significa que somente os arquivos no diretório do arquivo git ignore serão reconhecidos: /file
- A barra no final significam apenas pastas: folder/
- A exclamação negará outros padrões: !
    - Caso eu deseje ignorar todos os arquivos .txt e adicionar somente o ListaDeAfazeres.txt, basta escrever !ListaDeAfazeres.txt
- Também é possível ignorar certo tipo de arquivo por diretório: **
    - Caso eu deseje apenas ignorar os arquivos .js da pasta node eu posso escrever “node/**/*.js
- Comentários podem ser adicionados no arquivo utilizando: #

Um exemplo com os arquivos executáveis de um programa escrito em c++:


    #Executáveis
    *.exe
    *.out
    *.app


Aqui você pode encontrar um repositório oficial do GitHub com muitos exemplo de arquivos git ignore para o mais variados projetos. Acesse: https://github.com/github/gitignore


## Histórico do Projeto;
![Resultado de imagem para time machine logo](https://i2.wp.com/steve-morton.com/wp-content/uploads/2017/09/Time-Machine-5.png?fit=1024%2C1024&ssl=1)


O comando git log  mostra o histórico do repositório atravês de uma lista com os commits. O comando primeiro exibed as modificações mais recentes. Você verá o autor, a mensagem do commit, a data e horário de modificação. Existem muitas formas de exibir este histórico, por isso, nesta sessão, apenas mostraremos alguns dos comandos mais usados.

Um número pode ser usado depois do comando para limitar o número de commits expostos. Por exemplo, posso limitar o número de modificações exibidas à somente os dois últimos.


    $ git log -2

Usando a flag “-p” podemos observar os detalhes de cada modificação. Funciona de forma parecido com o comando git diff:


    & git log -p -1
    commit 5d1c7e89cf5686d114b91428ca080a000abbb3d2 (HEAD -> master)
    Author: Your Name <you@example.com>
    Date:   Mon Mar 23 08:01:34 2020 +0000
        add git ignore
    diff --git a/.gitignore b/.gitignorenew file mode 100644
    index 0000000..cfce1ad--- /dev/null+++ b/.gitignore
    @@ -0,0 +1,2 @@
    +*.log
    +

Outros comandos utilizados são:

    $ git log --pretty=oneline
    $ git log --pretty=full            #mostra muito informação
    $ git log --pretty=fuller          #mostra mais informações ainda
    $ git log --since "2 months"       #define o período de exibição
    $ git log --until "2 months"
    $ git log --graph
## Desfazendo erros


![Resultado de imagem para illustartion mistake](https://thinkingfit.co.za/wp-content/uploads/thinkingfit-you-cannot-grow-and-learn-without-making-mistakes.jpg)



1. --amend: Este comando permite adicionar, ou emendar, uma nova modificação num commit anterior. Por exemplo, é possível adicionar um arquivo README.md caso você tenha esquecido de criá-lo. Assim, é possível diminuir a quantidade de mensagens deixadas no histórico do repositório.

Para testar essa nova funcionalidade, crie um novo repositório e adicione o novo arquivo ao seu repositório. 


    $ git commit -m "Primeiro commit"
    [master (root-commit) a727085] Primeiro commit
     1 file changed, 1 insertion(+)
     create mode 100644 main.sh

Observe que no repositório apenas foi adicionado um arquivo:


    $ git log -p
    commit a727085491394573546410558bf874bd0197985e (
    HEAD -> master)
    Author: Your Name <you@example.com>
    Date:   Mon Mar 23 08:27:39 2020 +0000
    
        Primeiro commit
    
    diff --git a/main.sh b/main.sh
    new file mode 100644
    index 0000000..c346b86
    --- /dev/null
    +++ b/main.sh
    @@ -0,0 +1 @@
    +echo Hello World
    \ No newline at end of file

Utilize o comando git commit —amend para adicionar o arquivo README.md ao commit anterior. 


    $ >README.md
    $ git add .
    $ git commit --amend
    [master 250f7bc] Primeiro commit
     Date: Mon Mar 23 08:27:39 2020 +0000
     2 files changed, 1 insertion(+)
     create mode 100644 README.md
     create mode 100644 main.sh

Agora use git log -p para visualizar as modificações:


    $ git log -p
    commit 250f7bc1823e0caed776465b1d9bddc696dc321a (
    HEAD -> master)
    Author: Your Name <you@example.com>
    Date:   Mon Mar 23 08:27:39 2020 +0000
    
        Primeiro commit
    
    diff --git a/README.md b/README.md
    new file mode 100644
    index 0000000..e69de29
    diff --git a/main.sh b/main.sh
    new file mode 100644
    index 0000000..c346b86
    --- /dev/null
    +++ b/main.sh
    @@ -0,0 +1 @@
    +echo Hello World
    \ No newline at end of file



2. git revert: este comando é usado para reverter o commit anterior. Para isso é nessário ter o código de identificação do commit. Para isso, usaremos git log, e copiaremos a chave de caracteres que vem logo em seguida à palavra “commit” :



    $ git log      
    commit 250f7bc1823e0caed776465b1d9bddc696dc321a (
    HEAD -> master)
    Author: Your Name <you@example.com>
    Date:   Mon Mar 23 08:27:39 2020 +0000
    
        Primeiro commit

 
 Assim, é possível remover completamente os commits:
 

     $ git revert 250f7bc1823e0caed776465b1d9bddc696dc321a
    [master 141f969] Revert "Primeiro commit"
     2 files changed, 1 deletion(-)
     delete mode 100644 README.md
     delete mode 100644 main.sh
## Clonando um repositório
![Resultado de imagem para illustration clone](https://image.flaticon.com/icons/png/512/2205/2205368.png)

- Clonar um repositório cópia tudo existente de um outro repositório git;
- Este comando cria um diretório e cópia todo o histórico de modificações para ele;
- Para este exemplo usaremos o [](https://github.com/SlzPedroArthur/wdi-fundamentals-memorygame.git)[este repositório](https://github.com/SlzPedroArthur/Git_atv_2), acesse a página e copie o link de para baixar-lo:
![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584954094972_Screen+Shot+2020-03-23+at+05.59.32.png)

## Usando repositórios remotos

Repositórios remotos são cópias de um repositório hospedado na internet. Eles permitem a colaboração com outros desenvolvedores e podem ser removidos sempre que necessários.


    $ cd Git_atv_2/
    $ cat README.md
    # -PetComp-Git-atv-2
    Atividade para o curso de Git. 
    $ git remote
    origin
    $ git remote add new-remote http://new-remote-eample.com
    $ git remote
    new-remote
    origin
    $ git fetch origin
    remote: Enumerating objects: 5, done.
    remote: Counting objects: 100% (5/5), done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (3/3), done.
    From https://github.com/SlzPedroArthur/Git_atv_2
       9a2e33e..f453d89  master     -> origin/master
    $ cat README.md
    # -PetComp-Git-atv-2
    Atividade para o curso de Git 
    $ git merge origin/master master
    Updating 9a2e33e..f453d89
    Fast-forward
     README.md | 1 +
     1 file changed, 1 insertion(+)
    $ cat README.md
    # -PetComp-Git-atv-2
    Atividade para o curso de Git 
    Alguém modificou o arquivo!
    $ vi README.md
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.
    
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
    
    modified:   README.md
    
    no changes added to commit (use "git add" and/or "git commit -a")
    $ git add README.md 
    $ git commit -m "Eu sou a primeira linha"
    [master 945d420] Mudei o README
     1 file changed, 2 insertions(+)
    $ git push origin master
    Counting objects: 3, done.
    Delta compression using up to 4 threads.
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0)
    To https://github.com/SlzPedroArthur/Git_atv_2
       e6a4105..9b91f9a  master -> master



# 4. Branches e Workflow:


# 5. Workflow avançado:
# 6. Quer GUI? Pois tome: Git com Visual Studio e Git Kraken;

