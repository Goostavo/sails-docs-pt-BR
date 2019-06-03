# tasks/pipeline.js

O arquivo `pipeline.js` em sua aplicação Sails determina a ordem que suas folhas de estilo, 
JavaScript, e template do lado do cliente deverão ser compiladas e acopladas 
como tags de `<script>` ou `<link>`.

Se você não quer depender de um [acoplado de assets automático](https://sailsjs.com/documentation/concepts/assets/task-automation#?asset-pipeline), então você pode seguramente ignorar esse arquivo.

> Nota que você pode tomar vantagem das expressões wildcard/glob/splat dos estilos Grunt para corresponder a múltiplos arquivos, e usar `!` em frente das expressões para ignorar os arquivos.


<docmeta name="displayName" value="pipeline.js">
