If you experience difficulties setting up a NodeBB instance, perhaps one of the following may help.

## `npm` Errors

For the most part, errors involving `npm` are due to Node.js being outdated. If you see an error similar to this one while running `npm install`:

    npm ERR! Unsupported
    npm ERR! Not compatible with your version of node/npm: connect@2.7.11

You'll need to update your Node.js version to 0.8 or higher.

To do this on Ubuntu:

    # add-apt-repository ppa:chris-lea/node.js
    # apt-get update && apt-get dist-upgrade -y
    # apt-cache policy nodejs    // should show a version higher than 0.8

## I upgraded NodeBB and now X isn't working properly!

In early versions of NodeBB, many schema changes were made, usually necessitating a complete flush of the database. As of v0.0.5, an upgrade utility will always be provided and kept up to date so that existing NodeBB installs can maintain proper database schema.

For more information, please consult [[Upgrading NodeBB]]

## I've locked myself out of the administrative panel!

Versions of NodeBB prior to v0.0.7 allowed users to remove themselves as administrators, which is a bit of a problem if they happened to be the only administrator set. To re-add yourself as an administrator, first find your uid:

    $ redis-cli userslug:{slug}:uid    // where {slug} is your username
    "1"    // redis returned "1"
    $ redis-cli sadd administrators 1