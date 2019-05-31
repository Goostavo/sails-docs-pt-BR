# Gruntfile.js

Sails usa [Grunt](http://gruntjs.com) para gerenciamento de ativos (_assets_). Este arquivo contém o ponto de entrada para pipeline de assets padrão em Sails; qual é, o código que faz coisas como compilação de folhas de estilo em LESS, minificando scripts para produção, e precompilando e injetando templates no lado do cliente.

Integração de Sails com Grunt é altamente customizável, mas para maioria dos casos, esse arquivo (`Gruntfile.js`) deve permanecer inalterado. Ao invés disso, você pode instalar plugins de Grunt ou adicionar sua própria lógica customizada em novos arquivos no diretório [`tasks/`](./tasks).

> + Para aprender mais sobre o funcionamento de arquivos estáticos em Sails, confira a [documentação conceitual de assets](https://sailsjs.com/documentation/concepts/assets).
> + Para uma introdução mais ampla de tarefas Grunt em geral, veja [documentação de Grunt sobre configurações de tarefas](http://gruntjs.com/configuring-tasks).


<docmeta name="displayName" value="Gruntfile.js">
