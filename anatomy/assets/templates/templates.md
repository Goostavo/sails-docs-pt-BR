# assets/templates/

Templates HTML Client-side são importante pré-requisitos para certos tipos de mordenas e ricas aplicações contruídas paras os navegadores; particularmente [SPAs](https://en.wikipedia.org/wiki/Single-page_application). Para sua magia funcionar, frameworks como Backbone, Angular, Ember e Knockout requerem que você carregue template client-side; completamente separados da tradicionais [views server-side](https://sailsjs.com/documentation/concepts/views). Por convenção, novas aplicações Sails suportam o melhor dos dois mundos.

Se você utilizará ou não templates client-side em sua aplicação e onde você colocará eles, é claro, é completamente com você. Mais por convenção, novas aplicações Sails incluém pastas `templates/` por padrão para você.

### Como utilizo esses templates?

Por padrão, seu Gruntfile é configurado para automaticamente carregar e pré-compilar arquivos de template JST cliente-side em seu diretório `assets/templates`, eles incluém sua view `layout.ejs` automaticamente (entre TEMPLATES e TEMPLATES END)

    <!--TEMPLATES-->

    <!--TEMPLATES END-->

Isso expõe seus templates HTML como funções pré-compiladas em seu `window.JST` para você utilizar em seu JavaScript client-side.

Para personalizar esse comportamente para adequar a suas necessidades, você pode editr seu Gruntfile.
Por exemplo, aqui estão algumas poucas coisas que você pode fazer:

- Importar templates de outros diretórios
- Utilizar motores de templates diferentes (como handlebars, jade, dust, etc)
- Internacionalizar seus templates client-side usando stringfiles server-side antes de serem servidas.

Para mais informações, veja a documentação conceitual das [tarefas padrões do Grunt](https://sailsjs.com/documentation/concepts/assets/default-tasks) que fazem parte do asset pipeline do Sails.

<docmeta name="displayName" value="templates">
