# react

A template to create web applications on [Node.js](https://nodejs.org/) with [Gulp.js](https://www.npmjs.com/package/gulp) as the task-runner

## Technologies

### Server

[Express](https://www.npmjs.com/package/express) as the web server with [body parser](https://www.npmjs.com/package/body-parser) to serve static resources.

### Client

#### Web Application

 - [React](https://facebook.github.io/react/)
 - [ReactDOM](https://facebook.github.io/react/docs/react-dom.html)
 - [ReactRouterDOM](https://www.npmjs.com/package/react-router-dom)
 - [Bootstrap 3](https://getbootstrap.com/docs/3.3/)
 - [Font Awesome](http://fontawesome.io/)
 - [Ample Alerts](https://www.npmjs.com/package/ample-alerts/)
 - [jQuery](https://jquery.com/) as a dependency for Bootstrap
 - [ES2015](http://es6-features.org/)
 - [Less CSS](http://lesscss.org/)

#### Task Runner: Gulp

##### Plugins

 - [del](https://www.npmjs.com/package/del) to clean up the output directory at the start of every build
 - [gulp-concat](https://www.npmjs.com/package/gulp-concat) to concat files
 - [gulp-ejs](https://www.npmjs.com/package/gulp-ejs) to compile HTML templates before copying them to the output directory
 - [gulp-copy](https://www.npmjs.com/package/gulp-copy) to copy static resources to the output directory
 - [gulp-that](https://www.npmjs.com/package/gulp-that) to transform service-worker script to make sure it is updated on every build
 - [gulp-less](https://www.npmjs.com/package/gulp-less) to transpile LESS stylesheets into CSS
 - [effortless-css](https://www.npmjs.com/package/effortless-css) to provide Less CSS mixins
 - [gulp-cleancss](https://www.npmjs.com/package/gulp-cleancss) to minify CSS
 - [browserify](https://www.npmjs.com/package/browserify) to `require` JavaScript libraries from within the web browser
 - [vinyl-buffer](https://www.npmjs.com/package/vinyl-buffer) and [vinyl-source-stream](https://www.npmjs.com/package/vinyl-source-stream) to work with browserify
 - [babelify](https://www.npmjs.com/package/babelify), [babel-preset-env](https://www.npmjs.com/package/babel-preset-env) and [babel-preset-react](https://www.npmjs.com/package/babel-preset-react) for ES2015 and JSX transpilation
 - [gulp-uglify](https://www.npmjs.com/package/gulp-uglify) to minify JavaScript files
 - [gulp-eslint](https://www.npmjs.com/package/gulp-eslint), [babel-eslint](https://www.npmjs.com/package/babel-eslint), [eslint-config-myterminal](https://www.npmjs.com/package/eslint-config-myterminal), [eslint-config-airbnb](https://www.npmjs.com/package/eslint-config-airbnb), [eslint-plugin-import](https://www.npmjs.com/package/eslint-plugin-import), [eslint-plugin-jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y) and [eslint-plugin-react](https://www.npmjs.com/package/eslint-plugin-react) to run ESLint on JavaScript files

##### Tasks

 - **build** (default)
   - **clean** to clean the output directory
   - **copy**
     - **copyBootstrapCss** to copy Bootstrap CSS Stylesheets to the output directory
     - **copyBootstrapFonts** to copy Bootstrap fonts to the output directory
     - **copyFontAwesomeCss** to copy FontAwesome CSS Stylesheets to the output directory
     - **copyFontAwesomeFonts** to copy FontAwesome fonts to the output directory
     - **copyOthers** to copy data, fonts, images and favicon to the output directory
   - **manifest** to generate manifest file for release mode
   - **styles** to transpile Less CSS stylesheets into CSS stylesheets for the output directory
   - **scripts** to concatenate, transpile & minify all JavaScript to the output directory
   - **html** to copy HTML page to the output directory
   - **copyServiceWorker** to copy the service-worker script to the output directory after a few transforms
 - **debug**
   - **clean** to clean the output directory
   - **copy**
     - **copyBootstrapCss** to copy Bootstrap CSS Stylesheets to the output directory
     - **copyBootstrapFonts** to copy Bootstrap fonts to the output directory
     - **copyFontAwesomeCss** to copy FontAwesome CSS Stylesheets to the output directory
     - **copyFontAwesomeFonts** to copy FontAwesome fonts to the output directory
     - **copyOthers** to copy data, fonts, images and favicon to the output directory
   - **manifestDebug** to generate manifest file for debug mode
   - **styles** to transpile Less CSS stylesheets into CSS stylesheets for the output directory
   - **scriptsDebug** to concatenate and transpile all JavaScript to the output directory
   - **htmlDebug** to copy HTML page to the output directory
   - **lint** to run ESLint over JavaScript files
 - **lint**
   - run ESLint over JavaScript files
 - **develop** to watch over the source files and run tasks related to the changed files

## To-Do

 - Write unit-tests
 - Implement CSS modules
