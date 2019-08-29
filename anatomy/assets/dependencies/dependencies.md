# assets/dependencies/

Como um princípio básico, se o código é escrito por você ou alguém de seu time, ele _não pertence a este diretório._ Ao invés disso, `assets/dependencies/` é para suas dependências `client-side` como Vue.js, Bootstrap, ou jQuery. Este diretório pode incluir arquivos `client-side` como JavaScript, folhas de estilo, ou até imagens. (Veja o modelo "Aplicação Web" por exemplo.)

Arquivos JavaScript e folhas de estilo no diretório `assets/dependencies/` são carregadas primeiro, antes de seus assets. Esta convenção é um comportamento orquestrado por [tasks/pipeline.js](https://sailsjs.com/documentation/anatomy/tasks/pipeline.js), então vá lá se precisar ajustar esse comportamento (como exemplo, se alguma de duas dependências precisa ser carregada antes de outras.)

<docmeta name="displayName" value="dependencies">

