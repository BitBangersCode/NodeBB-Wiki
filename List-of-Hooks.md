The following is a list of all hooks present in NodeBB. This list is intended to guide developers who are looking to write plugins for NodeBB. For more information, please consult [[Writing Plugins for NodeBB]].

There are two types of hooks, **filters**, and **actions**. Filters take an input (provided as a single argument), parse it in some way, and return the changed value. Actions take multiple inputs, and execute actions based on the inputs received. Actions do not return anything.

**Important**: This list is by no means exhaustive. Hooks are added on an as-needed basis (or if we can see a potential use case ahead of time), and all requests to add new hooks to NodeBB should be sent to us via the [issue tracker](https://github.com/designcreateplay/NodeBB/issues).

----

## Filters

### `filter:post.save`

**Compatibility: v0.0.5+**<br />
**Argument(s)**: A post's content (markdown text)

Executed whenever a post is created or edited, but before it is saved into the database.

### `filter:post.get`

**Compatibility: v0.0.6+**<br />
**Argument(s)**: A post's content (markdown text)

Executed whenever a post is retrieved, but before being sent to the client.

## Actions

### `action:post.save`

**Compatibility: v0.0.5+**<br />
**Argument(s)**: A new post's `pid`, the post's content (markdown text)

Executed whenever a post is created or edited, after it is saved into the database.