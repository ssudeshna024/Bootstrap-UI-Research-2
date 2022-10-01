# Configure Webpack 
With dependencies installed and our project folder ready for us to start coding, we can now configure Webpack and run our project locally.

Open webpack.config.js in your editor. Since it’s blank, we’ll need to add some boilerplate config to it so we can start our server. This part of the config tells Webpack were to look for our project’s JavaScript, where to output the compiled code to (dist), and how the development server should behave (pulling from the dist folder with hot reload).


> const path = require('path')

> module.exports = {
  entry: './src/js/main.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist')
  },
  devServer: {
    static: path.resolve(__dirname, 'dist'),
    port: 8080,
    hot: true
  }
}

Next we fill in our dist/index.html. This is the HTML page Webpack will load in the browser to utilize the bundled CSS and JS we’ll add to it in later steps. Before we can do that, we have to give it something to render and include the output JS from the previous step.


> ### Look into code 1.html

We’re including a little bit of Bootstrap styling here with the div class="container" and < button > so that we see when Bootstrap’s CSS is loaded by Webpack.

Now we need an npm script to run Webpack. Open package.json and add the start script shown below (you should already have the test script). We’ll use this script to start our local Webpack dev server.

> ### Look into code 2.html

And finally, we can start Webpack. From the my-project folder in your terminal, run that newly added npm script:


> npm start

<img src="https://getbootstrap.com/docs/5.2/assets/img/guides/webpack-dev-server.png" />

Webpack dev server running
In the next and final section to this guide, we’ll set up the Webpack loaders and import all of Bootstrap’s CSS and JavaScript.