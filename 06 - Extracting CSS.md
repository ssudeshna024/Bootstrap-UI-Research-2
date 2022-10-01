# Extracting CSS 
The style-loader we configured above conveniently emits CSS into the bundle so that manually loading a CSS file in dist/index.html isn’t necessary. This approach may not work with a strict Content Security Policy, however, and it may become a bottleneck in your application due to the large bundle size.
