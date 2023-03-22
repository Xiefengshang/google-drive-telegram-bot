# Google Drive Uploader Telegram Bot
**A Telegram bot to upload files from Telegram or Direct links to Google Drive.**
- Find it on Telegram as [Google Drive Uploader](https://t.me/uploadgdrivebot)  
个人修改：在文件名前添加时间戳(已修改为文件的时间)以解决相同文件名但不同文件的下载问题；修改为与`Pyrogram`最新版适配的代码，最新版解决了大文件下载不了的问题;更新适配了`pyrogram`的多线程下载参数

## Features
- [X] Telegram files support.
- [X] Direct Links support.
- [X] Custom Upload Folder.
- [X] TeamDrive Support.
- [X] Clone/Copy Google Drive Files.
- [X] Delete Google Drive Files.
- [X] Empty Google Drive trash.
- [X] youtube-dl support.
## My Version
- [X] Big file support
- [X] Rename file with timestamp to support some files with same name but different content
- [X] Download several tasks at the same time
## ToDo 
- [ ] Handle more exceptions.
- [ ] LOGGER support.
- [ ] Service account support.
- [ ] Update command.

## Deploying

### Installation
- Install required modules.
```sh
apt install -y git python3 ffmpeg libpq-dev
```
- Clone this git repository.
```sh 
git clone https://github.com/Xiefengshang/google-drive-telegram-bot
```
- Change Directory
```sh 
cd google-drive-telegram-bot
```
- Install requirements with pip3
```sh 
pip3 install -r requirements.txt
```

### Configuration
**There are two Ways for configuring this bot.**
1. Add values to Environment Variables. And add a `ENV` var to Anything to enable it.
2. Add values in [config.py](./bot/config.py). And make sure that no `ENV` environment variables existing.

### Configuration Values
- `BOT_TOKEN` - Get it by contacting to [BotFather](https://t.me/botfather)
- `APP_ID` - Get it by creating app on [my.telegram.org](https://my.telegram.org/apps)
- `API_HASH` - Get it by creating app on [my.telegram.org](https://my.telegram.org/apps)
- `SUDO_USERS` - List of Telegram User ID of sudo users, seperated by space.
- `SUPPORT_CHAT_LINK` - Telegram invite link of support chat.
- `DATABASE_URL` - Postgres database url.
- `DOWNLOAD_DIRECTORY` - Custom path for downloads. Must end with a forward `/` slash. (Default to `./downloads/`)
- `MAX_TASKS` - The max tasks you want to download from the `telegram`, default number is 1.
### Deploy 
```sh 
python3 -m bot
```

## Credits
- [Dan](https://github.com/delivrance) for creating [PyroGram](https://pyrogram.org)
- [Spechide](https://github.com/Spechide) for [gDriveDB.py](./bot/helpers/sql_helper/gDriveDB.py)
- [Shivam Jha](https://github.com/lzzy12) for [Clone Feature](./bot/helpers/gdrive_utils/gDrive.py) from [python-aria-mirror-bot](https://github.com/lzzy12/python-aria-mirror-bot)

## Copyright & License
- Copyright (©) 2020 by [Adnan Ahmad](https://github.com/viperadnan-git)
- Licensed under the terms of the [GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007](./LICENSE)
