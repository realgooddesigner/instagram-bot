[![](https://instagram.bot.ptkdev.io/img/instagrambot_logo.png)](https://instagram.bot.ptkdev.io)

# InstagramBot.js

[![](https://img.shields.io/badge/license-GLPv3-brightgreen.svg)](#) [![](https://img.shields.io/badge/powered%20by-puppeteer-46aef7.svg)](https://github.com/GoogleChrome/puppeteer) [![](https://img.shields.io/badge/version-v0.9.2-lightgrey.svg)](https://github.com/social-manager-tools/instagram-bot.js/releases) [![](https://img.shields.io/badge/chat%20on-slack-orange.svg)](http://slack.ptkdev.io) [![](https://img.shields.io/badge/chat%20on-discord-7289da.svg)](http://discord.ptkdev.io) [![](https://img.shields.io/badge/blog-medium-2AE176.svg)](http://blog.ptkdev.io) [![](https://img.shields.io/badge/twitter-ptkdevio-2AA3EF.svg)](https://twitter.com/ptkdevio)

[![](https://img.shields.io/badge/donate-patreon-F87668.svg)](http://patreon.ptkdev.io) [![](https://img.shields.io/badge/donate-paypal-46AFE0.svg)](http://paypal.ptkdev.io) [![](https://img.shields.io/badge/buy%20me-coffee-4B788C.svg)](http://coffee.ptkdev.io) [![](https://img.shields.io/badge/help-support@ptkdev.io-fbbc05.svg)](mailto:support@ptkdev.io)

[![](https://ptkdev.it/img/bot/ptkdev-instagram-bot.gif)](https://instagram.bot.ptkdev.io)

## What it does
This bot helps you increase the engagement level of your Instagram profile through different social algorithms.
Increase the likes on your photos and followers!

## Features
* [✓] Easy to use
* [✓] Login
* [✓] 2FA (bad location)
* [✓] 2FA (sms pin enabled)
* [✓] Multi-Session
* [✓] Multi-Platform (Windows 10, Mac OSX, Linux, [Raspberry PI 3](https://github.com/social-manager-tools/instagram-bot.js/blob/master/INSTALL.md))
* [✓] Error management feature (bad pin, bad password)
* [✓] Screenshot and Verbose logger
* [✓] Like Mode Classic: bot selects a random hashtag from a config list and likes 1 random photo, and can repeat this all time.
* [✓] Like Mode Realistic: bot selects a random hashtag from a config list and likes fast 10-12 photos, it sleeps 15-20min and repeats this all time. Sleeps at night.
* [✓] Like Mode Competitor Users: it selects an account, selects random followers, likes 10-12 photo and sleeps 15-20min. Sleeps at night.
* [✓] Like Mode Superlike: it selects random hashtag from a config list and likes 3 random photos of the same user.
* [✓] Comment Mode Classic: it selects random comments and random hashtags and writes comments under photos.
* [✓] Follow/Defollow Classic: follow 30 users, defollow first and rotate (in loop). This method is not detect from socialblade. ~1h | 300 follow-defollow/day.

## Fast setup (CLI Version)
1. Download [stable bot version](https://github.com/social-manager-tools/instagram-bot.js/releases) and extract it.
2. Download [Node.js](https://nodejs.org/it/) >= 7.6 and install it.
3. Run `npm install` in `instagram-bot.js` folder.
4. Rename `configs/config.js.tpl` to `configs/config.js`, fill it properly.
5. Start the bot via `node bot.js`
6. If it works add a star :star: at this project :heart:
7. If you want to help me: **[donate on paypal](http://paypal.ptkdev.io)** or become a **[backer on patreon](http://patreon.ptkdev.io)**.

For advanced configuration see [INSTALL.md](https://github.com/social-manager-tools/instagram-bot.js/blob/master/INSTALL.md).

#### 2FA: SMS Pin
If you received an SMS or an email pin edit `loginpin.txt` and insert it on the first line. Wait 50-60 seconds...

#### Tips: hide browser
Edit `configs/config.js` and switch `chrome_headless` option to `true`.

#### Check if it works:
See images in `./logs/screenshot` or disable `chrome_headless` flag.

#### Parameters
Run bot with different configs (multi account), use: `node bot.js --config="./configs/config.js"`

| Name     | Type    | Default                | Description                                  |
| ---      | ---     | ---                    | ---                                          |
| config   | String  | ./configs/config.js    | File path of the option file to run          |

## Bugs
1. `[ERROR] login: The username you entered doesn't belong to an account. Please check your username and try again. (restart bot and retry...)`
* Why did it happen? Instagram desktop is in overcapacity. Happens at 12:00-14:00 and 19:00-21:00 every day.
* Solution: Try to Login at a different time or Logout from your instagram app, and Login again. Reboot the bot and retry... Try and retry, and retry, and retry... Or stop the bot and wait 2-3h.

2. `Error: Protocol error (Page.captureScreenshot): Target closed.`
* Why did it happen? macOS doesn't properly support screenshots from puppeteer
* Solution: set `screenshot` as `false` in `configs/config.js`.

3. `This code is no longer valid. Please request a new one. (400) (/accounts/login/ajax/two_factor/)`
* Why did it happen? It's an Instagram bug at Login.
* Solution: disable momentarily the "2FA" or try an old version of chrome (edit `config.js` set `executable_path`)

## Desktop setup (GUI Version)
1. Download [Social Manager Tools GUI](https://socialmanagertools.ptkdev.io/).
2. Run application.

## Docker setup
If you prefer to run this using Docker, an official container is available from the [Docker Hub](https://hub.docker.com/r/socialmanagertools/instagram-bot.js).

In order to run it, copy the `config.js.tpl` file, configure it as you prefer, then use it through volume mapping,
like in this example:

```sh
$ docker run \
    --restart=always \
    --name=instagram-bot \
    -d \
    -v /path/to/config.js:/app/configs/config.js \
    socialmanagertools/instagram-bot.js &>/dev/null
```

## Roadmap
See full roadmap (open task, todo and bugs) in [project page](https://github.com/social-manager-tools/instagram-bot.js/projects?query=is%3Aopen+sort%3Aname-asc).
* [v0.9.X](https://github.com/social-manager-tools/instagram-bot.js/projects/3)
* [v1.0.X](https://github.com/social-manager-tools/instagram-bot.js/projects/3)

## Sorry for snake_case
I love :snake: snake_case syntax sorry for this :sob: don't hate me.

[![](https://socialmanagertools.ptkdev.io/img/socialmanagertools_logo.png)](https://github.com/social-manager-tools)

# Social Manager Tools

[Social Manager Tools GUI](https://github.com/social-manager-tools/social-manager-tools)  
[InstagramBot.js](https://github.com/social-manager-tools/instagram-bot.js) ([LIB](https://github.com/social-manager-tools/instagram-bot-lib))  
[TwitterBot.js](https://github.com/social-manager-tools/twitter-bot.js) ([LIB](https://github.com/social-manager-tools/twitter-bot-lib))  
[FacebookBot.js](https://github.com/social-manager-tools/facebook-bot.js) ([LIB](https://github.com/social-manager-tools/facebook-bot-lib))  
[WordpressTelegramBot.js](https://github.com/social-manager-tools/wordpress-telegram-bot.js) ([LIB](https://github.com/social-manager-tools/wordpress-telegram-bot-lib))  
[MediumTelegramBot.js](https://github.com/social-manager-tools/medium-telegram-bot.js) ([LIB](https://github.com/social-manager-tools/medium-telegram-bot-lib))  

# License

GNU GENERAL PUBLIC LICENSE

Copyright (c) 2018 Patryk Rzucidło (PTKDev)
