# [PETComp] Gerenciamento de versões com Git
Este curso basea-se no curso “Learn Git in 3 Hours” por Ross Conyers.
https://github.com/SlzPedroArthur/PetComp-git


![Git Illustration](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/04/Como-Usar-Um-Git-Branch.png)

# 0. O que vamos aprender?
![Resultado de imagem para summary illustration](https://img.freepik.com/free-vector/notes-concept-illustration_114360-689.jpg?size=338&ext=jpg)

1. Controle de versão:
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=990555315340698927896613&h2=1.-Controle-de-Vers%C3%A3o)    1. Panorama do Curso;
    2. Versão de Controle;
2. O Terminal:
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=990555315340698927896613&h2=1.-Controle-de-Vers%C3%A3o)    1. Instalando e Configurando o Git;
    2. Introdução ao Terminal;
    3. Comandos básicos;
    4. Usando VI como editor;
3. Aprendendo o básico:
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=416672180182243193901392&h2=3.-Aprendendo-o-b%C3%A1sico)    1. Configurando e inicializando um repositório;
    2. Rastreando Arquivos;
    3. Visualizando mudanças;
    4. Commit
    5. Arquivos de SetUp e Git Ignore;
    6. Histórico do Projeto;
    7. Desfazendo erros;
    8. Clonando um repositório;
    9. Usando repositórios remotos;
    10. Tags
4. Branches:
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=175946464537728044108229&h2=4.-Branches-e-Workflow:)    1. O que é uma brach?
    2. Criando novas branches;
    3. Merge;
    4. Resolvendo conflitos;
    5. Branches remotas;
5. Workflow:
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=420462459154843077702432&h2=5.-Workflow-avan%C3%A7ado:)    1. GitHub;
    2. Fork;
    3. Commits;
    4. Merge Request;
    5. Customizando comandos;
6. Projeto;
7. Git com Visual Studio e Git Kraken;
8. Saiba Mais.
[](https://www.dropbox.com/scl/fi/2yd54toy785yjkc92ldbm/Gerenciamento-de-vers-es-com-Git.paper?dl=0&rlkey=heqpy520owvbw3yot1libwyjv#:uid=263256488206729706351850&h2=6.-Git-com-Visual-Studio-e-Git)# 1. Controle de Versão
## O que é um sistema de controle de versão?
- Um sistema que grava a mudanças de arquivos, salvando qualquer informação extra como data, autoria e possíveis mensagens explicando a mudança.
- Qualquer tipo de arquivo pode ter esse rastreamento, porém ele é mais comumente utilizado para projetos de desenvolvimento.
- Um exemplo muito utilizado e com características semelhantes é o Google Documentos. Nele você pode recuperar as versões anteriores e o arquivo pode ser modificado tanto localmente na sua máquina, como de maneira colaborativa de forma remota.


![Linus Torvalds like](https://www.linuxjournal.com/files/linuxjournal.com/linuxjournal/articles/036/3655/3655f1.jpg)

## Por que Git?
- Git é um dos sistemas mais utilizados tanto em projetos open source quanto em grandes empresas. Além disso, disponibiliza suporte da comunidade e um grande número de recursos.
- Simples, rápido e permite desenvolvimento não linear;
- Ele foi desenvolvido pela comunidade Linux em conjunto com Linus Torvalds;
![https://dl.acm.org/doi/abs/10.5555/2020786.2020790](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585127325793_Screen+Shot+2020-03-25+at+06.08.12.png)

## Principais características
- Armazenamento: as mudança são guardadas instantaneamente. Diferente de outros sistemas que salvam as informações continuamente. Os arquivos modificados serão salvos de imediato, aqueles sem alteração terão um link salvo apontando para a versão anterior. Assim, o Git funciona como um pequeno sistema de arquivos com ponteiros - em camadas.
- Branches: possibilita desenvolvimento não linear. Permite também que os membros de uma equipe trabalhem de forma independente em qualquer parte do projeto.
- Operações locais e remotas: tudo na nuvem e tudo na máquina. Você pode baixar ter todo o seu projeto e trabalhar nele mesmo sem conexão e ao simultaneamente utilizar remotamente na nuvem.

O Git diferente de outros sistemas compara as alterações byte por byte e possui uma estrutura em camadas que possui duas partes principais:


- *Repositório*: é a unidade de armazenamento principal e contem uma ou mais ramos (branches).
- *Branch*: os branches separam o workflow e possuim atribuições locais, ou seja, as modificações em uma branch ficam no mesmo escopo. Estas modificações podem ser unidas à outra branch e outras branches podem sair da mesma. Por padrão, todo repositório possui um branch master, essa funciona como a versão “oficial” ou “atual”. Ele além de ser o pai de todas as outras branches também funciona como o fim para o qual todas as branches foram criadas. 
- 

Além disso as modificações dos projetos podem ser feitas tanto localmente quanto remotamente através de sites como o github ou o gitlab. 

![](https://paper-attachments.dropbox.com/s_0B211155733E79F7595411CCB612405E9E19952930641DB06E51BDDB76B83AB7_1581771304053_git.png)

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

VI tem dois modos principais:  *insert* e *command*. No primeiro toda tecla apertada é interpretada como comando,  já a segunda permite você o texto é inserido no arquivo. 

Para entrar no modo de inserção basta aperta a tecla “i”. Assim, você já pode escrever.

Para sair do modo interativo e entrar no modo de comando basta apertar “Esc”.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584939216631_Screen+Shot+2020-03-23+at+01.51.50.png)


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


O comando git log  mostra o histórico do repositório atravês de uma lista com os commits. O comando primeiro exibed as modificações mais recentes. Você verá o autor, a mensagem do commit, a data e horário de modificação. Existem muitas formas de exibir este histórico, por isso, nesta seção, apenas mostraremos alguns dos comandos mais usados.

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
- Para este exemplo vamos usar um [repositório no GitHub](https://github.com/SlzPedroArthur/playground.git). Entre na página do repositório e copie o link de para clona-lo:
![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1584954094972_Screen+Shot+2020-03-23+at+05.59.32.png)


Você pode usar o comando “git clone” para baixar uma cópia dele na sua máquina.  Entre no diretório baixado e utilize o comando “ls -a” para visualizar todos os arquivos e diretórios baixos. 


    $ git clone https://github.com/SlzPedroArthur/playground.git
    Cloning into 'playground'...
    remote: Enumerating objects: 3, done.
    remote: Counting objects: 100% (3/3), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (3/3), done.
    $ ls -a
    .  ..  main.sh  playground
## Usando repositórios remotos
![Resultado de imagem para cloud service illustration](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585098199894_Screen+Shot+2020-03-24+at+22.02.57.png)


Repositórios remotos são cópias de um repositório hospedado na internet. Eles permitem a colaboração com outros desenvolvedores e podem ser removidos ou criados sempre que necessários. Nesta seção usaremos o repositório baixado no tópico anterior para aprender como gerenciar os repositórios na web. Antes de tudo, você pode notar que há somente um arquivo no repositório. Você pode visualizar o conteúdo usando o comando “cat”.


    $ cat README.md
    # playground 

Agora podemos utilizar o comando “git remote” para exibirmos todos repositório remotos que estão sendo usado. Já que clonamos este repositório, o comando exibirá “origin” (este é o nome padrão utilizado pelo git para os remotos configurados). Caso tivéssemos criado um repositório localmente nada seria exibido.


    $ git remote
    origin

Além disso, podemos criar remotos de forma explicita usando o comando “git remote add” seguindo pelo endereço de hospedagem do repositório.


    $ git remote add new-remote http://new-remote-example.com
    $ git remote
    new-remote
    origin

Agora que já temos o repositório localmente, caso uma modificação seja feita de forma remota e nós desejamos baixa-la, utilizaremos o comando “git fetch”. Isso pode ser feito com qualquer remoto configurado, neste caso utilizaremos origin. 


    $ git fetch origin
    remote: Enumerating objects: 5, done.
    remote: Counting objects: 100% (5/5), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (3/3), done.
    From https://github.com/SlzPedroArthur/playground
       2e87316..59de9c0  master     -> origin/master   #Atualizando commit

Note que a master branch de origin foi atualizada , mas que ainda assim o arquivo README.md não foi modificado. Por isso, devemos lembrar que este comando apenas baixa os arquivos, mas não junta-os com seu projeto. Para fazer isso podemos usar o comando git merge. Neste caso vamos juntar “origin/master” com “master”.


    $ git merge origin/master master
    Updating 2e87316..59de9c0
    Fast-forward
     README.md | 4 +++-
     1 file changed, 3 insertions(+), 1 deletion(-)
    $ cat README.md
    # playground
    
    Atualizando!

Para enviar as modificações do nosso repositório local para o remoto, vamos utilizar o comando git push. Primeiro precisamos modificar os arquivos que acabaram de ser baixados, para depois enviarmos as atualizações.


    $ vim README.md
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.
    
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
    
        modified:   README.md
    
    no changes added to commit (use "git add" and/or "git commit -a")

Vamos adicionar as modificações ao estágio de preparação. Depois faremos o commit.


    $ git add README.md
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.
    
    Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)
    
        modified:   README.md
    $ git commit README.md
    [master ec96889] estou modificando
     1 file changed, 4 insertions(+), 1 deletion(-)

Depois de fazer o commit, basta utilizar o comando git push seguido pelo remoto de destino e a branch de origem (de onde as moficações serão atualização). Caso seja a primeira vez que você está usando o comando, será necessário colocar seu usuário e senha.


    $ git push origin master
    Username for 'https://github.com': slzpedroarthur
    Password for 'https://slzpedroarthur@github.com': ********************
    Counting objects: 3, done.
    Delta compression using up to 4 threads.
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (3/3), 307 bytes | 307.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0)
    To https://github.com/SlzPedroArthur/playground.git
       59de9c0..ec96889  master -> master

Agora se voltarmos para página do repositório na GitHub, vamos ver que as atualizações foram feitas com sucesso. Para mais informações sobre os remotos e as branches podemos usar “git remote show” seguido pelo nome do remoto:


    $ git remote show origin
    * remote origin
      Fetch URL: https://github.com/SlzPedroArthur/playground.git
      Push  URL: https://github.com/SlzPedroArthur/playground.git
      HEAD branch: master
      Remote branch:
        master tracked
      Local branch configured for 'git pull':
        master merges with remote master
      Local ref configured for 'git push':
        master pushes to master (up to date)

Podemos ver aqui o URL, as branches e se nosso repositório local está atualizado. Além disso, vemos que podemos utilizar o comando “git pull”. Este comando funciona como a união dos comandos “git fetch” e “git merge” - no caso, merge para a master. 


    $ git pull origin
    remote: Enumerating objects: 5, done.
    remote: Counting objects: 100% (5/5), done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (3/3), done.
    From https://github.com/SlzPedroArthur/playground
       ec96889..05d66ac  master     -> origin/master
    Updating ec96889..05d66ac
    Fast-forward
     README.md | 2 ++
     1 file changed, 2 insertions(+)
    $ cat README.md
    # playground
    
    Atualizado! Estou aprendendo git! 
    
    
    ou tentando...
    
    Tantos comandos...


## Tags
![Resultado de imagem para tags illustration](https://images.twinkl.co.uk/tr/image/upload/illustation/price-tag.png)


Tags são usadas para marcar commits relevantes para o projeto. Por exemplo, uma tag v1.0.0 pode ser usada para marcar um commit que é o primeiro disponível para o usuário final. Cada atualização em geral recebe uma tag. Existem dois tipos de tags


- Annotated: possuem mais informações como o data e autor, além de possuirem uma mensagens.
- Lightweight: não podem ser movidas e são apenas ponteiros estáticos para um commit.

Para criarmos uma tag, vamos utilizar o comando “git tag”. Este comando criará a tag no nosso commit atual. Para visualizarmos a tag basta utilizar o comando “git show” seguindo pelo noma da tag.


    $ git tag "1.0"
    $ git show "1.0"
    commit fce5cb8730951f93eebfdf80c6cff920f95afa3d (HEAD ->
     master, tag: 1.0, origin/master
    , origin/HEAD)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:52:27 2020 +0000
    
        colocando erro
    
    diff --git a/README.md b/README.md
    index 529296d..ba12ab4 100644
    --- a/README.md
    +++ b/README.md
    @@ -5,4 +5,4 @@ Atualizado! Estou aprendendo git!
     
     ou tentando...
     
    -Tantos comandos...
    +Tantos comandss...

Perceba que acabamos de criar uma Lightweight tag. Se nós precisarmos salvar mais informações na nossa tag vamos precisar criar uma annotated tag. Para isso utilizaremos o mesmo comando, mas com a diferença da flag “-a”.


    $ git tag -a "1.1" -m "Essa é minha annotated tag."
    $ git show "1.1"
    tag 1.1
    Tagger: Your Name <you@example.com>
    Date:   Wed Mar 25 02:33:04 2020 +0000
    
    Essa é minha annotated tag.
    
    commit fce5cb8730951f93eebfdf80c6cff920f95afa3d (HEAD ->
     master, tag: 1.1, tag: 1.0, 
    origin/master, origin/HEAD)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:52:27 2020 +0000
    
        colocando erro
    
    diff --git a/README.md b/README.md
    index 529296d..ba12ab4 100644
    --- a/README.md
    +++ b/README.md
    @@ -5,4 +5,4 @@ Atualizado! Estou aprendendo git!
     
     ou tentando...
     
    -Tantos comandos...
    +Tantos comandss...

Se quisermos utilizar as tags remotamente, basta usar o “git push”.


    $ git push origin 1.1
    Counting objects: 16, done.
    Delta compression using up to 4 threads.
    Compressing objects: 100% (9/9), done.
    Writing objects: 100% (16/16), 2.46 KiB | 840.00 KiB/s, done.
    Total 16 (delta 2), reused 0 (delta 0)
    remote: Resolving deltas: 100% (2/2), done.
    To https://github.com/SlzPedroArthur/playground.git
     * [new tag]         1.1 -> 1.1

Isso pode tornar-se um pouco trabalhoso caso nós criemos muitas tags. Para isso, podemos usar o mesmo comando acima com a única diferença de que teremos que adicionar “--tags”.


    $ git push origin --tags
    Total 0 (delta 0), reused 0 (delta 0)
    To https://github.com/SlzPedroArthur/playground.git
     * [new tag]         1.0 -> 1.0


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585104022787_Screen+Shot+2020-03-24+at+23.39.56.png)

![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585104063198_Screen+Shot+2020-03-24+at+23.40.01.png)

# 4. Branches
## O que é uma Branch?
![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585111372490_file.png)


As branches são talvez umas das melhores funcionalidades do git, por poderem ser rapidamente criadas e removidas. Para entender as branches, primeiramente devemos lembrar de como o git salva as mudanças no decorrer do tempo. Diferente de outros sistemas, ele não salva diferentes arquivos continuamente, mas cada commit cria um arquivo que contem a referência para um estado. Assim, o git salva uma série de estados, funcionando em camadas.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585107897203_2.png)

![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585107906515_1.png)


Dessa forma, o git gerencia os arquivos de forma parecida com uma lista de vetores. Porém, podemos criar novas branches. Podemos visualizar o estado atual do nosso repositório usando o comando “git log” . Observe que já fizemos cinco commits:


    $ git log
    commit fce5cb8730951f93eebfdf80c6cff920f95afa3d (HEAD -
    > master, tag: 1.1, tag: 1.0, 
    origin/master, origin/HEAD)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:52:27 2020 +0000
    
        colocando erro
    
    commit 05d66ac86a628f5c58650fbca03c3075d7f3c176
    Author: SlzPedroArthur <56669563+SlzPedroArthur@users.noreply.github.com>
    Date:   Tue Mar 24 22:48:27 2020 -0300
    
        Update README.md
    
    commit ec968892f666053e662d523ee4c6b3c29a2ee986
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:36:20 2020 +0000
    
        estou modificando
    
    commit 59de9c0fca771a47d58abdbb9a7446a43eb09508
    Author: SlzPedroArthur <56669563+SlzPedroArthur@users.noreply.github.com>
    Date:   Tue Mar 24 22:17:51 2020 -0300
    
        Update README.md
    
    commit 2e8731607fbd74f0ff31f6bd1570a3d8a5970ba5
    Author: SlzPedroArthur <56669563+SlzPedroArthur@users.noreply.github.com>
    Date:   Tue Mar 24 21:53:29 2020 -0300
    
        Initial commit

O git utiliza um ponteiro para a branch que estamos usando no momento. No nosso caso, podemos entender da seguinte forma:


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585108705689_9070b.png)

## Criando novas branches

Para criar uma nova ramificação no nosso projeto basta nós utilizarmos o comando “git branch” seguido pelo nome da branch. Já para mudar a branch atual é só utilizar “git checkout” seguido pelo nome da branch. 


    $ git branch nome-da-nova-branch
    $ git checkout nome-da-nova-branch
    Switched to branch 'nome-da-nova-branch'
    $ git log -1
    commit fce5cb8730951f93eebfdf80c6cff920f95afa3d (HEAD -
    > nome-da-nova-branch, tag: 1.1, tag:
     1.0, origin/master, origin/HEAD, 
    master)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:52:27 2020 +0000
    
        colocando erro

Observe que agora que “nome-da-nova-branch” aparece qunado usamos “git log”. Além diso, podemos ver que HEAD está apontando para a branch que acabamos de criar. Caso um novo commit seja adicionado no repositório apenas a nova branch será movida.  Vamos modificar o arquivo README.md mais uma vez e fazer um commit.


    $ vi README.md
    $ git add .
    $ git commit
    $git log -1
    commit f36cf342f1ab8c4edc5bd51d6969fba432c8c4b3 (HEAD -
    > nome-da-nova-branch)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 04:05:04 2020 +0000
    
        aprendendo branches


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585109791299_Screen+Shot+2020-03-25+at+01.15.16.png)


Por outro lado, se formos para a branch master e observarmos seu histórico teremos um resultado diferente.


    $ git checkout master
    Switched to branch 'master'
    Your branch is up to date with 'origin/master'.
    $ git log -1
    
    commit fce5cb8730951f93eebfdf80c6cff920f95afa3d (HEAD -
    > master, tag: 1.1, tag: 1.0, 
    origin/master, origin/HEAD)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 01:52:27 2020 +0000
    
        colocando erro

Agora, faremos um novo commit na master. Editaremos o arquivo README.md. Por causa disso, uma divergência foi criada no seu workflow. Assim, temos o seguinte cenário:


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585110714908_Screen+Shot+2020-03-25+at+01.31.32.png)

## Merge

Trabalhar em grupo as vezes pode ser um pouco estressante. Um dos principais motivos de estresse é terem outras pessoas alterando o que você acabou de fazer. Para isso, as branches podem ser usadas para que o trabalho seja feito sem que os arquivos que você está modificando interfira no de seu colega. 

Imagine o seguinte cenário: você está trabalhando numa nova funcionalidade do seu sistema numa branch chama “nova-feature”. Entretanto, o usuário do sistema relatou um problema que impossibilita o acesso a algumas funcionalidades. Por isso, você você faz o checkout para a branch master - a branch principal e que o usuário usa - e a partir da master cria uma nova branch chamada “bug” e faz lá a manutenção necessária. Depois de terminar, você une a branch “bug” na “master” e volta a trabalhar na “nova-feature”. Isso funciona da seguinte forma:


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585114505859_Screen+Shot+2020-03-25+at+02.34.43.png)


Este exemplo representa um cenário bem comum durante o desenvolvimento de software. Para reproduzir esse cenário vamos utilizar o comando “git checkout” seguido pela flag “-b” e o nome da branch para criar uma nova branch. 


    $ git checkout -b feature-branch
    Switched to a new branch 'feature-branch'

Observação: Sempre que você precisar saber sua branch atual e quais as outras branches existentes basta usar o comando “git branch” sem nenhum parâmetro.


    $ git branch
    * feature-branch
      master
      nome-da-nova-branch

Adicione agora uma nova feature.


    $ vi README.md
    $ git add .
    $ git commit
    [feature-branch e889db2] new feature
     1 file changed, 2 insertions(+)

Agora vamos corrigir o bug. Para isso vamos da um checkout para a master e criar uma nova branchLembre-se de que os arquivos estão no estado em que deixamos no tópico anterior.


    $ git checkout master
    Switched to branch 'master'
    Your branch is ahead of 'origin/master' by 1 commit.
      (use "git push" to publish your local commits)
    $ git checkout -b bug-fix
    Switched to a new branch 'bug-fix'
    $ git branch
    * bug-fix
      feature-branch
      master
      nome-da-nova-branch

Vamos consertar o “bug” no arquivo README.md e fazer um novo commit.


    $ vi README.md
    $ git add .
    $ git commit -m "fix bug"

Agora que o erro foi corrigido vamos fazer o merge na master. Para isso, primeiro temos que fazer o checkout para a master e depois usar o comando “git merge” seguido pelo nome da branch, no caso “bug-fix”.


    $ git checkout master
    Switched to branch 'master'
    Your branch is ahead of 'origin/master' by 1 commit.
      (use "git push" to publish your local commits)
    $ git merge bug-fix
    Updating 372521f..5c7822c
    Fast-forward
     README.md | 4 +---
     1 file changed, 1 insertion(+), 3 deletions(-)

Observe que “Fast-forward” foi criado. Isso significa que nenhum commit novo foi criado, mas que a master simplismente aponta agora para bug-fix. Isso pode ser visto usando git log.


    $ git log -1
    commit 5c7822cddf62e355d64d71a2e5442b573d86122e (HEAD -
    > master, bug-fix)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 04:54:17 2020 +0000
    
        fix bug

Uma vez que o erro já foi corrigido podemos deletar a branch bug-fix. Isso não deletará as mudanças, pois está já foram salva na master.


    $ git branch -d bug-fix
    Deleted branch bug-fix (was 5c7822c).

Agora podemos voltar a trabalhar na nova feature. 


    $ git checkout nome-da-nova-branch
    Switched to branch 'feature-branch'

Vamos modificar o arquivo README.md e fazer o commit.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585113439042_Screen+Shot+2020-03-25+at+02.14.11.png)


Vamos repetir o processo anterior e fazer o checkout para a master.


    $ git checkout master
    Switched to branch 'master'
    Your branch is ahead of 'origin/master' by 2 commits.
      (use "git push" to publish your local commits)

Obrservação: Veja que a master local está na frente da que está no GitHub. Isso significa que existem mudanças que não estão no meu repositório remoto.


    $ git merge nome-da-nova-branch
    Auto-merging README.md
    Merge made by the 'recursive' strategy.
     README.md | 3 ++-
     1 file changed, 2 insertions(+), 1 deletion(-)

Você deve ter notado que o editor foi aberto quando tentado fazer o merge. Isso acontece porque estamos fazendo um merge commit. Neste caso houveram divergências, o que significa que a “nome-da-nova-branch” possui mudanças que não estão na master e vice-versa. Isso aconteceu por causa das mudanças da branch bug-fix. Por isso, invés de apenas trocar os ponteiros (Fast-forward), o Git cria um novo estado a partir do ancestral em comum mais recente.

Por fim, verifique se os arquivos foram atualizados e depois delete a branch.


    $ git branch -d nome-da-nova-branch
    Deleted branch nome-da-nova-branch (was f36cf34).



## Resolvendo conflitos

Neste tópico aprenderemos como solucionar conflitos durante o merge. Existem casos em que o mesmo arquivo possui as mesmas partes alteradas e o Git não consegue resolver os conflitos de forma automática. Por isso, intervenção humana será requerida. Vamos criar uma nova branch e ver como isso funciona no terminal.


    $ git checkout -b bug
    Switched to a new branch 'bug'
    $ vi README.md
    $ git add .
    $ git commit -m "conserto de bug"
    [bug 523a8ab] conserto de bug
     1 file changed, 3 insertions(+), 1 deletion(-)

Agora volte para a master e de lá crie uma nova branch e faça o checkout para ela. Nessa nova branch modifique o arquivo README.md na mesma linha que você modificou na branch bug.

    
    $ git checkout -b develop
    Switched to a new branch 'develop'

Volte para a master e faça o merge da branch bug. Observe que mais uma vez o git mesclou os ramos automaticamente usando o fast-forward.


    $ git checkout master
    Switched to branch 'master'
    Your branch is ahead of 'origin/master' by 5 commits.
      (use "git push" to publish your local commits)
    $ git merge bug
    Updating 856d565..523a8ab
    Fast-forward
     README.md | 4 +++-
     1 file changed, 3 insertions(+), 1 deletion(-)

Agora, vamos tentar fazer o merge da branch develop na master.


    $ git merge develop
    Auto-merging README.md
    CONFLICT (content): Merge conflict in README.md
    Automatic merge failed; fix conflicts and then commit the result.

Veja que o merge automático falhou e agora o git pede que nós resolvamos o conflito de forma manual. Para isso, vamos tentar descobrir o que está acontecendo usando git status.


    $ git status
    On branch master
    Your branch is ahead of 'origin/master' by 6 commits.
      (use "git push" to publish your local commits)
    
    You have unmerged paths.
      (fix conflicts and run "git commit")
      (use "git merge --abort" to abort the merge)
    
    Unmerged paths:
      (use "git add <file>..." to mark resolution)
    
        both modified:   README.md
    
    no changes added to commit (use "git add" and/or "git commit -a")

Se abrirmos o arquivo que modificamos podemos ver as linhas de conflito. Note que foram adicionadas algumas linha: duas que separam a seção de conflito (de <<<<<< HEAD até >>>>>>> develop) e uma separando as linhas de conflito (=======).


    # playground
      
    Usando branches.
    
    <<<<<<< HEAD
    Atualizado! Estou aprendendo git
    
    Alterando na "bug"!
    =======
    Atualizado! Estou aprendendo git!
    
    Desenvolvendo.
    >>>>>>> develop
    ~     

Para solucionarmos o problema, temos que manualmente deletar adicionadas pelo git. Neste caso, eu desejo manter as alterações de ambos os ramos.


    # playground
      
    Usando branches.
    Alterando na "bug"!
    Atualizado! Estou aprendendo git!
    Desenvolvendo.
    ~       

Agora vamos fazer um merge commit. Para tal, usaremos os mesmo comandos de um commit.


    $git add .
    $git commit

Observe que é exibido um layout um pouco diferente. Ele serve para explicar as razões do commit. Porém, para os propositos desse curso não faremos nenhuma modificação.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585117084036_Screen+Shot+2020-03-25+at+03.15.20.png)

    $ git commit
    [master 1deee07] Merge branch 'develop'

Se usarmos git log —graph, temos um gráfico do que acabamos de fazer.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585117247377_Screen+Shot+2020-03-25+at+03.19.42.png)

## Branches remotas

Agora, vamos apredender como gerenciar branches remotas. Essas branches são referencias locais à uma branch num servidor. Branches remotas usam um referência: <nome do remoto>/<nome da branch>. Por exemplo origin/master.

Para compartilhar suas branches com os outros, você precisar dar um push para o servidor. Basta usar git push (ex. git push origin my-feature-branch). Agora, os outros colaboradores podem usar git fetch parar reberem uma referência à sua branch. Para que eles trabalhem nela é preciso usar git checkout origin my-feature-branch. Isso cria uma tracking branch.

Uma tracking branch é uma branch que segue um branch remota. Qualquer mudança será atualizada na branch no servidor e qualquer mudança no servidor será atualizada localmente. Isso acontece quando clonamos um repositório. Neste caso estamos criando uma tracking branch para a master. Para rastrear outrar branch, basta usar:


- git checkout -b branch-nome remote/branch-nome

O git pode fazer isso automaticamente usando “git checkout branch-nome”. Para checar quais são suas branches remotas usando “git branch -vvt”. 

Outras ação importe é a de deletar branches remotas que não estão sendo utilizadas. Além disso colaborar para a organização do projeto, também deixa-o mais leve e evita que outras pessoas trabalhem em branches que não estão sendo usadas. Para isso usando:


- git push <remote-nome> —delete <branch-nome>


## Trocando de base

Trocar de base é outro método para combina diferentes branches. Esse método coloca todos os commits de duas branches numa nova branch. Isso evita com que merge commits sejam criados.

Isso funciona achando o ancestral comum das dadas branches e calculando o caminho que foi criado por cada commit, aplicando cada um deles na mesma ordem na nova branch que está sendo criada.  Os principais benefícios de usar rebasing são um histórico mais limpo na incorporação de mudanças. O histórico fica mais limpo e também podemos adicionar alterações que foram feitas antes depois que você criou sua branch. Por exemplo, caso uma mudança tenha sido feita na master depois de criarmos a branch bug, através desse método podemos incluir as últimas modificações. Entretando, essa prática pode ser muito perigosa quando colocamos a base de branches públicas nas nossas branches. 
 
Observe o diagrama abaixo para entender o que faremos no terminal a seguir.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585120206926_Screen+Shot+2020-03-25+at+04.09.48.png)


Na imagem acima, criamos uma nova brach e fizemos um commit tanto nela, quanto na master.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585120313840_Screen+Shot+2020-03-25+at+04.11.02.png)


Depois de trocarmos a base, você pode notar que os commits foram mantidos. Para finalizar o processo, basta fazer um merge da master na nova branch, ficando da seguinte forma:

![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585120423621_Screen+Shot+2020-03-25+at+04.13.29.png)


 
No terminal, vamos tentar reproduzir o que acabamos de ver na teoria. Primeiro precisamos verificar quais branches temos. Para isso, usaremos a forma do gráfico com os commits limitados a ocuparem uma linha da ela:


    $ git log --branches --graph --oneline
    * 0964a2d (HEAD -> master) master
    | * 58afc11 (feature) feature
    |/  

Para trocarmos de base, basta usar o comando “git rebase master”. Isto fará com que a nova base seja a master.


    $ git checkout feature
    $ git rebase master
    $ git log --branches --graph --oneline
    * 271fcfa (HEAD -> feature) mundando ai
    * 58c01e3 (master) mundando
    * 0964a2d master
    *   1deee07 Merge branch 'develop'
    |\  

Você pode ver que temos apenas uma linha reta de histórico. Agora para levarmos master para a ponta da branch basta usarmos git merge.


    $ git merge feature
    $ git log --branches --graph --oneline
    * 271fcfa (HEAD -> master, featur
    e) mundando ai
    * 58c01e3 mundando
    * 0964a2d master
    *   1deee07 Merge branch 'develop'
    |\  
# 5. Workflow
## GitHub
![Resultado de imagem para github illustration](https://i.pinimg.com/originals/bd/51/9a/bd519a06826b9043b8b6edd9e167123a.jpg)


GitHub é uma grande comunidade de repositórios, tanto públicos como privados. Colaboração se torna fácil com a plataforma, pois qualquer pessoa pode solicitar colaborar com seu repositório público. Além disso, os desenvolvedores não precisam preocupar-se com onde irão hospedar o seu código. Muitos projetos famosos utilizam o GitHub e suas funcionalidades hoje vão muito além da de fornecer um repositório remoto. Nele você pode encontrar ou criar cursos, fazer o deploy de sua aplicação, gerenciar times inteiros, submeter o seu código à testes (gitactions) e até mesmo criar uma página pessoal com seu portfólio (gitpages).  Um exemplo de um grande projeto do GitHub é o TensorFlow, o qual possui atualizações quase diárias:


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585122664914_Screen+Shot+2020-03-25+at+04.49.58.png)


Nesta seção usaremos o GitHub como exemplo. Porém, existem outras plataformas, como o GitLab que além de possuir ferramentas adicionais para testes e integração continua, tem crescido muito e recebido atualizações constantes.

## Fork

O fork é uma cópia de um repositório que fazemos para colaborar com os projetos de outras pessoas. O fork também pode ser utilizado para criar novos projetos fazendo reuso de outros. Podemos trabalhar na nossa cópia e depois solicitar que as alterações sejam mescladas no projeto original. Usaremos como exemplo o repositório do TensorFlow. Para copia-lo só precisamos apertar o botão fork no canto superior direito.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585123173023_Screen+Shot+2020-03-25+at+04.59.12.png)










## Commits

Existem dicas básicas que podem ser seguidas para que o trabalho no futuro seja mais fácil. Além de nos ajudar a entender o projeto no futuro, também faz com que outras pessoas entendam nossas contribuições. Acredite, todos agradecerão se nós seguirmos algumas regrinhas. Além disso, contribuir com open source ficará ainda mais fácil. Um exemplo de uma boa mensagem é a seguinte:


![by Ross Conyers](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585123773590_Screen+Shot+2020-03-25+at+05.08.57.png)


Além disso, tentar separar os commits de forma lógica em pequenos conjuntos sempre facilita o entendimento. Por isso, sempre esteja fazendo commits e nunca deixe para fazer-lo depois de horas trabalhando no mesmo projeto.

Outra funciona interessante do git é a de agrupar os commits que fazemos. Esta função nos ajuda a manter a qualidade nas mensagens. As vezes começamos bem com mensagens de qualidade, mas terminamos a seção de trabalho com “aahr NAO FUNCIONA”. 

 Para juntarmos as mensagens basta usar git reset seguido por —soft (mantendo as alteracões, mas deletando os commits). Depois, colocamos HEAD˜ seguido pelo número de commits que desejamos voltar.
 

    $ git reset --soft HEAD~7
    $ git log
    commit 2e8731607fbd74f0ff31f6bd1570a3d8a5970ba5
     (HEAD -> master)
    Author: SlzPedroArthur <56669563+SlzPedroArthur@use
    rs.noreply.github.com>
    Date:   Tue Mar 24 21:53:29 2020 -0300
    
        Initial commit

Para visualizarmos todas as mudanças que foram feitas no commits que acabamos de realizar, podemos usar git diff —staged.


    $ git diff --staged
    diff --git a/README.md b/README.md
    index 3b09d41..76aebf6 100644
    --- a/README.md
    +++ b/README.md
    @@ -1 +1,4 @@
    -# playground
    \ No newline at end of file
    +# playground
    +
    +Estou usando a master.
    +Estou usando a branch feature

Agora, só precisa fazer um commit seguido pela flag -v.


![](https://paper-attachments.dropbox.com/s_7B61B673B06C834F7D0D329CC4B613524EA1268C810743F1BE2663C2ABF4D355_1585124870081_Screen+Shot+2020-03-25+at+05.27.31.png)

    $ git log
    commit 7e8201f99a6cd3c77b8e80dbe9d8eb5f4638f5fd
     (HEAD -> master)
    Author: Your Name <you@example.com>
    Date:   Wed Mar 25 08:26:20 2020 +0000
    
        Editando a documentação
        
        Adicinados as  novas instruções  para o tutoria
    l degit.
        
        Explicando o que são as branches

Da mesma forma que o comando rebase, o comando reset reescreve o histórico o que pode ser perigoso. Por isso, verifique se a branch não é pública e não foi mesclada. 

## Merge Request

working on it.


## Customizando comandos

Podemos customizar os comandos, adaptando-os ao nosso ambiente de trabalho. Para fazer isso usaremos o git config. Por exemplo, mudaremos o comando git status para git st.


    $ git status
    On branch master
    Your branch and 'origin/master' have diverged,
    and have 1 and 4 different commits each, respectively.
      (use "git pull" to merge the remote branch into yours)
    
    nothing to commit, working tree clean
    $ git config --global alias.st status
    $ git st
    On branch master
    Your branch and 'origin/master' have diverged,
    and have 1 and 4 different commits each, respectively.
      (use "git pull" to merge the remote branch into yours)
    
    nothing to commit, working tree clean

Isso pode ser útil para tornar alguns comandos mais curtos.

# 6. Projeto

Para a implementação do projeto final, usaremos como base o seguinte [workflow](https://nvie.com/files/Git-branching-model.pdf).

O projeto é usar os [arquivos deste template web](https://drive.google.com/open?id=1Zf3Je4h6qohR2nzhMd5sMC3oTALW5bWt) e adicionar à ele um header, um footer e uma seção de compras. Para isso, os participantes deverão se dividir em três equipes e as três deverão utilizar o modelo de branches acima. Depois de baixar os arquivos, um repositório remoto deverá ser criado com os arquivos no GitHub e os integrantes de cada equipe deverão ser adicionados como colaboradores. Não será necessário layout muito sofisticados, o objetivo do curso não é esse. 

Atenção! Fique atento ao instrutor. Bugs podem ser encontrados durante o desenvolvimento!

Bom trabalho!

# 7. Quer GUI? Pois tome: Git com Visual Studio e Git Kraken


# 8. Saiba Mais


https://github.com/SlzPedroArthur/PetComp-git


[+[PETComp] Gerenciamento de versões com Git](https://paper.dropbox.com/doc/PETComp-Gerenciamento-de-versoes-com-Git-bTgJsXW85jvcl25DyANBz) 

