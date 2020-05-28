# CSS &mdash; SASS

Learning SASS (SCSS), a CSS pre-processor that makes writing CSS &mdash; 10 times faster, better and more organized.

*Note: This a course audited from **[here](https://www.udemy.com/course/advanced-css-and-sass/)**.*

## SASS (SCSS) Installation & Execution

Download and install node/npm from __[here](https://nodejs.org/)__. In the project where SASS is to be installed, type in `npm init` to initialize the project with a __package.json__ file. Now to install SASS, in the terminal (should be in pwd/our-project-directory), we type in the following commands:

- `npm install node-sass --save-dev` 
- `npm install live-server --save-dev`
- `npm install postcss-cli --save-dev`
- `npm install autoprefixer --save-dev`
- `npm install concat --save-dev`

and after the packages are installed, we shall see that our **package.json** file should have the following content:

<pre>
{
  "name": "project-name",
  "version": "1.0.0",
  "description": "project-description",
  "main": "index.js",
  "scripts": {},
  "author": "Ch Sriram",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^9.7.6",
    "concat": "^1.0.3",
    "node-sass": "^4.13.1",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^7.1.1"
  }
}
</pre>

If we look into `"devDependencies"`, we can see all the packages we installed along with their latest versions.

After that, we write our own scripts under `"scripts"` object in our **package.json** as follows:

<pre>
{
  "name": "nature-tours",
  "version": "1.0.0",
  "description": "landing page for nature tours",
  "main": "index.js",
  "scripts": {
    "watch:sass": "node-sass ./sass/main.scss ./css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel watch:sass devserver",

    "compile:sass": "node-sass ./sass/main.scss ./css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b \"last 10 versions\" css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.min.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
  "author": "Ch Sriram",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^9.7.6",
    "concat": "^1.0.3",
    "node-sass": "^4.13.1",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^7.1.1"
  }
}
</pre>

We can see how the `"scripts"` are defined in **package.json** file. 

There are 2 scripts of importance:

- When developing/working-on the project, run the script named **start** by typing in `npm run start`.
- When we need to deploy the project, we run the script named **build:css** by typing in `npm run build:css`.

**Note**: In case, if you do not want to go through this lengthy installation process, you can always download the respective child repository as a zip file and run `npm install` **to install all the `"devDependencies"` and the `"scripts"` automatically**.

## Child Repositories

*Note: One more child repository(s) to follow.*

1. Nature Tours - **[Link to repo](https://github.com/Ch-sriram/nature-tours)**
2. Trillo (flexbox) - **[Link to repo](https://github.com/Ch-sriram/trillo-flexbox)**

## Learning Resources

1. SASS (SCSS)
   1. **[SASS Demo - I \[Variables & Nesting\]](https://codepen.io/ch-sriram/pen/KKdMmZj)**
   2. **[SASS Demo - II \[@mixin, @extends & @function\]](https://codepen.io/ch-sriram/pen/MWaexGp)**
2. Flexbox
   1. **[Flexbox Demo - I \[Flex Container Properties\]](https://codepen.io/ch-sriram/pen/mdeGLxq)**
   2. **[Flexbox Demo - II \[Flex Item Properties\]](https://codepen.io/ch-sriram/pen/jObvKqN)**
   3. **[Flexbox Demo - III \[Adding More Flex Items\]](https://codepen.io/ch-sriram/pen/qBOJOWy)**
3. Grid
   1. **[Grid Demo - I \[Making The First Grid\]](https://codepen.io/ch-sriram/pen/KKdbqGg)**
   2. **[Grid Demo - II \[Using fr Unit\]](https://codepen.io/ch-sriram/pen/RwWEZGw)**
   3. **[Grid Demo - III \[Positioning Grid Items\]](https://codepen.io/ch-sriram/pen/qBOLPjN)**
   4. **[Grid Demo - IV \[Spanning Grid Items\]](https://codepen.io/ch-sriram/pen/JjYwZqW)**
   5. **[Grid Challenge - I](https://github.com/Ch-sriram/css-sass/blob/dev/3-nexter-grid/Resources/challenge--1.png)** | **[Solution](https://codepen.io/ch-sriram/pen/XWmOOzw)**
   6. **[Grid Demo - V \[Naming Grid Lines\]](https://codepen.io/ch-sriram/pen/gOaEjRz)**
   7. **[Grid Demo - VI \[Naming Grid Areas\]](https://codepen.io/ch-sriram/pen/PoPLdpr)**
   8. **[Grid Demo - VII \[Implicit vs. Explicit Grid\]](https://codepen.io/ch-sriram/pen/QWjoZmQ)**
   9. **[Grid Demo - VIII \[Aligning Grid Items in different Grid Areas\]](https://codepen.io/ch-sriram/pen/pojYqOe)**
   10. **[Grid Demo - IX \[Aligning Grid Tracks\]](https://codepen.io/ch-sriram/pen/OJyqdVX)**
   11. **[Grid Demo - X \[min-content, max-content & minmax() function\]](https://codepen.io/ch-sriram/pen/vYNwYWm)**
   12. **[Grid Demo - XI \[Responsive grid layouts with auto-fit & auto-fill\]](https://codepen.io/ch-sriram/pen/xxwNLKE)**