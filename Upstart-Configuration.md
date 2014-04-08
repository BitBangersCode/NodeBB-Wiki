The following article demonstrates how to configure NodeBB on your server to start automatically whenever a server restarts.

This article uses the [Upstart init daemon](http://en.wikipedia.org/wiki/Upstart).

----

## Steps

*Note: The following instructions are intended to be run as the __root user__. Optionally, you can preface all of the commands with `sudo`*

1. Navigate to `/etc/init`: `cd /etc/init`
1. Create a new file called "nodebb". (Alternatively, you can call it "forum", or whatever you'd like)
1. Paste the following into the file:

``` upstart
start on startup
stop on runlevel [016]

respawn

setuid nobody
setgid nogroup

script
    cd /path/to/your/nodebb
    ./nodebb start
end script
```

Then, save the file, and you can NodeBB will now automatically start on boot. You can also invoke this script on-demand by calling:

``` bash
$ start nodebb

# or...

$ stop nodebb
```