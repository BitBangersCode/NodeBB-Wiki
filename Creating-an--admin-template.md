# Creating an admin template:

Just a quick run down of what I needed to modify in order to add a feature to the admin panel. Here I will explain what I needed to get my "logger" template working. After writing this module, I can then access the admin panel (http://nodebb:4567/admin/logger) and modify/save configuration settings.



### Create a user-facing .tpl:

These files are found in: ./NodeBB/public/templates/admin/

For example, I will create a logger.tpl: ./NodeBB/public/templates/admin/logger.tpl

    <h1>Logger</h1>
    <hr />

    <h3>Logger Settings</h3>
    <div class="alert alert-warning">

    <p>
        By enabling the check box, you will receive http logs to standard output. If you specify a path, logs will then be saved to a file instead.
    </p>
    <br/>

    <form>

        <label>
            <input type="checkbox" data-field="loggerStatus"> <strong>Enable logging</strong>
        </label>
        <br/>

        <label>Path to log file</label>
        <input class="form-control" type="text" placeholder="/path/to/log/file.log" data-field="loggerPath" />    <br />
    </form>
    </div>

    <button class="btn btn-lg btn-primary" id="save">Save</button>

    <script>
    var loadDelay = setInterval(function() {
        if (nodebb_admin) {
            nodebb_admin.prepare();
            clearInterval(loadDelay);
        }
    }, 500);
    </script>


Notice the data-field elements? When you click "save", those fields are now accessible via "meta.config" in the NodeBB backend.



### Add the template route to config.json:

Edit ./NodeBB/public/templates/config.json & add your route. For example:

    "admin/logger.*": "admin/logger",


### Add your routes to NodeBB's backend:

Edit ./NodeBB/src/routes/admin.js and add your routes/handlers:


    Admin.create_routes = function (app) {

        (function () {
            var routes = [
                'categories/active', 'categories/disabled', 'users', 'topics', 'settings', 'themes',
                'twitter', 'facebook', 'gplus', 'redis', 'motd', 'groups','logger',
                'users/latest', 'users/sort-posts', 'users/sort-reputation',
                'users/search', 'plugins'
            ];

           app.get('/logger', function(req, res) {
                res.json(200, {});
            });



### Finally, edit the file that matters:

In my case, this will be ./NodeBB/src/webserver.js

Here, I will test a few configuration settings and decide whether or not I want to use the logger.

To access any of your saved settings, simply access "meta.config.*" from within the NodeBB backend. For example, here is what my meta.config object looks like while writing this wiki page:

    { postDelay: '10000',
      minimumPostLength: '8',
      minimumTitleLength: '3',
      minimumUsernameLength: '2',
      maximumUsernameLength: '16',
      minimumPasswordLength: '6',
      imgurClientID: '',
      maximumProfileImageSize: '256',
      loggerStatus: '1',
      loggerPath: '/tmp/nodebb.log',
      status: 'ok' }

And finally, here is some code using meta.config etc:

                if(nconf.get("express:logger") == true || meta.config.loggerStatus) {
                    var loggerObj = {};
                    if(meta.config.loggerPath) {
                        loggerObj.stream = fs.createWriteStream(meta.config.loggerPath, {flags: 'a'});
                        meta.config.loggerStream = loggerObj.stream
                    }
                    app.use(express.logger(loggerObj));
                }



Hope that is of some help.

-- adarqui