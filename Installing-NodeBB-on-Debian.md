The current Ubuntu guide is not completely compatible with Debian and there are some specificities and especially the NodeJS installation, and how to get latest Redis.

## Requirements
NodeBB requires these software to be installed :
* Node.js at least 0.8 and greater
* Redis, version 2.6 or greater
* cURL installed, just do `sudo apt-get install curl` in order to install it

## Node.js installation

Fedora is at the head for keeping packages updated and has Node.js already in the package manager.

To install:
```
yum install nodejs
```

## Installing NodeBB

Now, we have NodeJS installed and Redis ready to be installed, run this command for install the base software stack :
``` bash
$ apt-get install redis-server imagemagick git
```

Next clone this repository :
``` bash
$ cd /path/to/nodebb/install/location
$ git clone git://github.com/designcreateplay/NodeBB.git nodebb
```
Now we are going to install all dependencies for NodeBB via NPM :

    $ cd /path/to/nodebb/install/location/nodebb (or if you are on your install location directory run : cd nodebb)
    $ npm install

Install NodeBB by running the app with `--setup` flag :
``` bash
$ ./nodebb setup
```

1. `URL of this installation` is either your public ip address or your domain name pointing to that ip address.  
    *Example:* `http://0.0.0.0` or `http://example.org`  

2. `Port number of your NodeBB` is the port needed to access your site:  
    **Note:** If you do not proxy your port with something like nginx then port 80 is recommended for production.  
3. If you used the above steps to setup your redis-server then use the default redis settings.

And after all.. let's run the NodeBB forum
``` bash
$ ./nodebb start
```

**Note:** If you NodeBB or your server crash, your NodeBB instance will not reboot (snap), this is why you should take a look at the other way to start your NodeBB instance with helper programs such as `supervisor` and `forever`, just [take a look here](https://github.com/designcreateplay/NodeBB/wiki/How-to-run-NodeBB) it's simple as a click !

## Extras, tips and Advice

You should secure your NodeBB installation, [take a look here](https://github.com/designcreateplay/NodeBB#securing-nodebb).

You should use Nginx in order to reverse proxy your NodeBB installation on the port 80, [take a look here](https://github.com/designcreateplay/NodeBB/wiki/Configuring-nginx-as-a-proxy-to-NodeBB)