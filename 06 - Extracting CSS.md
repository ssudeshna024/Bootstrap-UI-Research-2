# Extracting CSS 
The style-loader we configured above conveniently emits CSS into the bundle so that manually loading a CSS file in dist/index.html isn’t necessary. This approach may not work with a strict Content Security Policy, however, and it may become a bottleneck in your application due to the large bundle size.

To separate the CSS so that we can load it directly from dist/index.html, use the mini-css-extract-loader Webpack plugin.

First, install the plugin:


> npm install --save-dev mini-css-extract-plugin

Then instantiate and use the plugin in the Webpack configuration:


> ### Look into code 4.html
