NodeBB version numbering follows the [semantic versioning] format after v0.1. Until then, the full upgraded steps provided at [[Upgrading NodeBB]] must be used in order to preserve data schema.

## Upcoming Releases / Roadmap

### v0.0.7
* Bootstrap 3 integration (issues [#168](https://github.com/designcreateplay/NodeBB/issues/168), [#169](https://github.com/designcreateplay/NodeBB/issues/169))
* Release of a default theme to be shipped with NodeBB
* Dynamically updating page URL to show post ([issue #185](https://github.com/designcreateplay/NodeBB/issues/185))
* Numerous updates to the chat module (issues [#169](https://github.com/designcreateplay/NodeBB/issues/169), [#208](https://github.com/designcreateplay/NodeBB/issues/208), [#209](https://github.com/designcreateplay/NodeBB/issues/209), [#210](https://github.com/designcreateplay/NodeBB/issues/210), [#211](https://github.com/designcreateplay/NodeBB/issues/211), [#213](https://github.com/designcreateplay/NodeBB/issues/213))
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
* Automatic updating of timestamps ([issue #306](https://github.com/designcreateplay/NodeBB/issues/306))
* CSRF fix for `/logout` route ([issue #315](https://github.com/designcreateplay/NodeBB/issues/315))
* Reduce unnecessary calls to Redis (re: category view) (issues [#320](https://github.com/designcreateplay/NodeBB/issues/320), [#321](https://github.com/designcreateplay/NodeBB/issues/321))
* Fixed script injection bug in post content ([issue #329](https://github.com/designcreateplay/NodeBB/issues/329))
* Login and `/outgoing` cancelation now take you back to the previous page ([issue #341](https://github.com/designcreateplay/NodeBB/issues/341))
* Asynchronous loading of middlewares ([issue #349](https://github.com/designcreateplay/NodeBB/issues/349))
* NodeBB now accessible via multiple addresses irrespective of `base_url` ([issue #356](https://github.com/designcreateplay/NodeBB/issues/356))

## Version History

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