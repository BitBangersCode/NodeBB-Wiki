## Static

### static:app.load
Executed when NodeBB is loaded, used to kickstart scripts in plugins (i.e. cron jobs, etc)
 
__Data Arguments__
* app - app
 * desc
* router - router
 * desc
* middleware - middleware
 * desc
* controllers - controllers
 * desc
 
Full desc 


## Filters

### filter:header.build
Allows plugins to add new navigation links to NodeBB.

__Data Arguments__
*

Full desc


### filter:admin.header_build
Allows plugins to create new navigation links in the ACP

__Data Arguments__
* 

Full desc


### filter:register.build
Allows plugins to add new elements to the registration form. At the moment, the only one supported is `data.captcha`;

__Data Arguments__
* req - express request object
 * desc
* res - express response object
 * desc
* templateData - object
 * The data passed to the template

Full desc


### filter:register.check
Allows plugins to run checks on information and deny registration if necessary.

__Data Arguments__
* `req` - express request object
 * desc
* `res` - express response object
 * desc
* `userData` - object
 * The user data parsed from the form.

Full desc


### filter:register.complete
Set the post-registration destination, or do post-register tasks here.

__Data Arguments__
* `uid` - Number
 * The new user id.
* `referrer` - String
 * The referral URL.

Full desc


### filter:post.getPosts

__Data Arguments__
* 

Full desc


### filter:post.getFields

__Data Arguments__
* 

Full desc


### filter:post.save
Executed whenever a post is created or edited, but before it is saved into the database.

__Data Arguments__
* 

Full desc


### filter:posts.custom_profile_info
Allows plugins to add custom profile information in the topic view's author post block.

__Data Arguments__
* 

Full desc


### filter:posts.modifyUserInfo
This is the user object found in any post array. It's a smaller subset of the full list of user data to save on bandwidth, so if you've added custom fields in via `user.setUserField`, add it here.

__Data Arguments__
* 

Full desc


### filter:parse.post
Executed when a post needs to be parsed from raw text to HTML (for output to client). This is useful if you'd like to use a parser to prettify posts, such as Markdown, or BBCode.

__Data Arguments__
* 

Full desc


### filter:parse.signature
.

__Data Arguments__
* 

Full desc


### filter:parse.raw
.

__Data Arguments__
* 

Full desc


### filter:scripts.get
Allows to add client-side JS to the header and queue up for minification on production.

__Data Arguments__
* 

Full desc


### filter:uploadImage

__Data Arguments__
* 

Full desc


### filter:uploadFile

__Data Arguments__
* 

Full desc


### filter:widgets.getAreas

__Data Arguments__
* 

Full desc


### filter:widgets.getWidgets

__Data Arguments__
* 

Full desc


### filter:widget.render

__Data Arguments__
* 

Full desc


### filter:search.query

__Data Arguments__
* 

Full desc


### filter:messaging.save

__Data Arguments__
* 

Full desc


### filter:messaging.parse

__Data Arguments__
* 

Full desc


### filter:sounds.get

__Data Arguments__
* 

Full desc


### filter:auth.init

__Data Arguments__
* 

Full desc


### filter:composer.help

__Data Arguments__
* 

Full desc


### filter:topic.thread_tools

__Data Arguments__
* 

Full desc


### filter:topic.get

__Data Arguments__
* 

Full desc


### filter:user.create

__Data Arguments__
* 

Full desc


### filter:user.delete

__Data Arguments__
* 

Full desc


### filter:user.profileLinks

__Data Arguments__
* 

Full desc


### filter:user.verify.code
Ability to modify the generated verification code (ec. for using a shorter verification code instead for SMS verification)

__Data Arguments__
* `confirm_code` - string
 * The confirmation code.

Full desc


### filter:user.custom_fields
Allows you to append custom fields to the newly created user, ex. mobileNumber.

__Data Arguments__
* `userData` - object
 * 

Full desc


### filter:templates.get_virtual
Allows you to modify the `api/get_templates_listing` API call, allowing ajaxification to custom templates that are not served physically via the `templates` parameter in `plugin.json`.

__Data Arguments__
* 

Full desc


### filter:templates.get_config
Allows you to add custom ajaxification rules in the `api/get_templates_listing` API call. See https://github.com/NodeBB/nodebb-theme-vanilla/blob/master/templates/config.json for more details

__Data Arguments__
* 

Full desc


### filter:sockets.sendNewPostToUids
An object consisting of a uidsTo array, a uidFrom integer, and a type ("newPost" or "newTopic". Useful for modifying who gets notifications of new posts (ex: ignore lists, etc).

__Data Arguments__
* 

Full desc


### filter:category.get
Fired when a category is retrieved.

__Data Arguments__
* `category` - Object
 * 
* `uid` - Number
 * 
* `cid` - Number
 * If applicable

Full desc


### filter:category.topics.get
Fired _before_ a category retrieves a listing of topics.

__Data Arguments__
* 

Full desc


### filter:privileges.topics.get
Fired when privileges are requested prior to topic access.

__Data Arguments__
* 

Full desc


## Actions

### action:page.load

__Data Arguments__
* `template`: 
 * The template loaded.
* `url`: String
 * Path to the page.

Full desc


### action:plugin.activate
Executed whenever a plugin is activated via the admin panel.

__Data Arguments__
* 

__Important__: Be sure to check the `id` that is sent in with this hook, otherwise your plugin will fire its registered hook method, even if your plugin was not the one that was activated.


### action:plugin.deactivate
Executed whenever a plugin is deactivated via the admin panel.

__Data Arguments__
* 

__Important__: Be sure to check the `id` that is sent in with this hook, otherwise your plugin will fire its registered hook method, even if your plugin was not the one that was deactivated.


### action:post.save
Executed whenever a post is created or edited, after it is saved into the database.

__Data Arguments__
* 

Full desc


### action:post.upvote
Executed whenever a post is upvoted.

__Data Arguments__
* `pid`: Number
 * The post id.
* `uid`: Number
 * The user that has triggered the upvote.

Full desc


### action:post.downvote
Executed whenever a post is downvoted.

__Data Arguments__
* `pid`: Number
 * The post id.
* `uid`: Number
 * The user that has triggered the downvote.

Full desc


### action:email.send

__Data Arguments__
* 

Full desc


### action:post.setField

__Data Arguments__
* 

Full desc


### action:topic.edit

__Data Arguments__
* 

Full desc


### action:topic.pin
Called when toggling pinned state.

__Data Arguments__
* `tid`: Number
 * The topic id.
* `isPinned`: Boolean
 * The pinned state of the topic.
* `uid`: Number
 * -

Full desc


### action:topic.lock
Called when toggling locked state.

__Data Arguments__
* `tid`: Number
 * The topic id.
* `isLocked`: Boolean
 * The locked state of the topic.
* `uid`: Number
 * -

Full desc


### action:topic.move
Called when moving a topic from on category to another.

__Data Arguments__
* `tid`: Number,
 * The topic id.
* `fromCid`: Number
 * The original category id.
* `toCid`: Number
 * The new category id.
* `uid`: Number
 * -

Full desc


### action:post.edit

__Data Arguments__
* 

Full desc


### action:post.delete
Called when deleting a post.

__Data Arguments__
* 

Full desc


### action:post.purge
Called when purging a post.

__Data Arguments__
* 

Full desc


### action:post.restore
Called when restoring a post.

__Data Arguments__
* 

Full desc


### action:notification.pushed
Executed whenever a notification is pushed to user(s).

__Data Arguments__
* 

Full desc


### action:config.set

__Data Arguments__
* 

Full desc


### action:topic.save
Called when saving a topic.

__Data Arguments__
* 

Full desc


### action:topic.delete
Called when deleting a topic.

__Data Arguments__
* 

Full desc


### action:topic.purge
Called when purging a topic.

__Data Arguments__
* 

Full desc


### action:user.create

__Data Arguments__
* 

Full desc


### action:user.verify

__Data Arguments__
* 

Full desc


### action:user.follow

__Data Arguments__
* 

Full desc


### action:user.unfollow

__Data Arguments__
* 

Full desc


### action:user.set

__Data Arguments__
* 

Full desc


### action:settings.set