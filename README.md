selfoss
=======

Copyright (c) 2013 Tobias Zeising, tobias.zeising@aditu.de  
http://selfoss.aditu.de  
Licensed under the GPLv3 license  
Version 2.1


INSTALLATION
------------

1. upload all files of this folder (IMPORTANT: also upload the invisible .htaccess files)
2. make the directories data/cache, data/favicons, data/logs, data/thumbnails, data/sqlite and public/ writeable
3. insert database access data in config.ini (you have not to change anything if you would like to use sqlite)
4. create cronjob for updating feeds and point it to http://<selfoss url>/update via wget or curl.


UPDATE
------

1. backup your database and your "data" folder
2. (IMPORTANT: don't delete the "data" folder) delete all old files and folders excluding the folder "data"
3. upload all new files and folders excluding the data folder (IMPORTANT: also upload the invisible .htaccess files)
4. Rename your folder /data/icons into /data/favicons
5. Delete the files /public/all.css and /public/all.js
6. Clean your browser cache
7. insert your current database connection and your individual configuration in config.ini. Important: we change the config.ini and add new options in newer versions. You have to update the config.ini too.


CHANGELOG
---------

Version 2.2-SNAPSHOT
* update fat free php Framework to 3.0.5

Version 2.1
* security bugfix

Version 2.0
* support of tags
* new user interface
* new interface for mobile devices
* mongodb database interface temporarily removed
* libs and third party plugins updated
* new spout for mmo-spy.de and golem.de with full text

Version 1.3
* search will now also search in the source title (for filtering by source)
* data/icons renamed in data/favicons for preventing mod_rewrite problems on apache
* improved scrolling for very long entries (thanks untitaker)
* Using more restrictive styles on entry content (thanks untitaker)
* redirect to base url on login/logout (thanks untitaker)
* improved base url handling

Version 1.2
* new json API for external software
* support for Android selfoss app
* improved heise spout
* some smaller bugfixes (e.g. increased session timeout)

Version 1.1
* hash password (you can set the salt in the config.ini and you can generate a password with following URL: http://your_selfoss_url.com/password)
* remove unused CSS
* minify JavaScript and CSS and collect them all in one all.js and all.css file
* activate caching and compression in .htaccess (if supported by current apache installation)
* code optimization and smaller bugfixes


CREDITS
-------

Special thanks to the great programmers of this libraries which will be used in selfoss:

* FatFree PHP Framework: http://fatfree.sourceforge.net/
* SimplePie: http://simplepie.org/
* jQuery: http://jquery.com/
* jQuery UI: http://jqueryui.com/
* WideImage: http://wideimage.sourceforge.net/
* htmLawed: http://www.bioinformatics.org/phplabware/internal_utilities/htmLawed/
* PHP Universal Feed Generator: http://www.ajaxray.com/blog/2008/03/08/php-universal-feed-generator-supports-rss-10-rss-20-and-atom/
* twitteroauth: https://github.com/abraham/twitteroauth
* floIcon: http://www.phpclasses.org/package/3906-PHP-Read-and-write-images-from-ICO-files.html
* keyboard shortcuts: http://www.openjs.com/scripts/events/keyboard_shortcuts/
* jsmin: https://github.com/rgrove/jsmin-php/blob/master/jsmin.php
* cssmin: http://code.google.com/p/cssmin/
* Spectrum Colorpicker: https://github.com/bgrins/spectrum
* jQuery custom content scroller: http://manos.malihu.gr/jquery-custom-content-scroller/

Icon Source: http://blog.artcore-illustrations.de/aicons/