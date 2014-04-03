### Required Software

First, install the following programs:

* https://windows.github.com/
* http://nodejs.org/
* http://sourceforge.net/projects/redis/files/redis-2.6.10/

You may have to restart your computer.

### Running NodeBB

Start Redis Server (C:\Program Files (x86)\Redis\StartRedisServer.cmd)

Open Git Shell, and type the following commands. Clone NodeBB repo:

    git clone https://github.com/designcreateplay/NodeBB.git

Enter directory: 

    cd NodeBB

Install dependencies:

    npm install

Run interactive installation:

    node app.js

You may leave all of the options as default.

And you're done! After the installation, run 

    node app.js

You can visit your forum at http://127.0.0.1:4567/


### Developing on Windows

It's a bit of a pain to shutdown and restart NodeBB everytime you make changes. First install supervisor:

    npm install -g supervisor

Open up bash:

    bash

And run NodeBB on "watch" mode:

    ./nodebb watch

It will launch NodeBB in development mode, and watch files that change and automatically restart your forum.
