The following is a list of all hooks present in NodeBB. This list is intended to guide developers who are looking to write plugins for NodeBB. For more information, please consult [[Writing Plugins for NodeBB]].

There are two types of hooks, **filters**, and **actions**. Filters take an input (provided as a single argument), parse it in some way, and return the changed value. Actions take multiple inputs, and execute actions based on the inputs received. Actions do not return anything.

**Important**: This list is by no means exhaustive. Hooks are added on an as-needed basis (or if we can see a potential use case ahead of time), and all requests to add new hooks to NodeBB should be sent to us via the [issue tracker](https://github.com/designcreateplay/NodeBB/issues).

----

## Filters

### `filter:admin.create_routes`
**Allows plugins to define new routes in the ACP**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/32990794ce7f1304655151eb1f11b169e525f901)<br />
See Example: [Sample Admin Page](https://github.com/psychobunny/nodebb-plugin-admin-sample)

### `filter:admin.header_build`
Allows plugins to create new navigation links in the ACP
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/2b07917020c9181ff15e6096012144f4a9c201d4)
See Example: [Sample Admin Page](https://github.com/psychobunny/nodebb-plugin-admin-sample)

### `filter:post.save`

**Compatibility: v0.0.5+**<br />
**Argument(s)**: A post's content (markdown text)

Executed whenever a post is created or edited, but before it is saved into the database.

### `filter:post.get`

**Compatibility: v0.0.6+**<br />
**Argument(s)**: A post object (javascript Object)

Executed whenever a post is retrieved, but before being sent to the client.

### `filter:category.build_sidebars`
**Allows plugins to define custom sidebar blocks in the category view**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/ca9c468edd94fcf36b93fbe145a25014a03513f2)<br />
See Example: [Sidebar Ad Block](https://github.com/psychobunny/nodebb-plugin-ad-block)

### `filter:footer.build`

**Compatibility: v0.1.1+**<br />
**Argument(s)**: An empty string

HTML returned by each plugin will be inserted into the `<footer>` element on the page.

### `filter:header.build`
**Allows plugins to add new navigation links to NodeBB**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/a63732027f9ba0bd54254c3b5c83f2a63f1ad531)<br />
See Example: [Sample Static Page](https://github.com/psychobunny/nodebb-plugin-static-page/)

### `filter:post.parse`

**Compatibility: v0.0.7+**<br />
**Argument(s)**: A post or signature's raw text (String)

Executed when a post or signature needs to be parsed from raw text to HTML (for output to client). This is useful if you'd like to use a parser to prettify posts, such as [Markdown](http://daringfireball.net/projects/markdown/), or [BBCode](http://www.bbcode.org/).

### `filter:posts.custom_profile_info`
**Allows plugins to add custom profile information in the topic view's author post block**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/bf677522a93ec4c48f6b0fa27ab1388f9eedba4c)<br />
See Example: [Cash MOD](https://github.com/psychobunny/nodebb-plugin-cash)

### `filter:register.check`
**Allows plugins to run checks on information and deny registration if necessary.**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/cd4a204f999d5ef5bac4557f03d4c15abebfdce3)<br />

### `filter:server.create_routes`
**Allows plugins to define new routes in NodeBB**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/2a4b228e19c939be1872ce6d9669ae03b98c853a)<br />
See Example: [Sample Static Page](https://github.com/psychobunny/nodebb-plugin-static-page/)

### `filter:scripts.get`
**Allows to add client-side JS to the header and queue up for minification on production**<br />
[View commit for more details](https://github.com/designcreateplay/NodeBB/commit/5357ad61db6c15bc25a7e836548a02fadd72e6b3)<br />
See Example: [Mousetrap](https://github.com/psychobunny/nodebb-plugin-mousetrap/)

### `filter:uploadImage`

### `filter:uploadFile`


## Actions

### `action:app.load`

**Compatibility: v0.1.2+**<br />
**Argument(s)**: None

Executed when NodeBB is loaded, used to kickstart scripts in plugins (i.e. cron jobs, etc)

### `action:page.load`

**Compatibility: v0.1.1+**<br />
**Argument(s)**: An object containing the following properties:

* `template` - The template loaded
* `url` - Path to the page (relative to the site's base url)

### `action:plugin.activate`

**Compatibility: v0.0.8+/v0.1.0+**<br />
**Argument(s)**: A String containing the plugin's `id` (e.g. `nodebb-plugin-markdown`)

Executed whenever a plugin is activated via the admin panel.

**Important**: Be sure to check the `id` that is sent in with this hook, otherwise your plugin will fire its registered hook method, even if your plugin was not the one that was activated.

### `action:plugin.deactivate`

**Compatibility: v0.0.8+/v0.1.0+**<br />
**Argument(s)**: A String containing the plugin's `id` (e.g. `nodebb-plugin-markdown`)

Executed whenever a plugin is deactivated via the admin panel.

**Important**: Be sure to check the `id` that is sent in with this hook, otherwise your plugin will fire its registered hook method, even if your plugin was not the one that was deactivated.

### `action:post.save`

**Compatibility: v0.0.6+**<br />
**Argument(s)**: A post object (javascript Object)

Executed whenever a post is created or edited, after it is saved into the database.