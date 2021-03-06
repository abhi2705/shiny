This directory contains build tools for Shiny.


## Grunt

Grunt is a build tool that runs on node.js. In Shiny, it is used for minifying and linting Javascript code.

### Installing Grunt

Grunt requires Node.js and npm (the Node.js package manager). Installation of these programs differs across platforms and is generally pretty easy, so I won't include instructions here.

Once node and npm are installed, install grunt:

```
# Install grunt command line tool globally
sudo npm install -g grunt-cli

# Install grunt plus modules for this project
npm install
```

### Using Grunt

To run all default grunt tasks (minification and jshint), simply go into the `tools` directory and run:

```
grunt
```

It's also useful to run `grunt` so that it monitors files for changes and run tasks as necessary. This is done with:

```
grunt watch
```

One of the tasks minifies `shiny.js` to generate `shiny.min.js`. The minified file is supplied to the browser, along with a source map file, `shiny.min.js.map`, which allows a user to view the original Javascript source when using the debugging console in the browser.

During development of Shiny's Javascript code, it's best to use `grunt watch` so that the minified file will get updated whenever you make changes to `shiny.js`.
