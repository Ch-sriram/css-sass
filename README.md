# CSS &mdash; SASS

Learning SASS (SCSS), a CSS pre-processor that makes writing CSS &mdash; 10 times faster, better and organized.

## SASS Install Notes

Download and install node/npm from __[here](https://nodejs.org/)__. In the project where SASS is to be installed, type in <code>npm init</code> to initialize the project with a __package.json__ file. Now to install SASS, in the terminal (should be in pwd/our-project-directory), we type in <code>npm install node-sass --save-dev</code> and after the package is installed, we shall see that our **package.json** file should have the following content:

<pre>
{
  "name": "nature-tours",
  "version": "1.0.0",
  "description": "landing page for nature tours",
  "main": "index.js",
  "scripts": {
    "compile-sass": "node-sass ./sass/main.scss ./css/style.css -w"
  },
  "author": "Ch Sriram",
  "license": "ISC",
  "devDependencies": {
    "node-sass": "^4.13.1"
  }
}
</pre>

We can see that **node-sass** is installed as a devDependency. We can also **compile-sass** script defined which is used to compile the SASS code into CSS. The syntax for the compilation code is &mdash; **<code>node-sass &lt;input-file> &lt;output-file> -w</code>**. The **-w** flag is used to compile the SCSS to CSS immediately, as soon as we type in the SASS code, because of which, we won't need to compile the SCSS code into CSS by running the script all the time.

The input-file (the SCSS file from which we are going to compile the SASS code into CSS code) in the given package.json file is *./sass/main.scss* and the output-file (target of the compilation, i.e., this is where the CSS file is generated. We link this file to index.html [main HTML markup file]).

To run the script that we just made, in the terminal, we type in **<code>npm run compile-sass</code>**, and we should see that the SASS is compiled into CSS and a CSS file is generated at the mentioned target.