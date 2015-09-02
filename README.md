# hyouka

Free theme for [Ghost](http://github.com/tryghost/ghost/) prepared by [Spin](http://dzx.me/).


This theme is derived from [Portfolio-Free-Ghost-Theme-v.1.2.0](http://portfolio-gk.ghost.io), provided by [GavickPro](http://www.gavick.com/). Greate Thanks for so awsome free theme!  

I'm trying to modify it !  

##v0.0.1
1. jiathis support  (default.hbs & post.hbs & assets/css/main.css)  
2. change &lt;pre>&lt;/pre> and &lt;code>&lt;/code> style  
3. some detail modification  

##v0.0.2
1. upgrade to Portfolio v1.4.0 to support built in navigation  
2. tag cloud support  
	*note that files in the `core` directory should not be placed into themes!!!! Do the follows:*  
2.1 add `core/core-server-helpers tag_cloud.js` to `ghost/core/server/helpers/tag_cloud.js`  
	this is the tags api call to generate all tags  
2.2 add `core/core-server-helpers-tpl tag_cloud.hbs` to `ghost/core/server/helpers/tpl/tag_cloud.hbs`  
	this is the tag_cloud template  
	you can use {{tag_cloud}} to generate the html content in the template, and you can modify it as you like  
2.3 modify the `ghost/core/server/helpers/index.js` file:  
	add `coreHelpers.tag_cloud = require('./tag_cloud');`  (about line 40)  
	add `registerAsyncThemeHelper('tag_cloud', coreHelpers.tag_cloud);`  (about line 121)  
	*see `core-server-helpers index.js` as reference*
