Like most Node.js applications, NodeBB runs off of a single file that starts the HTTP listener -- `app.js`.

### Simple Node.js Process

To start NodeBB, run it with `node` (some distributions use the executable `nodejs`, please adjust accordingly):

    $ cd /path/to/nodebb/install
    $ node app

However, bear in mind that crashes will cause the NodeBB process to halt, bringing down your forum. Consider some of the more reliable options, below:

### Supervisor Process

Using the [`supervisor` package](https://github.com/isaacs/node-supervisor), you can have NodeBB restart itself if it crashes:

    $ npm install -g supervisor
    $ supervisor app

As `supervisor` by default continues to pipe output to `stdout`, it is best suited to development builds.

### Forever Daemon

The best way to keep NodeBB up is to use the [`forever` package](https://github.com/nodejitsu/forever) via the command line interface, which can monitor NodeBB and re-launch it if necessary:

    $ npm install -f forever
    $ forever start app.js

`forever` is best used in conjunction with a production build.