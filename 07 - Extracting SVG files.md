# Extracting SVG files 
Bootstrap’s CSS includes multiple references to SVG files via inline data: URIs. If you define a Content Security Policy for your project that blocks data: URIs for images, then these SVG files will not load. You can get around this problem by extracting the inline SVG files using Webpack’s asset modules feature.

Configure Webpack to extract inline SVG files like this:


> ### Look into code 6.html
