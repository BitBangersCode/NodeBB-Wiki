1 . load tinymce
Add some in "header.tpl"

node_modules/nodebb-theme-lavender/templates/header.tpl

`        <script>
                var RELATIVE_PATH = "{relative_path}";
        </script>

<script type="text/javascript" src="http://www.chinagame.me/static/game/js/jquery.min.js"></script>

<script type="text/javascript" src="http://www.chinagame.me/static/tinymce/js/tinymce/jquery.tinymce.min.js"></script>
<script type="text/javascript" src="http://www.chinagame.me/static/tinymce/js/tinymce/tinymce.min.js"></script>
<script>

function loadtinymce()
{
        tinymce.init({
    selector: "textarea",
    theme: "modern",
    plugins: [
        "advlist autolink lists link image charmap print preview hr anchor pagebreak",
        "searchreplace wordcount visualblocks visualchars code fullscreen",
        "insertdatetime media nonbreaking save table contextmenu directionality",
        "emoticons template paste textcolor"
    ],
    toolbar1: "insertfile undo redo | styleselect | bold italic | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | link image",
    toolbar2: "print preview media | forecolor backcolor emoticons",
    image_advtab: true,
    templates: [
        {title: 'Test template 1', content: 'Test 1'},
        {title: 'Test template 2', content: 'Test 2'}
    ]
        });


}



</script>`

2. modify node_modules/nodebb-theme-vanilla/templates/composer.tpl
hide toolbar:
` <div class="btn-toolbar formatting-bar" style="visibility: hidden;">`

3. hide 

`<li class="active" style="visibility: hidden;"><a data-pane=".tab-write" data-toggle="tab">[[topic:composer.write]]</a></li>
                        <li style="visibility: hidden;"><a data-pane=".tab-preview" data-toggle="tab">[[topic:composer.preview]]</a></li>
                        <li class="hidden" style="visibility: hidden;"><a data-pane=".tab-help" data-toggle="tab">[[topic:composer.help]]</a></li>
                        <li class="btn-group pull-right action-bar">
                                <button class="btn btn-default" data-action="discard" tabIndex="5"><i class="fa fa-times"></i> [[topic:composer.discard]]</button>
                                <button data-action="post" class="btn btn-default btn-primary" tabIndex="3"><i class="fa fa-check"></i> [[topic:composer.submit]]</button>
                        </li>`

3. modify public/src/modules/composer.js
add loadtinymce()
to function end:
`composer.activateReposition = function(post_uuid) {
....
......
loadtinymce()
}
`

4 . tinyMCE data to textarea

`composer.post = function(post_uuid) {
                var mcecontent = tinyMCE.activeEditor.getContent({format : 'raw'});
                var postData = composer.posts[post_uuid],
                        postContainer = $('#cmp-uuid-' + post_uuid),
                        titleEl = postContainer.find('.title'),
                        bodyEl = postContainer.find('textarea'),
                        thumbEl = postContainer.find('input#topic-thumb-url');

                //console.log(mcecontent);
                //console.log(bodyEl.val());

                bodyEl.val(mcecontent);
`

5. load textarea content to tinyMCE

`        composer.editPost = function(pid) {
                if(allowed()) {
                        socket.emit('modules.composer.push', pid, function(err, threadData) {
                                if(err) {
                                        return app.alertError(err.message);
                                }
                                push({
                                        pid: pid,
                                        title: threadData.title,
                                        body: threadData.body,
                                        modified: false,
                                        isMain: !threadData.index,
                                        topic_thumb: threadData.topic_thumb
                                });
                                tinyMCE.activeEditor.setContent(threadData.body); //
                        });

                }

        };
` 

6 . delete parse html TAG

`        PostTools.parse = function(raw, callback) {
                raw = raw || '';

                /*plugins.fireHook('filter:post.parse', raw, function(err, parsed) {
                        callback(null, !err ? parsed : oraw);
                });*/
                callback(null,raw);
        };

        PostTools.parseSignature = function(raw, callback) {
                raw = raw || '';

                callback(null,raw);
                /*plugins.fireHook('filter:post.parseSignature', raw, function(err, parsedSignature) {
                        callback(null, !err ? parsedSignature : oraw);
                });*/
        };`

7. tar.gz file
fixtinymce-20140404.tar.gz