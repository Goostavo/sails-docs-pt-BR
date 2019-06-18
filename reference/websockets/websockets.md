# WebSockets

Para a discussão completa dos conceitos de tempo-real em Sails, veja a [documentação de conceito Realtime](https://sailsjs.com/documentation/concepts/realtime).

Para informações da comunicação socket cliente-para-servidor, veja [Cliente Socket (sails.io.js)](https://sailsjs.com/documentation/reference/web-sockets/socket-client).

Para informações da comunicação socket servidor-para-cliente, veja [sails.sockets](https://sailsjs.com/documentation/reference/web-sockets/sails-sockets).

Para informações no uso de mensagens em tempo-real para comunicar mudanças nos modelos Sails, veja [Referência Engenhosa PubSub](https://sailsjs.com/documentation/reference/web-sockets/resourceful-pub-sub).

Sails usa [socket.io](http://socket.io) como motor fundamental para comunicação em tempo-real. Toda aplicação Sails tem uma instância socket.io disponível como `sails.io`. Entretanto, maior funcionalidade de `socket.io` é envolvida por conveniência (e segurança) pelo método `sails.sockets`.

<docmeta name="displayName" value="WebSockets">

