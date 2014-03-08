First, we install our base software stack:

``` bash
$ apt-get install git nodejs redis-server build-essential imagemagick
```

If you want to use MongoDB instead of Redis install it from http://www.mongodb.org/downloads and remove 'redis-server' from the above command. [MongoDB-Setup](https://github.com/designcreateplay/NodeBB/wiki/Installing-NodeBB-With-MongoDB)

**If your package manager only installed a version of Node.js that is less than 0.8 (e.g. Ubuntu 12.10, 13.04):**

``` bash
$ add-apt-repository ppa:chris-lea/node.js
$ apt-get update && apt-get dist-upgrade
```

Next, clone this repository:

``` bash
$ cd /path/to/nodebb/install/location
$ git clone git://github.com/designcreateplay/NodeBB.git nodebb
```

Obtain all of the dependencies required by NodeBB:

```
$ cd nodebb
$ npm install
```

Initiate the setup script by running the app with the `--setup` flag:

``` bash
$ ./nodebb setup
```

The default settings are for a local server running on the default port, with a redis store on the same machine/port. You can optionally run

``` bash
$ ./nodebb setup --base_url http://localhost --port 4567 --use_port --secret MyAppSecret --bind_address 0.0.0.0 --database redis --redis:host 127.0.0.1 --redis:port 6379 --redis:password p4s$w0rd --redis:database 0
```

Lastly, we run the forum.

``` bash
$ ./nodebb start
```

NodeBB can also be started with helper programs, such as `supervisor` and `forever`. [Take a look at the options here](https://github.com/designcreateplay/NodeBB/wiki/How-to-run-NodeBB).