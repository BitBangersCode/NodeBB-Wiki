# Client Side Hooks

On the client-facing side, NodeBB fires off events and executes any handlers bound to the `window` object.

To attach a listener, do the following:

``` js
$(window).on('action:ajaxify.end', function(event, data) {
  console.log(data);  // to inspect that is passed back by NodeBB
});
```

* `filter:categories.new_topic`
* `action:popstate`
* `action:ajaxify.start`
* `action:ajaxify.loadingTemplates`
* `action:ajaxify.loadingData`
* `action:ajaxify.contentLoaded`
* `action:ajaxify.end`
* `action:reconnected`
* `action:connected`
* `action:disconnected`
* `action:categories.loading`
* `action:categories.loaded`
* `action:categories.new_topic.loaded`
* `action:topic.loading`
* `action:topic.loaded`
* `action:posts.loaded`
* `action:posts.edited`
* `action:composer.loaded`
* `action:chat.loaded`
* `action:tag.added`
* `action:widgets.loaded`