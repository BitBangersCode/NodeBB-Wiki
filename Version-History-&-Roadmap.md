To upgrade your NodeBB, please follow the upgrade steps provided at [[Upgrading NodeBB]].

## Upcoming Releases / Roadmap

### v0.2.1

* Revamped Email System (issues [#326](https://github.com/designcreateplay/NodeBB/issues/326), [#335](https://github.com/designcreateplay/NodeBB/issues/335))

## Version History

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