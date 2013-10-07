## Requirements

NodeBB requires the following software to be installed:

* A version of Node.js at least 0.8 or greater.
* Redis, version 2.6 or greater (steps to install from Joyent's package repository given below).
* nginx, version 1.3.13 or greater (**only if** intending to use nginx to proxy requests to a NodeBB server).

## Server Access

1. Sign in your Joyent account: [Joyent.com](http://joyent.com)

1. Select: `Create Instance`

1. Create the newest `smartos nodejs` image.  
**Note:** The following steps have been tested with image: `smartos nodejs 13.1.0`  

1. Wait for your instance to show `Running` then click on its name.

1. Find your `Login` and admin password. If the `Credentials` section is missing, refresh the webpage.  
*Example:* `ssh root@0.0.0.0` `A#Ca{c1@3`  

1. SSH into your server as the admin not root: `ssh admin@0.0.0.0`  
**Note:** For Windows users that do not have ssh installed, here is an option: [Cygwin.com](http://cygwin.com)  

## Installation

1. Install NodeBB's software dependencies:

        $ sudo pkgin update
        $ sudo pkgin install scmgit nodejs build-essential ImageMagick redis

    If any of these failed:

        $ pkgin search *failed-name*
        $ sudo pkgin install *available-name*

2. **If needed** setup a redis-server with default settings as a service (automatically starts and restarts):  
    **Note:** These steps quickly setup a redis server but does not fine-tuned it for production.  
    **Note:** If you ran `redis-server` manually then exit out of it now.  

        $ svcadm enable redis
        $ svcs

    *-* If `svcs` shows "/pkgsrc/redis:default" in maintenance mode then:

        $ scvadm clear redis  

    *-* To shut down your redis-server and keep it from restarting:

        $ scvadm disable redis

    *-* To start up your redis-server and have it always running:

        $ scvadm enable redis

1. Move to where you want to create the nodebb folder:

        $ cd /parent/directory/of/nodebb/

1. Clone NodeBB's repository:

        $ git clone git://github.com/designcreateplay/NodeBB.git nodebb

1. Install NodeBB's npm dependencies:

        $ cd nodebb/
        $ npm install

1. Run NodeBB's setup script:  

        $ node app --setup

    1. `URL of this installation` is either your public ip address from your ssh `Login` or your domain name pointing to that ip address.  
    *Example:* `http://0.0.0.0` or `http://example.org`  
    1. `Port number of your NodeBB` is the port needed to access your site:  
    **Note:** If you do not proxy your port with something like nginx then port 80 is recommended for production.  
    1. If you used the above steps to setup your redis-server then use the default redis settings.  

1. Start NodeBB process:  

    *Run NodeBB manually:*  
    **Note:** This should not be used for production.  

        $ node app

1. Visit your app!
    *Example:* With a port of 4567: `http://0.0.0.0:4567` or `http://example.org:4567`  
    **Note:** With port 80 the `:80` does not need to be entered.  

**Note:** If these instructions are unclear or if you run into trouble, please let us know by [filing an issue](https://github.com/designcreateplay/NodeBB/issues).

## Upgrading NodeBB

**Note:** Detailed upgrade instructions are listed in [Upgrading NodeBB](https://github.com/designcreateplay/NodeBB/wiki/Upgrading-NodeBB).