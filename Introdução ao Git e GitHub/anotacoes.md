# Anotações resumidas do curso de Introdução ao Git e GitHub - DIO



#### 1. Comandos no terminal do Windows (CMD):

- **DIR:** lista os diretórios da pasta 

- **cd:** comando para navegar entre as pastas/diretórios

  - cd *nome_da_pasta* : nos leva para *nome_da_pasta* 
  - cd / : nos leva ao início
  - cd .. : volta 1 nível

- **cls:** limpar o terminal (no Linux e no Git Bash usamos o atalho CRTL+L)

- **mkdir:** cria novo diretório

- **echo:** *printa* a mensagem escrita

  - echo *hello*: devolve a mensagem *hello*
  - echo *hello* > hello.txt : cria um arquivo .txt na pasta 

- **del:** deleta arquivo dentro de um diretório, não o diretório em si

- **rmdir:** deleta um diretório

  - rmdir *workspace* /S /Q

    

#### 2. Introdução ao Git

- **SHA1** é a encriptação usada pelo Git. Cria um código único de 40 caracteres. A cada modificação no objeto, há uma mudança no código, sendo importante para saber se houve alguma modificação.

- Tipos de **objetos do Git**:

  - **blobs:** guarda o SHA1 do arquivo; é o objeto mais "básico"; apresenta metadados.

  - **tree:** armazenam os blobs; também contém metadados; guarda o nome do arquivo e o SHA1; pode apontar para blob ou para outra tree.

  - **commit:** é o principal objeto do Git; pode apontar para blob, tree ou commit; guarda o nome do criador e o tempo em que foi criado.

    

#### 3. Primeiros comandos com Git

- **git init:** inicializa um repositório vazio no diretório em que se está trabalhando
  - ls -a : mostra pastas ocultas
- **git config:** utilizado para configurar o email e username antes de fazer o commit
  - git config --global user.email *email_do_usuario*
  - git config --global user.name *apelido_do_usuario*
- **git add:** diz ao Git que você quer incluir atualizações no próximo commit; torna o arquivo *staged*.
  - git add * : inclui tudo
- **git commit:** cria um commit; "salva" o conjunto de mudanças realizadas; muda o arquivo de *staged* (após usar *git add*) para *unmodified* e manda para o repositório local.
  - git commit -m "*alguma descrição sobre o commit*"
- **git status:** fornece informações sobre o *branch* em que você estiver no momento, como o nome, se está atualizada em relação à *master* e quais arquivos foram alterados.
- **git push:** publica as modificações no repositório remoto (GitHub).
  - git push origin main
- **git pull:** usado para buscar e baixar o conteúdo de repositórios remotos e realizar a atualização imediata no repositório local, para que os conteúdos fiquem iguais.
- **git clone:** faz uma cópia de um repositório remoto (GitHub) para um repositório local
  - git clone *link_do_repositorio* 



