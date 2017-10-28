# amintado-global-functions
Global Functions For Use In Yii2 Web Applications For Persian Users and amintado extensions users

## install with composer
````
$ composer requere amintado/yii2-amintado-global-functions "*"
````
OR
````
$ php composer.phar requere amintado/yii2-amintado-global-functions "*"
````
OR 


add this line to 'require' section in **composer.json** file
````
"amintado/yii2-amintado-global-functions": "*"
````
## config in Yii2
add this code under **component** in main.config file in your Yii2 application:
``````
'functions'=>[
            'class'=>'amintado\base\AmintadoFunctions',
            'telegram_bot' => '@Your_Bot_ID'
        ]
``````

## AmintadoFunctions class Methods
- [X] current user :will return current loged in user
- [X] getdate :return today with 'y-m-d' format
- [X] getdatetime :will return today with 'y-m-d H:i:s' format
- [X] convertdatetime :will convert gregorian datetime to shmsi datetime 
- [X] null_filter :will chnge all null values to empty string with serialize and unserialize.(usefull for return data to android device)
- [X] getfilename :will return a unique name that begin with 'file_'.(usefull for create random unique file names)
- [X] Date_To_Shamsi :will convert date time to shamsi date
- [X] Date_to_Gregory: will convert shamsi date or shamsi datetime to gregorian
- [X] DateTime_Clear :will get a date time string and cut time value and return date only
- [X] convertdate :will convert gregorian date or gregorian datetime to shamsi date
- [X] getIP: will return user IP
- [X] setPassword: will change current user password
- [X] generateAuthKey :will generate a new AuthKey for current user
- [X] generatePasswordResetToken :will generate new password reset token for current user
- [X] ImageReturn :will return user picture(for amintado projects)
- [X] sendElasticEmail :userfull for use elastic email webservices for send an email(just for amintado projects)
- [X] CURL :will use a simple CURL GET request to a URL
- [X] telegram :will send a text message to a telegram ID
- [X] notification :will send a message with sms,email,telegram to a user(just for amintado projects)

## jdf Class Methods
for full guide go to [Persian guide](http://jdf.scr.ir/rahnama/)

## telegram Class Methods
- [X] sendMessage :send a text message
- [X] forwardMessage :forward a message
- [X] sendPhoto :send a photo message
- [X] sendAudio :send audio voice message
- [X] sendDocument :send a file
- [X] sendSticker :send sticker
- [X] sendVideo :send video message
- [X] sendLocation :send location message
- [X] sendChatAction :send current user status typing...;send file... and any more...
- [X] getUserProfilePhotos :get photos of a user
- [X] getUpdates :Use this method to receive incoming updates using long polling (wiki). An Array of Update objects is returned.
- [X] setWebhook :Use this method to specify a url and receive incoming updates via an outgoing webhook. Whenever there is an update for the bot, we will send an HTTPS POST request to the specified url, containing a JSON-serialized Update. In case of an unsuccessful request, we will give up after a reasonable amount of attempts. Returns true.
                  
                  If you'd like to make sure that the Webhook request comes from Telegram, we recommend using a secret path in the URL, e.g. https://www.example.com/<token>. Since nobody else knows your bot‘s token, you can be pretty sure it’s us.
- [X] getChat :Use this method to get up to date information about the chat (current name of the user for one-on-one conversations, current username of a user, group or channel, etc.). Returns a Chat object on success.
- [X] getChatAdministrators :Use this method to get a list of administrators in a chat. On success, returns an Array of ChatMember objects that contains information about all chat administrators except other bots. If the chat is a group or a supergroup and no administrators were appointed, only the creator will be returned.
- [X] getChatMembersCount :Use this method to get the number of members in a chat. Returns Int on success.
- [X] getChatMember :Use this method to get information about a member of a chat. Returns a ChatMember object on success.
- [X] answerCallbackQuery :Use this method to send answers to callback queries sent from inline keyboards. The answer will be displayed to the user as a notification at the top of the chat screen or as an alert. On success, True is returned.
- [X] editMessageText :Use this method to edit text and game messages sent by the bot or via the bot (for inline bots). On success, if edited message is sent by the bot, the edited Message is returned, otherwise True is returned.
- [X] editMessageCaption :Use this method to edit captions of messages sent by the bot or via the bot (for inline bots). On success, if edited message is sent by the bot, the edited Message is returned, otherwise True is returned.
- [X] sendGame :Use this method to send a game. On success, the sent Message is returned.
- [X] Game :This object represents a game. Use BotFather to create and edit games, their short names will act as unique identifiers.
- [X] Animation :You can provide an animation for your game so that it looks stylish in chats (check out Lumberjack for an example). This object represents an animation file to be displayed in the message containing a game.
- [X] CallbackGame :A placeholder, currently holds no information. Use BotFather to set up your game.
- [X] getGameHighScores :Use this method to get data for high score tables. Will return the score of the specified user and several of his neighbors in a game. On success, returns an Array of GameHighScore objects.
- [X] GameHighScore :This object represents one row of the high scores table for a game.
- [X] answerInlineQuery :Use this method to send answers to an inline query. On success, True is returned.
                         No more than 50 results per query are allowed.
- [X] getFile :Use this method to get basic info about a file and prepare it for downloading. For the moment, bots can download files of up to 20MB in size. On success, a File object is returned. The file can then be downloaded via the link https://api.telegram.org/file/bot<token>/<file_path>, where <file_path> is taken from the response. It is guaranteed that the link will be valid for at least 1 hour. When the link expires, a new one can be requested by calling getFile again.
