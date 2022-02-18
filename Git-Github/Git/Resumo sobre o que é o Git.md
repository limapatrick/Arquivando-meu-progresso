#	Git, o que é

Git é o **sistema de controle de versão** open source mais usado no mundo atualmente! Ele é usado para controlar o **histórico de alterações** de arquivos e principalmente de projetos de desenvolvimento de software. Ele permite mais flexibilidade no fluxo de trabalho, segurança e desempenho.



#	Comando do git



### 1. Git init: criando seu repositório local



O **git init** serve para que você crie o seu repositório localmente, no seu computador. Para isso, se você quiser criar um novo repositório, crie uma pasta (ou se você quiser iniciar um repositório em uma pasta que já existe, vá até ela) e digite o comando **git init** e pronto, seu repositório Git foi criado! 

### 2. Git add: adicionando alterações no repositório!

Quando você cria ou modifica arquivos, você precisa adicionar eles para a área de *staging*, para isso você usa o comando git add para adicionar todos os arquivos ou git add nome-do-arquivo. Dessa forma, os arquivos estarão prontos para serem commitados

### 3. Git commit: confirmando e salvando as alterações no repositórios!

Após você usar o **git add**, os arquivos vão para a área de commit. Você pode empacotar todas essas alterações em um único commit com uma mensagem que resume aquelas alterações. Para isso você usa o comando **git commit-m “Mensagem das alterações”**.

### 4. Git Status: verificando se há alterações na branch

O **git status** mostra o status do seu repositório naquele momento. Ele mostra o *working directory*, a *staging area* com todos os arquivos em cada uma das áreas e qual o estado de cada um deles. Isso ajuda muito quando precisamos pensar em fazer um *commit* ou até mesmo verificar quais foram todos os arquivos modificados. 



### 5. Git log: verifique quais commits foram feitos até agora

O **git log** ajuda a saber quais foram os commits feitos no seu repositório, quem fez, quando e também qual a mensagem de cada um. Além disso, esse comando te mostra a hash de cada um dos commits, o que pode ajudar a executar alguns outros comandos também. 



### 6. Git reset: desfazendo as alterações de um repositório para um commit anterior!

O **git reset** é uma forma bem complexa para desfazer alterações. Teremos um post totalmente focado para falar dele, mas para falar sobre a forma mais usada dele, vamos dar dois exemplos. O primeiro deles é quando, localmente, precisamos voltar um commit. No exemplo da imagem abaixo, temos dois commits e queremos voltar para o primeiro. Para isso, usamos o comando:



Se você perceber, após rodar esse comando, o último commit sumiu e as alterações voltaram para o *working directory*. Um outro exemplo bem usado é quando você quer voltar ao estado original que estava no repositório remoto. Importante lembrar que ao rodar esse comando, você perderá o que está localmente! Logo, rodando esse comando, você recuperará o histórico mais recente da branch main do servidor e apagará todas as alterações e commits locais.



### 7. Git revert: Desfazendo um commit sem excluir os dados existentes!

O **git revert** faz parte de comandos do tipo “desfazer”. Mas ele não é uma opção tão tradicional. Basicamente, ele cria um novo *commit* desfazendo o *commit* que você especificar.

Criei um arquivo, adicionei um texto “primeiro conteúdo” e depois adicionei outro texto “conteúdo errado”. Fiz o *revert* do “conteúdo errado” e como pode ver, ele adicionou um novo *commit* fazendo o *revert. N*esse *commit,* ele desfez as alterações do último *commit*. Ou seja, no final, o meu arquivo ficou apenas com o texto “primeiro conteúdo”.8. Git diff: verificando as diferenças entre arquivos e repositórios!

Você pode ver as diferenças dos seus arquivos ou também entre os repositórios local e remoto. Para isso, você pode rodar o comando **git diff** depois das alterações que você fizer no seu repositório local ou, se você precisar ver antes de um *merge,* por exemplo, você também pode executar git diff <branch origem branch destino



### 9. Git remote: ligando seu repositório local a um repositório remoto!

Se você não clonou um repositório, você pode ligar o seu repositório local a um servidor com o comando *remote.* Para isso, basta usar git remote add origin servidor.

### 10. Git push: enviando as alterações do repositório local para o repositório remoto!

Depois que você fez as alterações, adicionou para a área de *staging*, fez os *commits*, você pode fazer o *push*. Ou seja, você consegue mandar todas essas alterações do seu repositório local para um remoto. Para isso, use o comando **git push origin main**, no qual *main* pode ser substituúida por qualquer outra *branch* que você estiver trabalhando. 

### 11. Git branch: listando e deletando branches 

Para listar todas as branches que estão em um repositório, basta rodar **git branch**. Para deletar uma branch específica basta rodar **git branch -d nome_da_branch**.

### 12. Git checkout: criando uma nova branch e restaurando arquivos!

Para criar uma nova branch, você deve rodar o comando **git checkout -b nome_da_branch**. E, para alternar entre *branches,* basta rodar **git checkout nome_da_branch**.

Agora, se você tiver feito algo errado e quiser restaurar o arquivo ao seu estado original, você pode rodar **git checkout — nome_do_arquivo**. Mas, isso só funcionará se o arquivo ainda estiver no *working directory*. Caso já esteja na área de *staging*, você terá que, primeiro, fazer um *reset* para depois conseguir fazer um *checkout*.

### 13. Git merge: mesclando as alterações em sua branch à branch master

Quando você precisa trazer as atualizações da *branch main*, a principal, para a *branch* que você está trabalhando, basta rodar da sua *branch*: **git branch main**. Se não tiver nenhum conflito nos arquivos que você mexeu na sua *branch* com as alterações da *main*, você não terá que fazer mais nada. Agora se tiver algum conflito, vai aparecer no seu terminal que houve um conflito e quais os arquivos conflitantes. Você precisará abrir cada um deles e escolher qual versão do código você vai querer manter. 

### 14. Git pull: atualizando o repositório local com a versão do repositório remoto! 

Quando você precisa atualizar o seu repositório local com a mais nova versão do repositório remoto, basta usar o comando **git pull**. Dessa forma, ele verificará se tem uma versão mais recente e, se tiver, vai baixar as diferenças para o seu computador. 

### 15. Git rebase: integrando todas as alterações de um branch em outro branch

O **git rebase** move e combina sequências de *commits* para uma nova *branch* de uma forma mais linear. Uma das diferenças do *rebase* para o *merge* é que o *rebase* mantém esse histórico do projeto de uma forma mais linear e organizada. O comando é simples, mas todo o conceito de como ele funciona é mais complexo. Para rodar, basta usar **git rebase <branch>**. Na imagem abaixo, mostramos o que acontece com o histórico quando fazemos um rebase:



16. Git stash: criando um backup das alterações atuais do seu projeto

O **git stash** serve para guardar ou arquivar as alterações que você fez por um determinado tempo. Ele é bem útil quando você precisa mudar de contexto rápido e ainda não está pronto para fazer um *commit*, ou também quando você precisa fazer um teste de uma nova linha de pensamento] e não quer perder tudo que já fez antes de ter certeza que a nova abordagem funcionará. Para usar o comando **git stash** e para recuperar as alterações, basta usar **git stash pop**.

### 17. Git clone: baixando o código fonte de um repositório!

Você consegue clonar, ou copiar, o projeto para o seu computador. Você pode clonar um repositório localmente, fazendo uma cópia dele. Para isso, basta rodar **git clone /caminho/para/o/repositório**. Ou você também pode clonar um repositório remoto e para isso usar **git clone “url”**.

Git é algo essencial no universo da programação nos dias de hoje! Você pode achar um pouco difícil de entender no início, mas vai perceber o quanto ele vai ajudar você e seu time no dia a dia. Além de você não precisar mais ter medo de perder código ou de algo dar errado e não conseguir desfazer. Independentemente de qual área da programação você seguir, é uma ferramenta muito importante em qualquer uma delas! 
