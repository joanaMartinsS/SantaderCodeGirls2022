# Anotações sobre o Cuso de Introdução ao Git e ao GitHub

> ### *COMANDOS DE NAVEGAÇÃO VIA COMMAND LINE INTERFACE E INSTALAÇÃO*

- dir (wind) e ls (linux e macOS);
- lista os diretórios;
- cd /     - navega em uma pasta específica (ENTRA);
- cd ..      - faz o caminho inverso;
- cls (wind) e clear (linux e macOS) - limpa a tela;
- Apertar a tecla TAB autocompleta;
- mkdir     - cria pasta (diretório);
- echo  - como se fosse um print;
- ">"  - joga a saída de uma função para um local;
    - echo hello > hello.txt - vai criar um arquivo de texto de nome hello.txt que tá escrito hello;
- del - apaga arquivos (se passar uma pasta apaga todos os arquivos que estão dentro da pasta);
- setinha pra cima ou para baixo passa por todos os comandos digitados no terminal;
- rmdir - remove o repositório.
    - rmdir workspace /S /Q - remove a pasta workspace passando essas duas flags para funcionar.
    

> ### *GIT POR BAIXO DOS PANOS*

- SHA1:
    - é um tipo de encriptação;
    - gera um conjunto de 40 dígitos que funciona como de identificador;
    - é uma forma curta de interpretar um arquivo;
    - SHA1 NO GIT;
        - openssl sha1 nome do arquivo - vai criar o código de identificação
    
- BLOOS:
    - Não entendi nd
    - guarda apenas o chá do arquivo
    - Bloco básico de composição?
    - Contém metadados?

- Tree:
    - Armazena conjunto de bloos;
    - Armazena os nomes dos arquivos;
    - Aponta para bloos e para outras Trees;
    - estrutura de onde estão os arquivos;
    - Existem os SHA1s das árvores;
        - Se mudar a Tree muda o SHA1 dela e muda o SHA1 dos bloos.
        
- Commit:
    - Aponta para Tree, parente (ultimo commit realzado), autor e para uma mensagem;
    - único para cada autor;
    - faz uma espécie de linha do tempo com essa história de autor;
    
- Por que o Git é um Sistema Distribuído Seguro?
    - Todo mundo que tem arquivos e quem tem eles são seguros.
    

> ### *CHAVE SSH E TOKEN - FORMAS DE ACESSO SEGURAS*

- Chave SSH:
    - Uma forma de forma de autenticar a sua máquina para o GitHub saber que você;

- Criando Chave
    - No Git Bash;
        ```
        cd /c/Users/joana/.ssh/
        $ cat id_ed25519.pub

        ```
    
    - Adiciona a chave gerada ao GitHub na área de SSH;
    - De volta no Git Bash;
        ```
        $ pwd
        $ eval (ssh-agent -s)
        $ ssh-add id_ed25519
        ```
    - Após esses passos vai aparecer o e-mail de onde o SSH foi gerado.
    
- TOKEN:
    - É tipo uma senha que quando for solicitado você insere.
    

> ### *INICIANDO O GIT E CRIANDO UM COMMIT*

- git init no repositório dentro do repositório que você quer;
- ls - a     - mostra pastas ocultas como a pasta git;
- git config  - se for a primeira vez;
- depois do arquivo .md criado (markdown);
- git add;
- git commit -m “frase para identificar o commit” - vai ficar como se fosse um histórico de alterações;

> ### *CICLO DE VIDA - ESTADOS DE UM ARQUVIO*

- git init - inicia o git em um repositório local;
- Tracked ou untracked - git tem ciencia ou não;
- Tracked contém Unmodified, Modified e Staged;
    - Unmodified - arquvio sem modificações;
    - Modified - arquivo modificado;
    - Staged - quando adiciona a um commit ele vai pra staged e depois volta pra Unmodified - arquivos esperando algo - é tirado uma “foto” dos arquivos para que eles voltem ao estado de Unmodified;
    - Esses 3 estados são um ciclo.

- git clone + link do github para clonar um repositório para a sua máquina.

> ### CRIANDO UM REPOSITÓRIO

- Repositório criado direto no git bash
    ```
    echo "texto" > README.md
    git init
    git add README.md
    git commit -m "informações sobre o commit"
    git branch -M main
    git remote add origin "link do repositório criado pelo GitHub"
    git push -u origin main
    ```