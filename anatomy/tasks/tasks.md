# tasks/

O diretório `tasks/` é uma suíte de tarefas Grunt e suas configurações, embutidas para sua conveniência. A integração Grunt é principalmente útil para unir assets front-end (como folhas de estilo, scripts e templates de marcação), mas também é usado para executar todo tipo de tarefa de desenvolvimento, de compilação browserify a migrações de banco de dados.

Se você nunca usou [Grunt](http://gruntjs.com/) antes, tudo bem! Para maioria dos casos comum de uso, você pode usá-lo sem nenhuma customização ou até mesmo olhando os arquivos neste diretório. Se você precisar personalizar algo, tenha certeza de confirir o guia de [Começando com Grunt](http://gruntjs.com/getting-started), explica conceitos básicos como o [Gruntfile](http://gruntjs.com/sample-gruntfile) como também como instalar e usar plugins Grunt. Quando estiver familiarizado com o processo, siga em frente!


### Como isto funciona?

O pipeline de assets incluso em Sails é uma série de tarefas Grunt configuradas com os padrões convencionais designados para fazer seu projeto mais consistente e produtivo.

Todo fluxo de trabalho de assets front-end em Sails é completamente personalizável-- enquanto ele provê algumas sugestões fora da caixa, Sails não faz pretensão que antecipe todas as necessidades que encontrará construindo uma porção baseada-no-browser/front-end de sua aplicação. Quem vai dizer que você está criando uma aplicação para um navegador?


### Que tarefas Sails executa automaticamente?

Sails executa algumas dessas tarefas (certamente os no diretório `tasks/register/`)

###### `sails lift`

Executa a tarefa `default` (`tasks/register/default.js`).

###### `sails lift --prod`

Executa a tarefa `prod` (`tasks/register/prod.js`).

###### `sails www`

Executa a tarefa `build` (`tasks/register/build.js`).

###### `sails www --prod` (produção)

Executa a tarefa `buildProd` (`tasks/register/buildProd.js`).

### Posso personalizar isto para SASS, Angular, templates lado do cliente em Jade, etc?

Você pode modificar, omitir, ou trocar qualquer uma dessas tarefas Grunt que encaixem seus requisitos. Você pode também adicionar tarefas Grunt- apenas adicione um arquivo `algumaTask.js` no diretório `grunt/config` para configurar uma nova tarefa, então registre a(s) tarefa(s) pai apropriadas (veja os arquivos em `grunt/register/*.js`).


### Tenho que usar Grunt?

Nope! O time principal de Sails tem usado Grunt em projetos do mundo real a cerca de 4 anos, e em geral está sendo uma ferramenta fantástica. Mas percebemos que não é para todo mundo. Para desabilitar a integração Grunt em Sails, apenas delete seu Gruntfile ou [desabilite o hook de Grunt](https://sailsjs.com/documentation/concepts/assets/disabling-grunt).

> Você também pode [gerar uma nova aplicação Sails sem Grunt através do parâmetro `--without=grunt`](https://sailsjs.com/documentation/reference/command-line-interface/sails-new).

### Se eu não estiver construindo um frontend web?

Tudo bem! Um inquilido principal de Sails é agonóstidade de cliente-- é especialmente desenhado para construir APIs usadas para todos tipos de clientes; Android/iOS/Cordova nativos, SDKs do lado do servidor, etc.

Você pode completamente desabilitar Grunt atráves das instruções [aqui](https://sailsjs.com/documentation/concepts/assets/disabling-grunt).

Se você ainda deseja usar Grunt para outros propósitos, mas não quer quaisquer front-end web padrão, apenas delete seu diretório `assets` de seu projeto e remova o front-end orientado a tarefas do diretório `grunt/register` e `grunt/config`. Você também pode executar `sails new myCoolApi --no-frontend` para omitir a pasta de `assets` e front-end orientado a tarefas Grunt de futuros projetos. Você também pode trocar seu módulo `sails-generate-frontend` com um gerador alternativo da comunidade, ou criar seu próprio. Isto permite `sails new` criar um boilerplate de apps iOS nativos, apps Android, apps Cordova, apps SteroidsJS, etc.

> Se você _nunca_ precisará de qualquer tipo de frontend web, você pode também [gerar uma aplicação com o parâmetro `--no-frontend`](https://sailsjs.com/documentation/reference/command-line-interface/sails-new).


### Mais informações

> Mais informações sobre o uso de Grunt para trabalhar com assets estáticos: http://gruntjs.com/configuring-tasks



<docmeta name="displayName" value="tasks">

