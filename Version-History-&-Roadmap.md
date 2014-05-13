To upgrade your NodeBB, please follow the upgrade steps provided at [[Upgrading NodeBB]].

## Upcoming Releases / Roadmap



## Version History

### 0.4.3

This release is a security update that addresses an issue affecting all 0.4.x versions of NodeBB. Administrators are advised to update as soon as possible.

* [Custom content can be added to the post composer's "Help" tab](https://github.com/designcreateplay/NodeBB/issues/1149)
* [Account locking after configurable # of unsuccessful login attemps](https://github.com/designcreateplay/NodeBB/issues/1453)
* [Multiple flags auto-ban a user](https://github.com/designcreateplay/NodeBB/issues/1483)
* [Better handling of access to pages that require login](https://github.com/designcreateplay/NodeBB/issues/1495)
* [Daily digest emails now opt-in instead of opt-out](https://github.com/designcreateplay/NodeBB/issues/1499)
* [Tweaked avatar resizing](https://github.com/designcreateplay/NodeBB/issues/1515)

### 0.4.2
* **New Languages** - American English (en_US), Japanese (jp), Lithuanian (lt), Malay (ms)
* [Better Groups handling and integration with Mentions plugin](https://github.com/designcreateplay/NodeBB/issues/1331)
* [User selectable languages](https://github.com/designcreateplay/NodeBB/issues/1013)
* Better robot detection for registration via Project Honey Pot plugin
* [Updating a theme's `package.json` no longer requires the theme to be re-activated](https://github.com/designcreateplay/NodeBB/issues/907)
* [Languages can be selected by individual users](https://github.com/designcreateplay/NodeBB/issues/1013)
* ["Username is typing" in chat window](https://github.com/designcreateplay/NodeBB/issues/1139)
* [Email Digests](https://github.com/designcreateplay/NodeBB/issues/1249)
* [Ability for plugins to use the sounds subsystem](https://github.com/designcreateplay/NodeBB/issues/1270)
* [NodeBB won't automatically restart every time a plugin or theme is activated now](https://github.com/designcreateplay/NodeBB/issues/1351)
* [Duplicate username handling](https://github.com/designcreateplay/NodeBB/issues/1372)
* [LevelDB Support](https://github.com/designcreateplay/NodeBB/issues/1373)
* [Ability to select multiple topics to move/delete/etc](https://github.com/designcreateplay/NodeBB/issues/1398)
* [Guest posting](https://github.com/designcreateplay/NodeBB/issues/1410) [problems resolved](https://github.com/designcreateplay/NodeBB/issues/1412)
* [.getTeaser() endpoint](https://github.com/designcreateplay/NodeBB/issues/1422)
* [Plugins can now also be installed/removed directly from the ACP](https://github.com/designcreateplay/NodeBB/issues/1426)
* [Gravatar Fallbacks](https://github.com/designcreateplay/NodeBB/issues/1432)
* [When you create a new topic, you will be sent there](https://github.com/designcreateplay/NodeBB/issues/1439)
* [Modals can now be resized](https://github.com/designcreateplay/NodeBB/issues/1472)

### v0.4.1

* **New Languages** - Estonian (et), and just for fun, Pirate English (en@pirate)
* [Scrolling up will show a "Loading more Posts" indicator](https://github.com/designcreateplay/NodeBB/issues/1186)
* [Widget](https://github.com/designcreateplay/NodeBB/issues/1304) [system](https://github.com/designcreateplay/NodeBB/issues/1312) [fixes](https://github.com/designcreateplay/NodeBB/issues/1313)
* [Tweaks to how "Reply" and "Quote" buttons work](https://github.com/designcreateplay/NodeBB/issues/1316)
* [`./nodebb reset` fleshed out into four separate commands: `plugins`, `themes`, `widgets`, or `all`](https://github.com/designcreateplay/NodeBB/issues/1317)
* [A user's profile now contains a list of topics they have created](https://github.com/designcreateplay/NodeBB/issues/1318)
* [Log files now always contained in `./logs`](https://github.com/designcreateplay/NodeBB/issues/1321)
* [Fixed issue where a newly rendered post's options were reflective of the poster, and not of the viewer](https://github.com/designcreateplay/NodeBB/issues/1322)
* [Fixed issue where the Bootswatch list wouldn't load if behind HTTPS](https://github.com/designcreateplay/NodeBB/issues/1325)
* [Faster restarts](https://github.com/designcreateplay/NodeBB/issues/1328)
* [Social Media share of the homepage should default to the forum brand first](https://github.com/designcreateplay/NodeBB/issues/1334)
* [Fixed the user search page](https://github.com/designcreateplay/NodeBB/issues/1335)
* [Username mentions less buggy](https://github.com/designcreateplay/NodeBB/issues/1339)
* [SVGs now supported for category pictures](https://github.com/designcreateplay/NodeBB/pull/1344)
* [When a user is deleted, they will also be immediately logged out](https://github.com/designcreateplay/NodeBB/issues/1346)
* [Better options for marking "unread" messages as read](https://github.com/designcreateplay/NodeBB/issues/1353)
* [Fixed broken Themes page if widget-essentials is not enabled](https://github.com/designcreateplay/NodeBB/issues/1358)

### v0.4.0 ([Notes](http://community.nodebb.org/topic/865/gotchas-for-v0-4-0))

* **New Languages** - Polish (pl), Dutch (nl), Thai (th), Sardinian (sc), Persian (fa_IR)
* [Plugins can now use LESS stylesheets. Developers are encouraged to use LESS instead of CSS.](https://github.com/designcreateplay/NodeBB/issues/1168)
* [Daily Digest emails](https://github.com/designcreateplay/NodeBB/issues/326) - Sent *only* if you have unread notifications
* [User Deletion](https://github.com/designcreateplay/NodeBB/issues/746)
* [Notifications Dropdown now shows user avatars](https://github.com/designcreateplay/NodeBB/issues/852)
* Search subsystem modularified (see `nodebb-plugin-dbsearch`)
* [Better SEO metadata](https://github.com/designcreateplay/NodeBB/issues/1027)
* [Administrators can change user passwords](https://github.com/designcreateplay/NodeBB/issues/1044)
* [Tracking of IP Addresses](https://github.com/designcreateplay/NodeBB/issues/1045)
* Widgets system for inclusion on non-standard elements (text/html snippets, etc)
* [Sounds are played when notifications are received, and when chat messages are sent and received](https://github.com/designcreateplay/NodeBB/issues/1131)
* [The "Recent Replies" block should update automatically when new posts arrive](https://github.com/designcreateplay/NodeBB/issues/1138)
* [Users can now log in via an email address](https://github.com/designcreateplay/NodeBB/issues/1175)
* [Chat modal now contains user status](https://github.com/designcreateplay/NodeBB/issues/1229)
* [Better avatar cropping](https://github.com/designcreateplay/NodeBB/issues/1240)
* [Notifications when posts are upvoted or favourited](https://github.com/designcreateplay/NodeBB/issues/1184)

### v0.3.2

* **New Languages** - Swedish (sv), Russian (ru), Italian (it), and Hebrew (he)
* [Flagging a post now requires a confirmation step](https://github.com/designcreateplay/NodeBB/issues/939)
* [Post composer UI enhancements](https://github.com/designcreateplay/NodeBB/issues/943)
* [Administrators can now see "invisible" users](https://github.com/designcreateplay/NodeBB/issues/929)
* [**Upvoting and Downvoting**](https://github.com/designcreateplay/NodeBB/issues/955)
* [**Moderators**](https://github.com/designcreateplay/NodeBB/issues/961)
* [Optional Pagination instead of infinite scrolling](https://github.com/designcreateplay/NodeBB/issues/986)
* [Ability to preview a post before submitting it](https://github.com/designcreateplay/NodeBB/issues/975)
* [Refactoring of the RSS system](https://github.com/designcreateplay/NodeBB/issues/973) (thanks @miksago/@TeamKano!)
* [Better handling of cache busters in non-git environments](https://github.com/designcreateplay/NodeBB/issues/1006)
* [Optional `themes_path` in case your theme is not an npm package](https://github.com/designcreateplay/NodeBB/pull/1020)
* [Warnings when a NodeBB install does not satisfy a plugin's `minver`](https://github.com/designcreateplay/NodeBB/issues/997)
* [Performance enhancements re: Notification pruning](https://github.com/designcreateplay/NodeBB/issues/999)
* [Ability to use a different config file if defined via `--config` flag](https://github.com/designcreateplay/NodeBB/issues/1025)
* Lots of bug fixes!

### v0.3.1

* Traditional Chinese (zh_tw), Slovak (sk), Finnish (fi), Brazilian Portuguese (pt_br), Turkish (tr), Norwegian Bokmål (nb), and Hungarian (hu) languages have been added
* Translations now handled by [Transifex](https://www.transifex.com/projects/p/nodebb/)
* Updates to the plugin system
* UI Fixes for the post composer
* Single sign on packages are their own npm packages now, reducing the size of the main core codebase
* Pagination, for those who really want pages
* Improvements to the mentions engine
* "Remember Me" option when logging in
* Tweaked permission control, users with no write access shouldn't see "Post/Reply" buttons anymore. Those without view permissions shouldn't be able to see hidden forums anymore.
* New User states (Away, Busy, Do Not Disturb)
* Post Flagging

### v0.3.0 ([Notes](http://community.nodebb.org/topic/436/gotchas-for-0-3-0))

* Various security and bug fixes, dataset optimizations
* Revamped Email System (issues [#326](https://github.com/designcreateplay/NodeBB/issues/326), [#335](https://github.com/designcreateplay/NodeBB/issues/335))
* Support for **four** new languages, Italian (it) and Czech (cs), Simplified Chinese (zh_CN), and Arabic (ar)
* [Topic forking](https://github.com/designcreateplay/NodeBB/issues/524)
* [Category outgoing links](https://github.com/designcreateplay/NodeBB/issues/665)
* [Moving posts between topics](https://github.com/designcreateplay/NodeBB/issues/667)
* [Support for usernames with unicode characters](https://github.com/designcreateplay/NodeBB/issues/724)
* [Ability to select board language via Admin Panel](https://github.com/designcreateplay/NodeBB/issues/728)
* [Ability to override the default `robots.txt`](https://github.com/designcreateplay/NodeBB/issues/732)
* [Ability to change usernames](https://github.com/designcreateplay/NodeBB/issues/745)
* [Fixed issue where client side was getting old client-side js](https://github.com/designcreateplay/NodeBB/issues/784)
* [Fixes to French translation](https://github.com/designcreateplay/NodeBB/pull/790)
* New composer styling (at bottom of screen)
* Instant Messaging / Chat front-end rewritten
* Web Socket backend rewritten

### v0.2.1

* Desktop Notifications (via [Notifications API](https://developer.mozilla.org/en-US/docs/Web/API/notification) -- thanks @psychobunny)
* Chat Modal fixes (issues [#690](https://github.com/designcreateplay/NodeBB/issues/690), [#691](https://github.com/designcreateplay/NodeBB/issues/691), [#697](https://github.com/designcreateplay/NodeBB/issues/645))
* Topic RSS feeds now working again ([issue #703](https://github.com/designcreateplay/NodeBB/issues/703))
* Restriction on topic and category title lengths ([issue #705](https://github.com/designcreateplay/NodeBB/issues/705))
* Unicode Slugs ([issue #708](https://github.com/designcreateplay/NodeBB/issues/708))
* Social sharing buttons can now be hidden via admin panel option ([issue #712](https://github.com/designcreateplay/NodeBB/issues/712))
* [[Upgrade steps|Upgrading NodeBB]] have been simplified

### v0.2.0

* Unread notifications are now automatically marked read when a topic is accessed ([issue #219](https://github.com/designcreateplay/NodeBB/issues/219))
* Third-party plugins can now introduce scripts into NodeBB ([issue #400](https://github.com/designcreateplay/NodeBB/issues/400))
* Privilege Thresholds can now be disabled, if desired ([issue #528](https://github.com/designcreateplay/NodeBB/issues/528))
* Better responsive handling (issues [#539](https://github.com/designcreateplay/NodeBB/issues/539), [#552](https://github.com/designcreateplay/NodeBB/issues/552))
* New permissions system ([issue #565](https://github.com/designcreateplay/NodeBB/issues/565))
* System-only user groups ([issue #566](https://github.com/designcreateplay/NodeBB/issues/566))
* Ability to upload multiple images in multiple composers ([issue #575](https://github.com/designcreateplay/NodeBB/issues/575))
* Search Re-indexing is no longer open to public ([issue #579](https://github.com/designcreateplay/NodeBB/issues/579))
* Cache buster ([issue #586](https://github.com/designcreateplay/NodeBB/issues/586))
* Notification count now shown in favicon ([issue #610](https://github.com/designcreateplay/NodeBB/issues/610))
* Dropdown added to show recently chatted-with users ([issue #615](https://github.com/designcreateplay/NodeBB/issues/615))
* Socket reconnection rejoins rooms that were inadvertently left on disconnection ([issue #652](https://github.com/designcreateplay/NodeBB/issues/652))
* Language files for Spanish, French, and German
* Bug Fixes ([#396](https://github.com/designcreateplay/NodeBB/issues/396), [#435](https://github.com/designcreateplay/NodeBB/issues/435), [#519](https://github.com/designcreateplay/NodeBB/issues/519), [#553](https://github.com/designcreateplay/NodeBB/issues/553), [#557](https://github.com/designcreateplay/NodeBB/issues/557), [#560](https://github.com/designcreateplay/NodeBB/issues/560), [#616](https://github.com/designcreateplay/NodeBB/issues/616), [#619](https://github.com/designcreateplay/NodeBB/issues/619))

### v0.1.1

v0.1.1 is contains several security fixes -- users are encouraged to upgrade to this version as soon as possible.

* Logging out should return you to where you were previously ([issue #358](https://github.com/designcreateplay/NodeBB/issues/493))
* Fixed an issue with image uploading ([issue #497](https://github.com/designcreateplay/NodeBB/issues/497))
* New installs should no longer ask you to update the schema ([issue #502](https://github.com/designcreateplay/NodeBB/issues/502))
* Password reset is no longer available to people who have not set up email ([issue #507](https://github.com/designcreateplay/NodeBB/issues/507))
* Clicking on incoming chats now works in the `/notifications` page ([issue #514](https://github.com/designcreateplay/NodeBB/issues/514))
* Minor bug re: themes not switching properly ([issue #517](https://github.com/designcreateplay/NodeBB/issues/517))
* Interstitial `/outgoing` page now refers to the site title, not "NodeBB" ([issue #518](https://github.com/designcreateplay/NodeBB/issues/518))
* [Google Analytics!](https://github.com/julianlam/nodebb-plugin-google-analytics) ([issue #522](https://github.com/designcreateplay/NodeBB/issues/522))
* Minor improvement to the composer ([issue #525](https://github.com/designcreateplay/NodeBB/issues/525))
* Security issue re: `/plugins/fireHook` ([issue #533](https://github.com/designcreateplay/NodeBB/issues/533))
* Made the Register/Login link more obvious ([issue #535](https://github.com/designcreateplay/NodeBB/issues/535))
* Recent topics now have a corresponding RSS feed ([issue #536](https://github.com/designcreateplay/NodeBB/issues/536))
* Categories can now be selected via hexadecimal colour codes ([issue #540](https://github.com/designcreateplay/NodeBB/issues/540))

### v0.1.0
* Better notifications handling ([issue #219](https://github.com/designcreateplay/NodeBB/issues/219))
* Category ordering ([issue #288](https://github.com/designcreateplay/NodeBB/issues/288))
* Stylistic revamp of the category view (topic listing) ([issue #333](https://github.com/designcreateplay/NodeBB/issues/333))
* Dedicated notifications page (`/notifications`) ([issue #336](https://github.com/designcreateplay/NodeBB/issues/336))
* Handling of expired notifications ([issue #337](https://github.com/designcreateplay/NodeBB/issues/337))
* Updates to the admin panel ([issue #338](https://github.com/designcreateplay/NodeBB/issues/338))
* New hooks: `filter:avatar.get`, `action:avatar.save` ([issue #340](https://github.com/designcreateplay/NodeBB/issues/340))
* Ability to disable the `/outgoing` page on link click ([issue #345](https://github.com/designcreateplay/NodeBB/issues/345))
* Changes to settings in the admin panel no longer require a restart ([issue #353](https://github.com/designcreateplay/NodeBB/issues/353))
* Socket disconnections are less obtrusive ([issue #354](https://github.com/designcreateplay/NodeBB/issues/354))
* Better handling of images on mobile responsive view ([issue #374](https://github.com/designcreateplay/NodeBB/issues/374))
* NodeBB now responds properly to all hostnames ([issue #375](https://github.com/designcreateplay/NodeBB/issues/375))
* Plugins can now route CSS files to be loaded ([issue #383](https://github.com/designcreateplay/NodeBB/issues/383))
* `/recent/` now lists topics from the last 7 days ([issue #394](https://github.com/designcreateplay/NodeBB/issues/394))
* Fixes to the chat modal (issues [#397](https://github.com/designcreateplay/NodeBB/issues/397), [#434](https://github.com/designcreateplay/NodeBB/issues/434))
* Better SEO handling (theoretically...) ([issue #401](https://github.com/designcreateplay/NodeBB/issues/401))
* More plugin hooks ([issues [#402](https://github.com/designcreateplay/NodeBB/issues/402), [#407](https://github.com/designcreateplay/NodeBB/issues/407))
* Better IE9 compatibility ([issue #417](https://github.com/designcreateplay/NodeBB/issues/417))
* Theme engine now takes themes from NPM only ([issue #418](https://github.com/designcreateplay/NodeBB/issues/418))
* Header brand can now be an image, text, or both ([issue #425](https://github.com/designcreateplay/NodeBB/issues/425))
* Tweaks to the top bar (user profile) ([issue #426](https://github.com/designcreateplay/NodeBB/issues/426))
* Themes can now use static assets (images, backgrounds, etc) ([issue #427](https://github.com/designcreateplay/NodeBB/issues/427))
* The footer now only appears on the `/` route ([issue #429](https://github.com/designcreateplay/NodeBB/issues/429))
* Updates to the way pinned topics are handled internally (issues [#433](https://github.com/designcreateplay/NodeBB/issues/433), [#457](https://github.com/designcreateplay/NodeBB/issues/457))
* Fixes to the privilege thresholds ([issue #445](https://github.com/designcreateplay/NodeBB/issues/445))
* Username login in no longer case sensitive [issue #448](https://github.com/designcreateplay/NodeBB/issues/448))
* Notification dropdown now properly handles long titles ([issue #452](https://github.com/designcreateplay/NodeBB/issues/452))
* Locally installed plugins are no longer supported ([issue #455](https://github.com/designcreateplay/NodeBB/issues/455))
* Added an "Admin" button to the top bar, for admins ([issue #459](https://github.com/designcreateplay/NodeBB/issues/459))
* Banning a user now takes effect immediately ([issue #462](https://github.com/designcreateplay/NodeBB/issues/462))
* Plugins can now be turned on and off without a server restart ([issue #478](https://github.com/designcreateplay/NodeBB/issues/478))

### v0.0.7 ([Milestone issues](https://github.com/designcreateplay/NodeBB/issues?milestone=7&state=closed))
* Bootstrap 3 integration (issues [#168](https://github.com/designcreateplay/NodeBB/issues/168), [#169](https://github.com/designcreateplay/NodeBB/issues/169))
* Release of a default theme to be shipped with NodeBB
* Dynamically updating page URL to show post ([issue #185](https://github.com/designcreateplay/NodeBB/issues/185))
* Numerous updates to the chat module (issues [#169](https://github.com/designcreateplay/NodeBB/issues/169), [#208](https://github.com/designcreateplay/NodeBB/issues/208), [#209](https://github.com/designcreateplay/NodeBB/issues/209), [#210](https://github.com/designcreateplay/NodeBB/issues/210), [#211](https://github.com/designcreateplay/NodeBB/issues/211), [#213](https://github.com/designcreateplay/NodeBB/issues/213))
* Dedicated NodeBB Theme ([issue #195](https://github.com/designcreateplay/NodeBB/issues/195))
* Topic-based notifications are automatically marked read if you go to the topic directly ([issue #219](https://github.com/designcreateplay/NodeBB/issues/219))
* Category creation ([issue #228](https://github.com/designcreateplay/NodeBB/issues/228))
* Better search results + user searching (issues [#205](https://github.com/designcreateplay/NodeBB/issues/205), [#229](https://github.com/designcreateplay/NodeBB/issues/229))
* User Groups ([issue #230](https://github.com/designcreateplay/NodeBB/issues/230))
* `nodebb-plugin-markdown` now sanitizes HTML input by default (issues [#214](https://github.com/designcreateplay/NodeBB/issues/214), [#251](https://github.com/designcreateplay/NodeBB/issues/251))
* Fixed javascript-less view of NodeBB ([issue #253](https://github.com/designcreateplay/NodeBB/issues/253))
* Dropped use of [node-rss](https://npmjs.org/package/node-rss) in favour of [rss](https://npmjs.org/package/rss) ([issue #258](https://github.com/designcreateplay/NodeBB/issues/258))
* Links to RSS feeds are now shown in the breadcrumbs ([issue #259](https://github.com/designcreateplay/NodeBB/issues/259))
* Maximum password length restriction removed ([issue #261](https://github.com/designcreateplay/NodeBB/issues/261))
* Better installation script (issues [#264](https://github.com/designcreateplay/NodeBB/issues/264), [#265](https://github.com/designcreateplay/NodeBB/issues/265), [#266](https://github.com/designcreateplay/NodeBB/issues/266), [#275](https://github.com/designcreateplay/NodeBB/issues/275))
* Added Heroku support (dynamic port via the `PORT` environment variable)
* Minor refactoring of saved data (issues [#286](https://github.com/designcreateplay/NodeBB/issues/286), [#287](https://github.com/designcreateplay/NodeBB/issues/287), [#303](https://github.com/designcreateplay/NodeBB/issues/304))
* Drag/drop uploaded images are now placed inline instead of attachment-style ([issue #294](https://github.com/designcreateplay/NodeBB/issues/294))
* Automatic updating of timestamps ([issue #306](https://github.com/designcreateplay/NodeBB/issues/306))
* CSRF fix for `/logout` route ([issue #315](https://github.com/designcreateplay/NodeBB/issues/315))
* Reduce unnecessary calls to Redis (re: category view) (issues [#320](https://github.com/designcreateplay/NodeBB/issues/320), [#321](https://github.com/designcreateplay/NodeBB/issues/321))
* Online users' page (`/users/online`) ([issue #323](https://github.com/designcreateplay/NodeBB/issues/323))
* Fixed script injection bug in post content ([issue #329](https://github.com/designcreateplay/NodeBB/issues/329))
* Login and `/outgoing` cancelation now take you back to the previous page ([issue #341](https://github.com/designcreateplay/NodeBB/issues/341))
* Asynchronous loading of middlewares ([issue #349](https://github.com/designcreateplay/NodeBB/issues/349))
* Some changes to the admin panel no longer require a restart ([issue #353](https://github.com/designcreateplay/NodeBB/issues/353))
* Revamped reconnection notification ([issue #354](https://github.com/designcreateplay/NodeBB/issues/354))
* NodeBB now accessible via multiple addresses irrespective of `base_url` ([issue #356](https://github.com/designcreateplay/NodeBB/issues/356))
* Ability to bind NodeBB to a specific IP address ([issue #359](https://github.com/designcreateplay/NodeBB/pull/359))
* Topics now have a meta description tag ([issue #362](https://github.com/designcreateplay/NodeBB/issues/362))

### v0.0.6
* More user management options (bans, ip bans) ([issue #125](https://github.com/designcreateplay/NodeBB/issues/125))
* Introduction of dedicated `error.log`, with better logging capability
* Fulltext search through Reds
* Chat logs are now saved ([issue #109](https://github.com/designcreateplay/NodeBB/issues/109))
* Better page titles and notifications
* Username mentions ([issue #164](https://github.com/designcreateplay/NodeBB/issues/164)) - through use of [nodebb-plugin-mentions](https://github.com/julianlam/nodebb-plugin-mentions) package, included with all future installs
* Drag/Drop uploader fixes (Issues [#172](https://github.com/designcreateplay/NodeBB/issues/172), [#173](https://github.com/designcreateplay/NodeBB/issues/173), [#174](https://github.com/designcreateplay/NodeBB/issues/174), [#175](https://github.com/designcreateplay/NodeBB/issues/175), [#182](https://github.com/designcreateplay/NodeBB/issues/182))
* Favourited posts are now accessible via the user profile
* You can no longer access a deleted topic via its URL ([issue #198](https://github.com/designcreateplay/NodeBB/issues/198))
* Lots of bug fixes, stability upgrades, and refactoring to reduce technical debt

### v0.0.5
* Basic plugin system (with hooks and sample plugins) ([issue #143](https://github.com/designcreateplay/NodeBB/issues/143))
* Infinite scrolling on topics, categories and user pages ([issue #141](https://github.com/designcreateplay/NodeBB/issues/141))
* Better page titles ([issue #160](https://github.com/designcreateplay/NodeBB/issues/160))
* Improved notification handling ([issue #137](https://github.com/designcreateplay/NodeBB/issues/134))
* Category removal/disable ([issue #93](https://github.com/designcreateplay/NodeBB/issues/93))
* External link interpage ([issue #154](https://github.com/designcreateplay/NodeBB/issues/154))

### v0.0.4
* Theming manager to allow third-party bootstrap themes to be uploaded/installed ([issue #92](https://github.com/designcreateplay/NodeBB/issues/92))
* Ability to add/delete categories in the admin panel ([issue #93](https://github.com/designcreateplay/NodeBB/issues/93))
* `sitemap.xml` for better search engine indexing ([issue #96](https://github.com/designcreateplay/NodeBB/issues/96))
* Fixed Twitter Registrations ([issue #131](https://github.com/designcreateplay/NodeBB/issues/131))
* Open Graph tags present on most pages ([issue #116](https://github.com/designcreateplay/NodeBB/issues/116))
* Improved post composer styling ([issue #137](https://github.com/designcreateplay/NodeBB/issues/137), etc)
* Various UI fixes ([issue #95](https://github.com/designcreateplay/NodeBB/issues/95), etc)
* Bugfixes and stability updates

### v0.0.3 ([Milestone Issues](https://github.com/designcreateplay/NodeBB/issues?milestone=2&page=1&state=closed))
* Bugfixes and stability updates
* NodeBB can now be installed into a subfolder (e.g. example.org/forum)
* User and Category editing tools for the administration panel