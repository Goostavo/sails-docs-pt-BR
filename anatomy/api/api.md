# api/

Este diretório contém uma grande maioria da lógica back-end de sua aplicação. É o lar para o 'M' e o 'C' em um <a href="http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller" target="_blank">Framework MVC</a>.

Nele você encontrará os seguintes:

- Controllers: [Ações](https://sailsjs.com/documentation/concepts/actions-and-controllers) contém lógica back-end que lidará com a chegada de requisições (como lidar com o envio de um formulário ou respondendo com HTML personalizado, renderizado pelo servidor).

- Helpers: [Auxiliares](https://sailsjs.com/documentation/concepts/helpers) são funções compartilhadas que podem ser chamadas de qualquer lugar de sua aplicação.

- Models: [Modelos](https://sailsjs.com/documentation/concepts/models-and-orm) são estruturas que contém dados de sua aplicação Sails.

- Policies: [Policies](https://sailsjs.com/documentation/concepts/policies) são middleware que restrigem o acesso para certas ações de sua aplicação.

Você também pode encontrar essas pastas, que nem sempre são geradas por padrão em aplicações Sails:

- Hooks: [Hooks](https://sailsjs.com/documentation/concepts/extending-sails/hooks) são módulos que adicionam funcionalidade ao núcleo do Sails. Você pode utilizar hooks para executar código personalizado quando sua aplicação inicia e antes de lidar com a chegada de cada requisição. Hooks também podem ser instalados como plugins, mas os hooks nessa pasta sempre são personalizados para sua aplicação.

- Responses: [Respostas personalizadas](https://sailsjs.com/documentation/concepts/extending-sails/custom-responses) podem ajudar a manter comportamentos e código de status HTTP consistentes em sua aplicação. (Como nem toda aplicação Sails precisa definir suas próprias respostas personalizadas, essa pasta às vezes é excluída.

- Services: [Serviços](https://sailsjs.com/documentation/concepts/services) são utilitários compartilhados em comum em suas aplicações Sails escritas antes da versão 1.0. Eles podem ser _praticamente qualquer coisa_, então para novas aplicações, é recomendado que utilize [helpers](https://sailsjs.com/documentation/concepts/helpers) ao invés disso.

<docmeta name="displayName" value="api">

