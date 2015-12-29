## Browsersync recipes.

There are endless amounts of possible integrations and workflow scenarios when using Browsersync, so this project is an 
attempt to highlight as many of them as we can, whilst providing full, working examples.

#### Grunt recipes
- [SASS](https://github.com/Browsersync/recipes/tree/master/recipes/grunt.sass)
- [SASS, Autoprefixer](https://github.com/Browsersync/recipes/tree/master/recipes/grunt.sass.autoprefixer)
- [SASS, HTML/CSS injection](https://github.com/Browsersync/recipes/tree/master/recipes/grunt.html.injection)

#### Gulp recipes
- [SASS](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.sass)
- [SASS, Jade Templates](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.jade)
- [Ruby SASS](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.ruby.sass)
- [SASS, Slow running tasks](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.task.sequence)
- [Swig Templates](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.swig)

#### Other recipes
- [Browserify, Babelify, Watchify, Sourcemaps](https://github.com/Browsersync/recipes/tree/master/recipes/gulp.browserify)
- [HTML/CSS injection](https://github.com/Browsersync/recipes/tree/master/recipes/html.injection)
- [Middleware, CSS](https://github.com/Browsersync/recipes/tree/master/recipes/middleware.css.injection)

#### Server recipes
- [Example](https://github.com/Browsersync/recipes/tree/master/recipes/server)
- [With pre-gzipped assets](https://github.com/Browsersync/recipes/tree/master/recipes/server.gzipped.assets)
- [Using includes](https://github.com/Browsersync/recipes/tree/master/recipes/server.includes)
- [Middleware: logging, history](https://github.com/Browsersync/recipes/tree/master/recipes/server.middleware)

#### Webpack recipes
- [Babel](https://github.com/Browsersync/recipes/tree/master/recipes/webpack.babel)
- [Monkey Hot Loader](https://github.com/Browsersync/recipes/tree/master/recipes/webpack.monkey-hot-loader)
- [React Hot Loader](https://github.com/Browsersync/recipes/tree/master/recipes/webpack.react-hot-loader)
- [React Transform HMR](https://github.com/Browsersync/recipes/tree/master/recipes/webpack.react-transform-hmr)


### Contributions / Feedback

Spotted an error? Couldn't get one of the examples running? Have your own sweet setup that you want to show off to the world?
We'd love to receive your feedback and contributions - so please get in touch! We aim to make this project the canonical source 
of example projects & code snippets related to running Browsersync.


### How to contribute an example

First thing you should do, is take a look at our [simplest example here](https://github.com/Browsersync/recipes/tree/master/recipes/server) - 
this will give you a great head-start on setting up your code.

Then, `fork` this repo and `clone` your fork down to your local machine. Now create a new folder inside `recipes`
(note the naming structure). This is where you create your awesome example. You're free to do as you like,
but there are a couple of rules you'll need to follow to ensure the project can build.

**Required Files**

- `package.json` (see below for requirements)
- `app.js` (or any JS file showing the example)
- `./app` directory. Always include the minimum HTML, JS & CSS needed to prove your example.

**Do NOT include**
- `readme.md` (this is created dynamically for you)
- any other files that are not related to your example.


### package.json requirements

**start command**: For consistency, ensure your example can be run with the command `npm start`. To 
do this, you just need to provide something along these lines:

```json
"scripts": {
    "start": "node app.js"
},
```

**main file**: We inline your main Javascript file into the `readme.md`, so
don't miss this field.

```json
"main": "app.js" // or gulpfile.js etc
```

**description**: We use this as the Title. So make it short and descriptive, such as 

```json
"description": "Server example"
```


### Finally, build.
After you've added your example in the recipes folder, return to the root and run

```bash
npm install && npm run build
```

This will install [Crossbow.js](https://github.com/shakyShane/crossbow.js) and compile the project.
Commit everything that has changed and push it up to your fork. Send a Pull Request when you're
ready, or if you'd like us to have a look over your code before that, just ping us [twitter](https://twitter.com/browsersync) and we'll 
take a look! 
