**plugin.json**

{
      "id": "nodebb-plugin-youtube"
    , "name": "NodeBB YouTube Plugin"
    , "description": "NodeBB Plugin that enables users to embed YouTube videos inline in their posts."
    , "url": "https://github.com/psychobunny/nodebb-plugin-youtube"
    , "library": "./library.js"
    , "hooks": [
        {
            "hook": "filter:post.parse"
            , "method": "parse"
            , "callbacked": true
        }
    ]
}

**library.js**

/*
	nodebb modules (eg db) have paths that are relative to the object javascript source file.
	nodejs modules (eg async) have no path.
*/

(function(Youtube) {
	'use strict'

	var	async = module.parent.require('async')
		db = module.parent.require('./database')

	Youtube.parse = function(postContent, callback) {
		postContent = postContent.replace(/<a href="(?:https?:\/\/)?(?:www\.)?(?:youtube\.com|youtu\.be)\/(?:watch\?v=)?(.+)<\/a>/g, '<iframe class="youtube-plugin" width="640" height="360" src="http://www.youtube.com/embed/$1" frameborder="0" allowfullscreen></iframe>')
		callback(null, postContent)
	}

}(module.exports))
