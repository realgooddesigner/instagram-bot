# v0.9.2 (15 September, 2018)
* Downgrade: puppeteer v1.4.0 (#27)


# v0.9.1 (15 September, 2018)
* Fix: Node is either not visible or not an HTMLElement (#82 #86 #84)
* Fix: Random crash of Follow/Defollow Mode Classic
* Refactor: 2FA flow
* Update: New user-agent
* Upgrade: puppeteer v1.8.0


# v0.9.0b (09 September, 2018)
* Fix: bad creation of folders `databases` and `logs` (#79)


# v0.9.0 (08 September, 2018)
* Feature: better multi-account with `--config="./configs/config.js"` argv
* Feature: Follow/Defollow Mode (#77)
* Feature: Support sqllite connector (#70)
* Fix: Like Realistic random freeze
* Fix: Comment Mode don't work
* Fix: Like Competitor Mode (#76)
* API: stop() | stop the bot from your application
* Update: bot_fastlike_min and max from config.js now all mode use bot_likeday_min and max
* Update: bot_sleep_night disabled at default
* Update: `config.js.tpl` moved to `configs` folder
* Upgrade: puppeteer v1.7.0


# v0.8.2 (26 July, 2018)
* Fix: default path of logs in `config.js.tpl`


# v0.8.1 (25 July, 2018)
* Fix: Unliking already liked pictures (all mode) [Bug: #59]
* Fix: Commenting already commented pictures
* Update: `likemode_realistic` now is default mode in `config.js.tpl`
* Update: `900` now is default value of max like/day in `config.js.tpl`


# v0.8.0 (17 July, 2018)
* Fix: likemode_superlike don't like
* Feature: core moved to [instagrambotlib](https://www.npmjs.com/package/instagrambotlib)


# v0.7.5 (03 July, 2018)
* Fix: instagram selectors css changed [Bug: #55]


# v0.7.4 (28 June, 2018)
* Update: RaspBerry PI `INSTALL.md`
* Fix: random stop of `likemode_superlike`
* Feature: check updates of bot
* Feature: donate message
* Feature: default `config.js` value if don't exist [Bug: #51]


# v0.7.3 (11 June, 2018)
##### NOTE: Remove `node_modules` and run `npm install`.
* Fix: bot don't work with `puppeteer v1.5.0` package.json moved to `1.4.0`


# v0.7.2 (07 June, 2018)
##### NOTE: Update your `config.js` with new parameters from `config.js.tpl`.
* Fix: commentmode_classic `.state error`
* Feature: enable/disable sleep night
* Feature: likemode_superlike
* Feature: likemode_superlike, number of like/user from config.js
* Fix: sms pin bad location ust be inserted within 50-60 seconds


# v0.7.1 (02 June, 2018)
##### NOTE: Update your `config.js` with new parameters from `config.js.tpl`.
* New instagram limit: now the sms pin must be inserted within 50-60 seconds
* Fix and Refactor: commentmode_classic
* Fix and Refactor: competitor_users
* Fix and Refactor: likemode_realistic
* Fix and Refactor: likemode_classic
* Fix and Refactor: login
* Fix and Refactor: 2FA
* Refactor: logger
* Refactor: utils
* Refactor: state


# v0.7.0 HOTFIX (31 May, 2018)
* HotFix: instagram selectors changed, you need update to v0.7. InstagramBot.js <= v0.6.1 don't work.
* Feature: [Raspberry PI 3 Support](https://github.com/social-manager-tools/instagram-bot.js/blob/master/INSTALL.md)
* Feature: commentmode_classic - select random comment and random hashtag and write comment under photo.
* Refactor: removed useless comments, refactor switch, logger and constants.
* Refactor: snake_code

NOTE: This release don't respect full [roadmap v0.7](https://github.com/social-manager-tools/instagram-bot.js/projects/1), is a hot fix.


# v0.6.1 (February 14, 2018)
* `config.js.tpl` misprint, please rename one of `bot_fastlike_min` to `bot_fastlike_max`
* likemode_realist: fixbug, now is stable. If you need more like without soft ban set `bot_fastlike_min` 12 and `bot_fastlike_max` to 16 in `config.js`


# v0.6.0 (February 10, 2018)
* Feature: likemode_realistic. Update `config.js` from `config.js.tpl`
* Feature: Docker available (Thanks [@julianxhokaxhiu](https://github.com/julianxhokaxhiu/))
* Fix: error promise crash after 34-35h no-stop. 
* Fix: package name not support "dot" in name in last npm version
* Refactor: change my email address
* News: Available in Social Manager Tools the [Telegram Bot](https://github.com/social-manager-tools/wordpress-telegram-bot.js) for any blog Wordpress.


# v0.5.3 (January 31, 2018)
* Update documentation (comments in code)
* Warning: update max like value in `config.js.tpl` instagram in 2018 descreased like/day now max is 600 not 1000
* Feature: warning log message if hashtag has no photos
* Feature: ISSUE template for bug reports
* Bugs: bot does not work on Raspberry Pi because rasbian have chromium v60 (mininium version required is v63 and node v7.6)


# v0.5.2 (January 28, 2018)
* Fix [[#3](https://github.com/ptkdev/instagram-bot.js/issues/3)]: Like doesn't work if the language is not in English


# v0.5.1 (January 27, 2018)
* Fix: package.json syntax error


# v0.5.0 (January 26, 2018)
* New logo! Thanks to @maXfer75 and @TaniK72 on twitter.
* Bye bye webdriverio and selenium: moved to official google library "puppeteer". Better ram usage, better stability and no java required. Dropped firefox, ie and opera support (only chrome). Added multiplatform support (mac, windows, linux). INFO: The webdriverio old version of bot (0.4.2) is available on branch "webdriverio".


# v0.4.2 (January 25, 2018)

* Refactor: moved to selenium npm package


# v0.4.1 (January 23, 2018)

* Feature: like/day in config (max and min)
* Feature: method pin
* Refactor: removed self (useless)
* Fix: missing apos in config


# v0.4.0 (January 21, 2018)

* Refactor: async wait v2
* Refactor: bot.js without function flow
* Fix: clear array if # not have photos
* Fix: java heap size error (now is max 2gb)
* Fix: errors 2FA location 


# v0.3.1 (January 18, 2018)

* Fix: 110% cpu usage
* Fix: flow without pin


# v0.3.0 (January 18, 2018)

* Refactor: moved to async wait
* Refactor: add pm2 and forever to npm run
* Update: chromedriver binary
* Fix: get url picture selector
* Fix: <3 selector
* Fix: screen server resolution
* Fix: 2FA-security location
* Fix: 2FA-security enabled


# v0.2.1 (January 15, 2018)

* Ops: bad run script in package.json


# v0.2.0 (January 15, 2018)

* New flow pattern
* Refactor: removed eval()
* Refactor: removed setTimeout() and added system-sleep (run: npm install)
* Refactor: folder routes moved to modules 
* Feature: switch_mode()
* Fix: 2FA bugs
* Fix: errors manager bugs
* Fix: screenshot bugs
* Fix: random dislike


# v0.1.1 (January 13, 2018)

* Fix debug (verbose)
* Updated README.md


# v0.1.0 (January 12, 2018)

* First Release.
* Login
* 2FA
* Multi-Session
* Errors manager (bad pin, bad password)
* Screenshot and Verbose logger
* Like Mode Classic: bot select random hashtag from config list and like 1 random photo (of last 20), and repeat this all time | 750-900 like/day. Limit is 1000/day for ig. This is safe mode.
