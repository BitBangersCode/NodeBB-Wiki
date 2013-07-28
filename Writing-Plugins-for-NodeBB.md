So you want to write a plugin for NodeBB, that's fantastic! There are a couple of things you need to know before starting that will help you out.

Like WordPress, NodeBB's plugins are built on top of a hook system in NodeBB. This system exposes parts of NodeBB to plugin creators in a controlled way, and allows them to alter content while it passes through, or execute certain behaviours when triggered.

The complete list of hooks built into NodeBB can be found at [[List of Hooks]]

## Filters and Actions

There are two types of hooks: **filters** and **actions**.

*Filters* act on content, and can be useful if you want to alter certain pieces of content as it passes through NodeBB. For example, a filter may be used to alter posts so that any occurrences of "apple" gets changed to "orange". Likewise, filters may be used to beautify content (i.e. code filters), or remove offensive words (profanity filters).

*Actions* are executed at certain points of NodeBB, and are useful if you'd like to *do* something after a certain trigger. For example, an action hook can be used to notify an admin if a certain user has posted. Other uses include analytics recording, or automatic welcome posts on new user registration.

When you are writing your plugin, make sure a hook exists where you'd like something to happen. If a hook isn't present, [file an issue](https://github.com/designcreateplay/NodeBB/issues) and we'll include it in the next version of NodeBB.

## `plugin.json`

Each plugin package contains a configuration file called `plugin.json`. Here is a sample:

    {
        "id": "my-plugin",
        "library": "./my-plugin.js",
        "hooks": [
            { "hook": "filter:save_post_content", "method": "filter" },
            { "hook": "action:save_post_content", "method": "emailme" }
        ]
    }

The `id` property is a unique name that identifies the plugin.

The `library` property is a relative path to the library in your package. It is automatically loaded by NodeBB (if the plugin is activated).

The `hooks` property is an array containing objects that tell NodeBB which hooks are used by your plugin, and what method in your library to invoke when that hook is called. Each object contains the following properties (those with a * are required):

* `data.hook`*, the name of the NodeBB hook
* `data.method`*, the method called in your plugin
* `data.callbacked`, whether or not the hook expects a callback (true), or a return (false). Only used for filters. (Default: false)
* (Not implemented) `data.priority`, the relative priority of the method when it is eventually called (default: 10)

## Writing the plugin library

The core of your plugin is your library file, which gets automatically included by NodeBB if your plugin is activated.

Each method you write into your library takes a certain number of arguments, depending on how it is called:

* Filters send a single argument through to your method, although asynchronous methods can also accept a callback (if specified in `plugin.json`).
* Actions send a number of arguments (the exact number depends how the hook is implemented). These arguments are listed in [[List of Hooks]].