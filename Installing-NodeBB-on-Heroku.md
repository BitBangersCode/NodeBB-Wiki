## Installation

**Note**: Installations to Heroku require a local machine with some flavour of unix, as NodeBB does not run on Windows.

1. Download and install [Heroku Toolbelt](https://toolbelt.heroku.com/) for your operating system
1. Log into your Heroku account: `heroku login`
1. Verify your Heroku account by adding a credit card (at http://heroku.com/verify)
1. Enable [Redis To Go](https://addons.heroku.com/redistogo) for your heroku account: `heroku addons:add redistogo:nano`
1. Clone the repository: `git clone https://github.com/designcreateplay/NodeBB.git /path/to/repo/clone`
1. `cd /path/to/repo/clone`
1. Install dependencies locally `npm install`
1. Run the NodeBB setup script: `node app --setup` (information for your Heroku server and Redis to Go instance can be found in your account page)
    * Your server name is found in your Heroku app's "settings" page, and looks something like `adjective-noun-wxyz.herokuapp.com`
    * Use any port number. It will be ignored.
    * Specify "n" when asked if a port will be used. Heroku transparently proxies all requests.
    * Your redis server can be found as part of the redis url. For example, for the url: `redis://redistogo:h28h3wgh37fns7@crestfish.redistogo.com:10026/`
    * The server is `crestfish.redistogo.com`
    * The port is `10036`
    * The password is `h28h3wgh37fns7`
1. Create a Procfile for Heroku: `echo "web: node app.js" > Procfile`
1. As Heroku does not support web sockets natively, disable the 'websocket' option by editing the file `src/websockets.js` and removing `'websocket'` from the third line of the file.
    * The line should read: `transports: ['websocket', 'xhr-polling', 'jsonp-polling', 'flashsocket']`
1. `git add -f Procfile config.json public/config.json && git commit -am "adding Procfile and configs for Heroku"`
1. Create the heroku app: `heroku create`
1. Push to heroku: `git push heroku master`
1. Initialise a single dyno: `heroku ps:scale web=1`
1. Visit your app!

If these instructions are unclear or if you run into trouble, please let us know by [filing an issue](https://github.com/designcreateplay/NodeBB/issues).

## Keeping it up to date

If you wish to pull the latest changes from the git repository to your Heroku app:

1. Navigate to your repository at `/path/to/nodebb`
2. `git pull`
3. `npm install`
4. `node app --upgrade`
5. `git commit -am "upgrading to latest nodebb"
6. `git push heroku master`