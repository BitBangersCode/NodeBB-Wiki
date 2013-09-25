NodeBB's periodic releases are located in the [Releases](https://github.com/designcreateplay/NodeBB/releases). These releases contain what is usually considered the most bug-free code, and is designed to be used on production-level instances of NodeBB.

To obtain more recent fixes and features, you can also `git clone` the latest version directly from the repository, although its stability cannot be guaranteed. Core developers will attempt to ensure that every commit results in a working client, even if individual features may not 100% complete.

## Upgrade Steps

After upgrading between revisions (i.e. v0.0.4 to v0.0.5), it may be necessary to run the following upgrade steps to ensure that any data schema changes are properly upgraded as well:

### 1. Shut down your forum

While it is possible to upgrade NodeBB while it is running, it is definitely not recommended, particularly if it is an active forum.

### 2. Back up your data

As with all upgrades, the first step is to **back up your data**! Nobody likes database corruption/misplacement.

All of the textual data stored in NodeBB is found in a `.rdb` file. On typical installs of Redis, the main database is found at `/var/lib/redis/dump.rdb`.

**Store this file somewhere safe.**

Uploaded images (avatars) are stored in /public/uploads. Feel free to back up this folder too:

    cd /path/to/nodebb/public
    tar -czf ~/nodebb_assets.tar.gz ./uploads

### 3. Grab the latest and greatest code

Navigate to your NodeBB: `$ cd /path/to/nodebb/instance`, and then run:

    $ git pull

This should retrieve the latest (and greatest) version of NodeBB from the repository. Alternatively, download and extract the latest versioned copy of the code from [the Releases Page](https://github.com/designcreateplay/NodeBB/releases). Overwrite any files as necessary.

### 4. Install any missing packages

Run `npm` to install any new packaged dependencies that may now be required by this new version of NodeBB:

    npm install

*Note*: You can also run `npm update`, but it is not necessary.

### 5. Database Migration

Occasionally, we may make changes to the database that require a migration. Run this:

    node app --upgrade

If nothing needs to be migrated, this script will do nothing.

### 6. Start up NodeBB & Test!

You should now be running the latest version of NodeBB.