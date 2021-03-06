selfoss
=======

Copyright (c) 2013 Tobias Zeising, tobias.zeising@aditu.de  
http://selfoss.aditu.de  
Licensed under the GPLv3 license  
Version 2.4-SNAPSHOT


INSTALLATION
------------

1. Upload all files of this folder (IMPORTANT: also upload the invisible .htaccess files)
2. Make the directories data/cache, data/favicons, data/logs, data/thumbnails, data/sqlite and public/ writeable
3. Insert database access data in config.ini (see below -- you have not to change anything if you would like to use sqlite)
3. You don't have to install the database, it will be created automatically
4. Create cronjob for updating feeds and point it to http://yourselfossurl.com/update via wget or curl. You can also execute the update.php from commandline.

For further questions or on any problem use our support forum: http://selfoss.aditu.de/forum

CONFIGURATION
-------------

1. Copy defaults.ini to config.ini
2. Edit config.ini and delete any lines you do not wish to override
3. Do not delete the [globals] line
4. See http://selfoss.aditu.de/ for examples


UPDATE
------

1. backup your database and your "data" folder
2. (IMPORTANT: don't delete the "data" folder) delete all old files and folders excluding the folder "data"
3. upload all new files and folders excluding the data folder (IMPORTANT: also upload the invisible .htaccess files)
4. Rename your folder /data/icons into /data/favicons
5. Delete the files /public/all.css and /public/all.js
6. Clean your browser cache
7. insert your current database connection and your individual configuration in config.ini. Important: we change the config.ini and add new options in newer versions. You have to update the config.ini too.

For further questions or on any problem use our support forum: http://selfoss.aditu.de/forum


OPML Import
-----------

Visit the page http://yourselfossurl.com/opml for importing your OPML File. If you are a user of the google reader then use https://www.google.com/takeout/ to get all your feeds in one opml file.


CHANGELOG
---------

Version 2.4-SNAPSHOT
* prevent error on icons parsing error
* new homepage parameter (thanks a lot to Jean Baptiste Favre)
* new button for open an articles source
* no error message if no unread item is available and mark all as read was pressed
* improve logger
* readability is now available as spout instead as global parameter
* new share buttons for google+, twitter and facebook
* mysql use longtext for articles content
* improved detection of mobile devices
* allow more tags in articles content
* show unread items per tag in taglist (thanks a lot to Fedor Bezrukov)
* show list of sources for filtering (thanks a lot to Fedor Bezrukov)
* use more eye catching unread stats in main navigation
* show source title in selfoss RSS feed (thanks a lot to Darkwing1)
* load sources for update by last update time (thanks a lot to Lars Formella)
* Opening feed search focus the search input field
* Scroll blockquotes and pre on overflow (especially good for mobile devices)
* new option for automatically mark items as read
* new share buttons for email and pocket (thanks a lot to Francis Noel)
* new shortcut r for reloading the current list

Version 2.3
* new shortcut library jquery hotkeys (thanks a lot to Sigill)
* new shortcut for mark as read and switch to next in one step (thanks a lot to Sigill)
* prevent error on png conversion
* items will be saved in mysql databases also no icon is available
* support of PostgreSQL Database (thanks a lot to volkadav)
* now updates by command line are possible (thanks a lot to Jeppe Toustrup)
* default charset on mysql is utf8
* new readability support (thanks a lot to oxman)
* link to opml import added
* Use IfMoudule to avoid errors in Etags settings (thanks to vincebusam)
* Allow tag filtering to not include partial matches (thanks to WalterWeight and bsweeney)

Version 2.2
* update fat free php Framework to 3.0.5
* new opml import page (thanks a lot to Michael Moore)

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

Very special thanks to all contributors of pull requests here on github. Your improvements are awesome!!!

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
* jQuery hotkeys: https://github.com/tzuryby/jquery.hotkeys
* jsmin: https://github.com/rgrove/jsmin-php/blob/master/jsmin.php
* cssmin: http://code.google.com/p/cssmin/
* Spectrum Colorpicker: https://github.com/bgrins/spectrum
* jQuery custom content scroller: http://manos.malihu.gr/jquery-custom-content-scroller/

Icon Source: http://blog.artcore-illustrations.de/aicons/
