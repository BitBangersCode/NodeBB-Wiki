If you experience difficulties setting up a NodeBB instance, perhaps one of the following may help.

### Is it possible to install NodeBB via FTP?

It is possible to transfer the files to your remote server using FTP, but you do require shell access to the server in order to actually "start" NodeBB. Here is [a handy guide for installing NodeBB on DigitalOcean](http://burnaftercompiling.com/nodebb/setting-up-a-nodebb-forum-for-dummies/)

### `npm` says something is wrong...

For the most part, errors involving `npm` are due to Node.js being outdated. If you see an error similar to this one while running `npm install`:

    npm ERR! Unsupported
    npm ERR! Not compatible with your version of node/npm: connect@2.7.11

You'll need to update your Node.js version to 0.8 or higher.

To do this on Ubuntu:

    # add-apt-repository ppa:chris-lea/node.js
    # apt-get update && apt-get dist-upgrade -y
    # apt-cache policy nodejs    // should show a version higher than 0.8

### I upgraded NodeBB and now X isn't working properly!

Please consult [[Upgrading NodeBB]]