# assets/styles/importer.less

Por padrão, novos projetos Sails são configurados para compilar esse arquivo de LESS para CSS. Diferente de outros arquivos CSS, arquivos LESS não são compilados e incluídos automaticamente ao menos que sejam importados aqui.

Os arquivos LESS importados neste arquivo são compilados e incluídos na medida que são listados. Mixins, variáveis, etc. devem ser importadas primeiro para que possam ser acessadas por páginas de estilo LESS subsequentes.

(Assim como o resto da pipeline de assets empacotada em Sails, você sempre omitir, personalizar, ou substituir esse comportamento com SASS, SCSS, ou quaisquer outras tarefas Grunt que quiser.) 


<docmeta name="displayName" value="importer.less">
