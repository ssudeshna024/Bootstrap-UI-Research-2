# Setup 
We’re building a Webpack project with Bootstrap from scratch, so there are some prerequisites and up front steps before we can really get started. This guide requires you to have Node.js installed and some familiarity with the terminal.

- Create a project folder and setup npm. We’ll create the my-project folder and initialize npm with the -y argument to avoid it asking us all the interactive questions.


> mkdir my-project && cd my-project
> npm init -y

- Install Webpack. Next we need to install our Webpack development dependencies: webpack for the core of Webpack, webpack-cli so we can run Webpack commands from the terminal, and webpack-dev-server so we can run a local development server. We use --save-dev to signal that these dependencies are only for development use and not for production.


> npm i --save-dev webpack webpack-cli webpack-dev-server

- Install Bootstrap. Now we can install Bootstrap. We’ll also install Popper since our dropdowns, popovers, and tooltips depend on it for their positioning. If you don’t plan on using those components, you can omit Popper here.


> npm i --save bootstrap @popperjs/core

- Install additional dependencies. In addition to Webpack and Bootstrap, we need a few more dependencies to properly import and bundle Bootstrap’s CSS and JS with Webpack. These include Sass, some loaders, and Autoprefixer.


> npm i --save-dev autoprefixer css-loader postcss-loader sass sass-loader style-loader

- Now that we have all the necessary dependencies installed, we can get to work creating the project files and importing Bootstrap.