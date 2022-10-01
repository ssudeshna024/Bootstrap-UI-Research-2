# Extracting CSS 
The style-loader we configured above conveniently emits CSS into the bundle so that manually loading a CSS file in dist/index.html isn’t necessary. This approach may not work with a strict Content Security Policy, however, and it may become a bottleneck in your application due to the large bundle size.

To separate the CSS so that we can load it directly from dist/index.html, use the mini-css-extract-loader Webpack plugin.

First, install the plugin:


> npm install --save-dev mini-css-extract-plugin

Then instantiate and use the plugin in the Webpack configuration:


> ### Look into code 4.html

After running npm run build again, there will be a new file dist/main.css, which will contain all of the CSS imported by src/js/main.js. If you view dist/index.html in your browser now, the style will be missing, as it is now in dist/main.css. You can include the generated CSS in dist/index.html like this:

> ### Look into code 5.html

