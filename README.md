![Squiddy lê a documentação](https://sailsjs.com/images/squidford_swimming.png)

# Documentação de Sails.js

A oficial documentação para a atual versão estável de Sails está no [ramo master](https://github.com/balderdashy/sails-docs) deste repositório. Conteúdo para maioria das seções no [site oficial de Sails](https://sailsjs.com) foi compilada daqui.


## Em outros idiomas

A documentação para Sails foi traduzida para um numero diferente de idiomas. A lista abaixo é referente a tradução de projetos que estamos cientes.

| Idioma                     | [Rótulo de Idioma IETF](https://en.wikipedia.org/wiki/IETF_language_tag)  | Versão |  Mantenedor(es)        | Repositório                               |
| ---------------------------- | ------- | ------- | ------------------ | ---------------------------------- |
| Japonês                     | `ja`    | v0.11.x | [@kory-yhg](https://github.com/kory-yhg)      | [sails-docs-ja](https://github.com/balderdashy/sails-docs/tree/ja)
| Espanhol                      | `es`    | v0.12.x | [@eduartua](https://github.com/eduartua/) & [@alejandronanez](https://github.com/alejandronanez)   | [sails-docs-es](https://github.com/eduartua/sails-docs-es)
| Português do Brasil         | `pt-BR` | v1.0.x  | [@Avlye](https://github.com/Avlye) | [sails-docs-pt-BR](https://github.com/Avlye/sails-docs-pt-BR)
|                              |         | v0.10.x | [@marceloboeira](https://github.com/marceloboeira)   | [sails-docs-pt-BR](https://github.com/balderdashy/sails-docs/tree/pt-BR)
| Mandarim Taiwanês           | `zh-TW` | v0.10.x | [@CalvertYang](https://github.com/CalvertYang)   | [sails-docs-zh-TW](https://github.com/balderdashy/sails-docs/tree/zh-TW)
| Coreano                       | `ko`    | v0.10.x | [@sapsaldog](https://github.com/sapsaldog)   | [sails-docs-ko](https://github.com/balderdashy/sails-docs/tree/ko)
| Chinês                      | `zh-cn`    | v0.12.x | [@linxiaowu66](https://github.com/linxiaowu66)   | [sails-docs-zh-cn](https://github.com/linxiaowu66/sails-docs-zh-cn)
| Francês                       | `fr`    | v0.12.x | [@marrouchi](https://github.com/marrouchi)   | [sails-docs-fr](https://github.com/marrouchi/sails-docs-fr)


> Enquanto nós estamos usando ramos para manter diferente versões da documentação, nos afastamos da abordagem original de ramos para diferentes idiomas. Antes de embarcar com uma nova tradução do projeto, nós pedimos para que revise a [informação de atualização abaixo](#how-can-i-help-translate-the-documentation) -- o processo mudou um pouco.



## Contribuindo para documentação de Sails

Nós agradecemos sua ajuda! Por favor mande uma pull request para **master** com as correções/adições e eles irão re-checar e atualizaram assim que possível.

Segundamente, nós estamos abertos para sugestões sobre o processo que usamos para gerenciar nossa documentação, e trabalhar com a comunidade em geral. Por favor, publique ao Grupo no Google com suas ideias- ou se estiver interessado em ajudar diretamente, contate @fancydoilies, @rudeboot, ou @mikermcneil no Twitter.

#### Que ramo devo editar?

<!-- Com o lançamento da nova versão de Sails chegando, nós pedimos para que todas pull requests sejam feitas ao ramo `1.0`, até que o conteúdo da documentação 0.12 seja substituída no site principal. A única exceção é se você estiver documentando algo que não é relevante para Sails v1. -->

Para fazer edições que sejam relevantes a versão estável de Sails (ex: a versão em [NPM](npmjs.org/package/sails)), você irá querer editar o ramo `master` _deste_ repositório (que você vê no repositório sails-docs por padrão). O time principal de Sails atualiza o master nos ramos apropriados para última versão estável de Sails, e assim disponibiliza em sobre de sailsjs.com uma vez por semana.
 
 <!-- Isso depende de que tipo de edição você está fazendo. Mais comumente, você fará edições que são relevantes para última versão estável de Sails (como exemplo, a versão em [NPM](npmjs.org/package/sails)) e então queira editar o ramo `master` __desse__ repositório (que pode encontrar por padrão no repositório sails-docs). O time de documentação funde o master dentro do ramo apropriado para a última versão estável disponível de Sails, e então implementa no sailsjs.com uma vez por semana.

Por outro lado, se você está editando recursos não disponíveis relacionados a próxima versão; mais comumente como acompanhamento uma proposta de recurso ou uma pull request aberta de Sails ou um projeto relacionado, então você deva querer editar o ramo de próximas versões disponíveis de Sails (algumas vezes chamada de "edge").
-->

| Ramo (em `sails-docs`)                                          | Documentação de Sails versão...                                                     | Acessível em...   |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------|:-------------------|
| [`master`](https://github.com/balderdashy/sails-docs/tree/master) | _Bleeding edge_                                                                        | [`next.sailsjs.com`](https://next.sailsjs.com)
| [`1.0`](https://github.com/balderdashy/sails-docs/tree/1.0)       | [![NPM version](https://badge.fury.io/js/sails.png)](http://badge.fury.io/js/sails)    | [`sailsjs.com`](https://sailsjs.com)
| [`0.12`](https://github.com/balderdashy/sails-docs/tree/0.12)     | Sails v0.12.x                                                                          | [`0.12.sailsjs.com`](https://0.12.sailsjs.com)
| [`0.11`](https://github.com/balderdashy/sails-docs/tree/0.11)     | Sails v0.11.x                                                                          | [`0.11.sailsjs.com`](http://0.11.sailsjs.com)


#### Como é compilada essa documentação e publicada ao site?

Nós usamos um módulo chamado `doc-templater` para converter os arquivos .md em HTML para o site. Você pode aprender mais como funciona no [repositório doc-templater](https://github.com/uncletammy/doc-templater).

Cada arquivo .md tem sua própria página no site (ex: todas referências, conceitos e arquivos de anatomia), e devem incluir um rótulo especial `<docmeta name="displayName">` com uma propriedade `value` específica ao título da página. Isto impactará como a página da dcoumentação aparecerá nos resultadores de motores de busca, e será usado para mostrar o nome no menu de navegação de sailsjs.com. Por exemplo:

```markdown
<docmeta name="displayName" value="Construindo Pudins Caseiros Personalizados">
```

#### Quando minhas mudanças aparecerão no site de Sails?

Mudanças na documentação serão disponiblizadas quando eles forem unificados em um ramo especial correspondente a versão estável de Sails (ex: 0.12). Nós não podemos unificar pull request mandadas diretamente a esse ramo-- seu único propósito é refletir o conteúdo correspondendo ao hospedado em sailsjs.com, e conteúdo é apenas unificado apenas antes de reimplementar no site de sails. 

Se você quer ver como as mudanças na documentação aparecerão em sailsjs.com, você pode visitar [preview.sailsjs.com](http://preview.sailsjs.com). O site de pré-visualização atualiza automaticamente com as mudanças unidas no ramo master de sails-docs.

#### Como posso ajudar a traduzir a documentação?

Um bom jeito de ajudar o projeto Sails, especialmente se você fala outro idioma além de Inglês nativamente, é voluntariar para traduzir a documentação Sails. Se você está interessado em colaborar com qualquer projeto de tradução listado na tabela abaixo, contate os mantenedores do projeto de tradução usando as instruções em README no fork.

Se seu idioma não está representado na tabela acima, e você está interessado em começar um projeto de tradução, siga estes passos:

+ Faça um fork desse repositório (`balderdashy/sails-docs`) e mude o nome de seu fork para `sails-docs-{{IETF}}` onde {{IETF}} é o [rótulo IETF](https://en.wikipedia.org/wiki/IETF_language_tag) de seu idioma.
+ Edite o README para resumir seu progresso até então, providenciando qualquer outra informação que você que ajude outros lendo sua tradução, e deixe contribuidores interessados saber como contatar você.
+ Mande uma pull request editando a tabela acima para o link de seu fork.
+ Quando estiver satisfeito com sua primeira versão completa de sua tradução, abra uma pergunta e alguém de nosso time de documentação ajudará contentamente a obter uma pré-visualização no contexto do site de Sails, obtenha um domínio (seu, ou um subdomínio em sailsjs.com, qualquer que faça mais sentido), e compartilhe com o resto da comunidade Sails.


#### Com o que mais posso ajudar?

Para mais informações na contribuição de Sails em geral, veja o [Guia de Contribuição](sailsjs.com/contributing).


## Licença

[MIT](./LICENSE.md)

O [framework Sails](https://sailsjs.com) é livre e de código aberto sobre a [Licença MIT](https://sailsjs.com/license).

_(E esses arquivos desse repositório também são.)_

