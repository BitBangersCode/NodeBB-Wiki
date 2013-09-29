If you experience difficulties setting up a NodeBB instance, perhaps one of the following may help.

### I set up my NodeBB to point to a certain URL, but when I try accessing it, the page looks weird, and I see lots of curly braces?

Whenever this happens, it is usually indicative of the server being accessed by an address that is unexpected. For example, if NodeBB were set up so that its base URL is `http://192.168.1.100:4567`, and it were accessed via `http://10.10.232.185:4567`, even if both of these addresses pointed to the same physical machine, the proper template data would not load, as the ajax request fetching the data would violate the [same-origin policy](http://en.wikipedia.org/wiki/Same-origin_policy).

Simply put, NodeBB can only be accessed by one address at a time (for now). If you are attempting to access it from a different address, run NodeBB with the `--setup` flag and enter that new address into the `Publically accessible URL` field.

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

In early versions of NodeBB, many schema changes were made, usually necessitating a complete flush of the database. As of v0.0.5, an upgrade utility will always be provided and kept up to date so that existing NodeBB installs can maintain proper database schema.

For more information, please consult [[Upgrading NodeBB]]

### I've locked myself out of the administrative panel!

Versions of NodeBB prior to v0.0.7 allowed users to remove themselves as administrators, which is a bit of a problem if they happened to be the only administrator set. To re-add yourself as an administrator, first find your uid:

    $ redis-cli userslug:{slug}:uid    // where {slug} is your username
    "1"    // redis returned "1"
    $ redis-cli sadd administrators 1