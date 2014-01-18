### Hashes (Objects)
key **global**
```
{
"nextUid": "572",
"nextTid": "487",
"nextGid": "8",
"nextNid": "6208",
"nextCid": "13",
"nextMid": "1723",
"nextPid": "2889",
"userCount": "573",
"topicCount": "469",
"postCount": "2826",
}
```
key **user:[id]**
```
{
  "showemail": "0",
  "email": "test1@test.com",
  "uid": "300",
  "lastposttime": "0",
  "uploadedpicture": "",
  "banned": "0",
  "reputation": "0",
  "profileviews": "1",
  "birthday": "",
  "username": "ninja",
  "gravatarpicture": "http://www.gravatar.com/avatar/f2c97b1f2d2898cd2d6466ce95d4ba33?size=128&default=identicon&rating=pg",
  "signature": "",
  "location": "",
  "fullname": "",
  "joindate": "1383949222783",
  "userslug": "ninja",
  "website": "",
  "picture": "http://www.gravatar.com/avatar/f2c97b1f2d2898cd2d6466ce95d4ba33?size=128&default=identicon&rating=pg",
  "postcount": "0"
}
```

key **category:[id]**
```
{
"cid":"1",
"name":"Announcements",
"description":"Check here for announcments about NodeBB",
"icon":"fa-bullhorn",
"slug":"1/announcements",
"topic_count":"11",
"disabled":"0",
"order":"3",
"bgColor":"#0059b2",
"link":"",
"class":"col-md-3 col-xs-6",
"numRecentReplies":"2"
}
```

key **topic:[id]**
```
{
"tid":"300",
"uid":"382",
"cid":"7",
"title":"[nodebb-plugin-openid-steam] Steam/OpenID register/login",
"slug":"300/nodebb-plugin-openid-steam-steamopenid-registerlogin",
"timestamp":"1386363075518",
"lastposttime":"1387457563203",
"postcount":"9",
"viewcount":"221",
"locked":"0",
"deleted":"0",
"pinned":"0"
}
```

key **post:[id]**
```
{
"content":"ITS OVER 9000\n\n![over 9000](http://stream1.gifsoup.com/view/17416/it-s-over-9000-o.gif)",
"timestamp":"1387158935468",
"uid":"3",
"edited":"1387159006377",
"tid":"322",
"deleted":"0",
"reputation":"1",
"editor":"3",
"pid":"2000"
}
```

key **gid:[id]** // should be group:[id] to be consistent
```
{
"gid":"1",
"name":"Administrators",
"description":"Forum Administrators",
"deleted":"0"
}
```

key **notifications:[id]** //should be notification:[id] to be consistent
```
{
"uniqueId":"topic:115",
"path": "/topic/115",
"text": "Vit_Prog has posted a reply to: \"Testing awesome node forum\"",
"datetime":"1384760394689"
}
```

key **message:[id]**
```
{
"touid": "2",
"timestamp": "1377573874790",
"content": "hi this forum is awesome",
"fromuid": "20"
}
```

key **config** 
```
{
"allowFileUploads":"0",
"allowGuestPosting":"1",
"allowGuestSearching":"0",
"allowRegistration":"1",
"brand:favicon":"",
"brand:logo":"",
"chatMessagesToDisplay":"50",
"description":"",
"disableSignatures":"0",
"disableSocialButtons":"0",
"email:from":"yoursite@domain.com",
"email:smtp:host":"",
"email:smtp:port":"",
"ga:domain":"yourdomain.org",
"ga:id":"xxx",
"imgurClientID":"xxxxxx",
"keywords":"",
"maximumFileSize":"2048"
"maximumProfileImageSize":"256",
"maximumSignatureLength":"255",
"maximumTitleLength":"255",
"maximumUsernameLength":"16",
"minimumPasswordLength":"6",
"minimumPostLength":"8",
"minimumTitleLength":"3",
"minimumUsernameLength":"2",
"motd":"",
"nodebb-plugin-markdown:options:breaks":"1",
"nodebb-plugin-markdown:options:gfm":"1",
"nodebb-plugin-markdown:options:highlight":"1",
"nodebb-plugin-markdown:options:langPrefix":"lang-",
"nodebb-plugin-markdown:options:pedantic":"0",
"nodebb-plugin-markdown:options:sanitize":"1",
"nodebb-plugin-markdown:options:smartLists":"1",
"nodebb-plugin-markdown:options:smartypants":"0",
"nodebb-plugin-markdown:options:tables":"1",
"postDelay":"2",
"postageapp:apiKey":"xxx",
"privileges:disabled":"0",
"privileges:manage_content":"1000",
"privileges:manage_topic":"1000",
"profile:convertProfileImageToPNG":"0",
"robots.txt":"",
"show_motd":"1",
"social:facebook:app_id":"xxx",
"social:facebook:secret":"xxx",
"social:google:id":""
"social:google:secret":"",
"social:twitter:key":"xxx",
"social:twitter:secret":"xxx",
"theme:id":"nodebb-theme-cerulean",
"theme:src":"",
"theme:staticDir":"",
"theme:templates":"",
"theme:type":"local",
"title":"NodeBB",
"useOutgoingLinksPage":"0",
}
```
## Sets
//TODO:
## Sorted Sets
//TODO:
## Lists
//TODO: