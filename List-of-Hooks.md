The following is a list of all hooks present in NodeBB. This list is intended to guide developers who are looking to write plugins for NodeBB. For more information, please consult [[Writing Plugins for NodeBB]].

There are two types of hooks, **filters**, and **actions**. Filters take an input (provided as a single argument), parse it in some way, and return the changed value. Actions take multiple inputs, and execute actions based on the inputs received. Actions do not return anything.

----

## Filters

### `filter:save_post_content`

**Introduced: v0.0.5**
**Argument(s)**: A post's content (markdown text)

Executed whenever a post is created or edited, but before it is saved into the database.

## Actions

### `action:save_post_content`

**Introduced: v0.0.5**
**Argument(s)**: A new post's `pid`, the post's content (markdown text)

Executed whenever a post is created or edited, after it is saved into the database.