### Tarefa 003: Git Exercícios - 03/06/2021.

Responda as questões abaixo (exercite os comandos do git correspondentes). Lembre-se de que o “interessante” não é exatamente o conjunto de respostas, mas o processo de obtê-las e a experiência obtida com a execução dos comandos.


1. Qual o comando para obter a versão instalada do Git?
   - o comando utilizado para obter a versão instalada do git é 
   ```
    git --version
   ```
2. Qual o efeito da execução de cada um dos comandos abaixo?
   - a. git help
     - O comando git help exibe uma lista de comandos comuns utilizados juntamente com as descrições das funcionalidades de alguns comandos 
   - b. git help checkout
     - O comando git help checkout exibe as especificações de uso do comando checkout
   - c. git help merge
     - O comando git help merge exibe as especificações de uso do comando merge 
   - d. git init
     - O comando git init serve para iniciar um novo projeto que utilizará git 
   - e. git add --all
     - O comando git add adiciona todos os novos arquivos e alterações feitas em arquivos existentes ao projeto, a descrição dada pelo git sobre esse comando diz que "ele adiciona todas as atualizações ao index"
   - f. git add -u
     - O comando git add -u também realiza a ação de atulizar o projeto com os alterações que foram feitas, porem, ele não adiciona novos arquivos caso eles existam
   - g. git config -l
     - O comando git config -l exibe uma lista contendo todas as variáveis existentes no arquivo de configuração do git 
   - h. git mv a.txt b.txt
     - A execução do comando acima irá alterar o nome do arquivo a.txt para b.txt
   - i. git reset --hard
     - O comando reset --hard irá resetar o projeto, revertendo commits e apagando arquivos que haviam previamente sido adicionados 
   - j. git log -27
     - O comando git log -27 irá exibir o histórico dos últimos 27 commits
3. O fluxo “clássico” de interação com o Git é algo como “alterar um ou mais arquivos”, “acrescentar essas mudanças para serem contemplados no próximo commit” e, finalmente, executar um “commit”. Quais os comandos necessários para realizar os dois últimos “passos” desse fluxo?
   - Os comandos necessários para realizar os dois últimos passos são respectivamente:
     ```
      git add
      git commit
     ```
     Para adicionar todas as alterações feitas, e depois realizar um commit contendo uma mensagems podemos executar esses comandos da seguinte forma 
     ```
      git add .
      git commit -m "Mensagem do commit"
     ```
4. Qual o comando deve ser executado para identificar o que foi alterado desde o último “commit”?
   - O comando utilizado para monitorar as modificações feitas entre commits é 
     ```
      git diff
     ```
5. Em um dado repositório, arquivos simplesmente copiados para lá, ou seja, _untracked_, podem ser exibidos/identificados com que comando?
   - É possível identifica-los apartir do seguinte comando git
     ```
      git status
     ```
6. Qual o comando para efetuar um _commit_?
   - O comando usado para realizar um commit é o comando 
     ```
      git commit
     ```
7. Qual o comando que devemos empregar para descartar mudanças ocorridas no arquivo teste.txt, por exemplo?
   - Podemos descartar mudanças feitas no arquivo teste.txt com o seguinte comando 
     ```
      git reset teste.txt
     ```
8. O que deve ser feito para que um determinado diretório do seu repositório seja ignorado pelo Git? Faça uma busca por **.gitignore**.
   - Para que um determinado diretário seja igorado precisamos criar um arquivo com o nome **.gitignore** e adicionar os diretórios que devem ser ignorados q esse arquivo 
9. O que acontece se o seu repositório local for acidentalmente removido?
   - Caso esse repositório esteja hospedado em um repositório no github é possível clona-lo para sua máquina recuperando o que foi perdido 
10. Como clonar um repositório remoto?
    - É possível clonar um repositório utilizando o seguinte comando 
      ```
       git clone 
      ```
      seguindo do link referente ao repositório
11. Em alguns cenários **git log** pode produzir extensos resultados. Se houver interesse em visualizar o histórico de um repositório, onde cada mudança é fornecida exatamente em uma única linha, qual o comando que deve ser empregado?
    - O comando usado para realizar essa tarefa é o seguinte 
      ```
       git log --oneline
      ```
12. Em qual arquivo o Git armazena informações de configuração empregadas por usuário?
    - Ele armazena em um arquivo com o nome "config" dentro da pasta .git
13. Qual o comando para criar um repositório local?
    - O comando usado para criar um repositório local é o comando
      ```
       git init
      ```
14. Qual o nome do diretório criado pelo Git quando se executa o comando **git init**?
    - O repositório criado pelo git ao executar esse comando leva o nome de .git 
15. Qual o comando para adicionar todos os arquivos modificados? (Aqueles para os quais **git status** identificam como **modified**?)
    - O comando utilizado para adicionar todos os arquivos modificados é 
      ```
       git add .
      ```
16. O Git faz uso do valor de hash conhecido por SHA1. O que isto significa? Qual o propósito? O que é SHA1?
    - O função SHA1 é uma função utilizada para criptografar valores, gerando hashes
17. Qual a palavra para indicar o último _commit_ em vez do valor de hash SHA1 correspondente?
    - Palavra usada é -abbrev-commit, ela pode ser utilizada da seguinte forma
      ```
       git log --abbrev-commit
      ```
18. Quando se cria dois arquivos usando um editor de texto qualquer e, na sequência, executamos o comando **git add -u**, os dois arquivos criados passam de _untracked_ para _new file_?
    - Não, os arquivos continam como _untracked_
19. Qual o efeito da execução dos dois comandos abaixo, nesta ordem, em um dado repositório?
**git reset --soft HEAD~1**
**git reset --hard**
    - A execução do comando 
      ```
       git reset --soft HEAD~1
      ```
      irá reverter o ultimo commit mantendo qualquer alteração feita ou arquivo adicionado como mudanças a serem submetidas. E a execução do comando 
      ```
       git reset --hard
      ```
      irá apagar qualquer mudança que está em estado de ser submetida.
20. Após o emprego de um ambiente integrado de desenvolvimento (IDE), é comum a criação de arquivos e diretórios. Qual o comando que podemos empregar para remover arquivos e diretórios _untracked_?
    - Para realizar essa tarefa podemos utilizar o seguinte comando 
      ```
       git clean -fxd
      ```
21. Qual o nome do arquivo no qual podemos inserir a indicação para o Git de arquivos e diretórios a serem ignorados?
    - O nome desse arquivo é ".gitignore"
22. Quando se cria o arquivo _MinhaClasse.class_ em um dado diretório e desejamos que arquivos com a extensão .class, como neste caso, sejam ignorados por todos os membros de uma equipe que estão contribuindo com um dado projeto, como devemos proceder?
    - Devemos incluir ao arquivo .gitignore a seguinte sintaxe '*.class' para que ele ignore todos os arquivos com a extenção class
23. jQuery é uma famosa biblioteca em JavaScript. Consulte detalhes em [jQuery](http://jquery.com). O repositório correspondente encontra-se em [gitRep](https://github.com/jquery/jquery.git). Faça o clone deste repositório.
24. No repositório **jqueryrepo**, criado no passo anterior, qual o efeito do comando
**git shortlog -sne**?
    - Esse comando exibq uma lista contendo os últimos commits que foram feitos, juntamente o nome e email dos usuários que realizaram esses commits 
25. No repositório **jqueryrepo**, qual o efeito de **git remote -v**?
    - Esse comando exibe o endereço dos repostórios remotos aos quais o projeto está associado
26. Um repositório Git pode ser etiquetado ao longo do tempo. Ou seja, _commits_ específicos podem ser “marcados” ou “etiquetados” para facilitar referências posteriores. Para listar todas as “etiquetas” (_tags_) estabelecidas para um dado repositório, qual comando deve ser executado?
    - O comando utilizado para listar as tags de um projeto é o sequinte comando
      ```
       git tag
      ```
27. Caso um dato repositório retorne muitas “marcas” ou “etiquetas” para o comando **git tag**, como retornar apenas aquelas que atendem a determinado padrão, por exemplo, iniciadas por 2.0?
    - Para realizar essa tarefa podemos executar o comando git tag da seuinte forma
      ```
       git tag -l '2.0*'
      ```
28. Qual o efeito do comando **git tag -a 3.4-gold -m “minha versão ouro”**?
    - O git nos retorna uma mensagem dizendo "fatal: too many params" indicando que forma passados parâmetros em excesso
29. Após executado o comando acima, qual o efeito de **git show 3.4-gold**?
    - O git nos retorna uma mensagem dizendo "fatal: ambiguous argument '3.4-gold': unknown revision or path not in the working tree."
30. O que o comando **git push origin 3.4-gold** teria como efeito?
    - Caso existisse uma branch com esse nome poderiamos enviar qualquer commit feito locamente para essa branch no repositório remoto
31. Após executar um commit, qual o efeito de **git commit --amend**?
    - A excução desse comando permite a edição do último commit feito
32. Após executar **git add x.txt**, qual o efeito de **git reset HEAD x.txt**?
    - Esse último comando retorna o arquivo x.txt para o estado de _untracked_
33. Após alterar o conteúdo de um arquivo committed em passo anterior, qual o efeito do comando **git checkout -- a.txt**?
    - Ele retornará ao estado anterior as mudanças realizadas no arquivo a.txt
34. Qual a diferença entre os comandos **git reset HEAD a.txt** e **git checkout -- a.txt**?
    - O primeiro leva em consideração as mudanças realizadas no projeto e o segundo leva em consideração as mudanças realizadas naquele arquivo específico
35. Veja como interpretar o resultado de git diff [aqui](https://medium.com/therobinkim/how-to-read-a-git-diff-6c87a9dc47c5). Execute, em um dos seus projetos, o comando **git diff HEAD~1 HEAD** e certifique-se de que entende o resultado apresentado.

</DIV/>
