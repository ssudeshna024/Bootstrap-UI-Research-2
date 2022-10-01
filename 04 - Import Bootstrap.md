Import Bootstrap 
Importing Bootstrap into Webpack requires the loaders we installed in the first section. We’ve installed them with npm, but now Webpack needs to be configured to use them.

- Set up the loaders in webpack.config.js. Your configuration file is now complete and should match the snippet below. The only new part here is the module section.


> ### Look into code 3.html

Here’s a recap of why we need all these loaders. style-loader injects the CSS into a < style > element in the < head > of the HTML page, css-loader helps with using @import and url(), postcss-loader is required for Autoprefixer, and sass-loader allows us to use Sass.

- Now, let’s import Bootstrap’s CSS. Add the following to src/scss/styles.scss to import all of Bootstrap’s source Sass.


> // Import all of Bootstrap's CSS
> @import "~bootstrap/scss/bootstrap";

You can also import our stylesheets individually if you want. [Read the Sass import docs](https://getbootstrap.com/docs/5.2/customize/sass/#importing) for details.

- Next we load the CSS and import Bootstrap’s JavaScript. Add the following to src/js/main.js to load the CSS and import all of Bootstrap’s JS. Popper will be imported automatically through Bootstrap.


> // Import our custom CSS

> import '../scss/styles.scss'

> // Import all of Bootstrap's JS

> import * as bootstrap from 'bootstrap'

You can also import JavaScript plugins individually as needed to keep bundle sizes down:


> import Alert from 'bootstrap/js/dist/alert'

> // or, specify which plugins you need:

> import { Tooltip, Toast, Popover } from 'bootstrap'

[Read the JavaScript docs](https://getbootstrap.com/docs/5.2/getting-started/javascript/) for more information on how to use Bootstrap’s plugins.

- And you’re done! 🎉 With Bootstrap’s source Sass and JS fully loaded, your local development server should now look like this.

<img src="https://getbootstrap.com/docs/5.2/assets/img/guides/webpack-dev-server-bootstrap.png" />

Now you can start adding any Bootstrap components you want to use. Be sure to [check out the complete Webpack example project](https://github.com/twbs/examples/tree/main/webpack) for how to include additional custom Sass and optimize your build by importing only the parts of Bootstrap’s CSS and JS that you need.