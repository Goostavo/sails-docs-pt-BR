# views/pages/homepage.ejs

Esse é o real template que é renderizado por padrão quando um usuário visita a URL base de sua aplicação levantada. Notou a extensão do arquivo? Significa [Embedded JavaScript](http://ejs.co/). EJS é o que Sails usa por padrão para renderizar views HTML do lado do servidor. Isto pode ser mudado em `config/views.js`.

Se uma nova view que você criou não está sendo renderizada, tenha certeza de configurá-la em seu `config/routes.js`.

Se você está acostumado a colocar todo o seu HTML em um único arquivo, isso pode parecer engraçado. Você deve pensar "Onde estão as tags de Head e Body?". A resposta é, `views/layouts/layout.ejs`.


<docmeta name="displayName" value="homepage.ejs">
