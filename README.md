# CSS &mdash; SASS

Learning SASS (SCSS), a CSS pre-processor that makes writing CSS &mdash; 10 times faster, better and more organized.

*Note*: This a course audited from **[here](https://www.udemy.com/course/advanced-css-and-sass/)**.

## General SASS Install Notes

Download and install node/npm from __[here](https://nodejs.org/)__. In the project where SASS is to be installed, type in <code>npm init</code> to initialize the project with a __package.json__ file. Now to install SASS, in the terminal (should be in pwd/our-project-directory), we type in <code>npm install node-sass --save-dev</code> and after the package is installed, we shall see that our **package.json** file should have the following content:

<pre>
{
  "name": "nature-tours",
  "version": "1.0.0",
  "description": "landing page for nature tours",
  "main": "index.js",
  "scripts": {
    "watch:sass": "node-sass ./sass/main.scss ./css/style.css -w",
    "compile:sass": "node-sass ./sass/main.scss ./css/style.comp.css"
  },
  "author": "Ch Sriram",
  "license": "ISC",
  "devDependencies": {
    "node-sass": "^4.13.1",
  }
}
</pre>

We can see that **node-sass** is installed as a **devDependency**.

For compilation, we run <code>npm run compile:sass</code> and during development, to see the changes live, we use <code>npm run watch:sass</code>


## Child Repositories

*Note*: *Two more child repositories to follow*.

1. Nature Tours - **[Link to repo](https://github.com/Ch-sriram/nature-tours)**