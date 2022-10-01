# Project structure 
We’ve already created the my-project folder and initialized npm. Now we’ll also create our src and dist folders to round out the project structure. Run the following from my-project, or manually create the folder and file structure shown below.


> mkdir {dist,src,src/js,src/scss}

touch dist/index.html src/js/main.js src/scss/styles.scss webpack.config.js
When you’re done, your complete project should look like this:


>my-project/
├── dist/
│   └── index.html
├── src/
│   ├── js/
│   │   └── main.js
│   └── scss/
│       └── styles.scss
├── package-lock.json
├── package.json
└── webpack.config.js
At this point, everything is in the right place, but Webpack won’t work because we haven’t filled in our webpack.config.js yet.