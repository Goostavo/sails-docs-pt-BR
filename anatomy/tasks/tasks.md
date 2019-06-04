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


### Do I have to use Grunt?

Nope!  The Sails core team has used Grunt on real-world projects for upwards of 4 years now, and overall it's been a fantastic tool.  But we realize it's not for everyone.  To disable Grunt integration in Sails, just delete your Gruntfile or [disable the Grunt hook](https://sailsjs.com/documentation/concepts/assets/disabling-grunt).

> You can also [generate a new Sails app `--without=grunt`](https://sailsjs.com/documentation/reference/command-line-interface/sails-new).


### What if I'm not building a web frontend?

That's ok! A core tenant of Sails is client-agnosticism-- it's especially designed for building APIs used by all sorts of clients; native Android/iOS/Cordova, serverside SDKs, etc.

You can completely disable Grunt by following the instructions [here](https://sailsjs.com/documentation/concepts/assets/disabling-grunt).

If you still want to use Grunt for other purposes, but don't want any of the default web front-end stuff, just delete your project's `assets` folder and remove the front-end oriented tasks from the `grunt/register` and `grunt/config` folders.  You can also run `sails new myCoolApi --no-frontend` to omit the `assets` folder and front-end-oriented Grunt tasks for future projects.  You can also replace your `sails-generate-frontend` module with alternative community generators, or create your own.  This allows `sails new` to create the boilerplate for native iOS apps, Android apps, Cordova apps, SteroidsJS apps, etc.

> If you know you'll _never_ need any kind of web frontend, you can also [generate a new Sails app with `--no-frontend` at all](https://sailsjs.com/documentation/reference/command-line-interface/sails-new).


### Mais informações

> Mais informações sobre o uso de Grunt para trabalhar com assets estáticos: http://gruntjs.com/configuring-tasks



<docmeta name="displayName" value="tasks">

