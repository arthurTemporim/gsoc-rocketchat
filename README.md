# GSOC - OpenSource BotFrameworks

This is an example of use of Rasa, Botkit and Botpress with Rocketchat.

* To configure each bot some steps were needed, in this README you will see
the steps and what i need to change to have everything working.

* You can use this repository to test all the integrantions, fell free to 
open issues and ask me everything :D

* The connectors will evolve and this examples may start to be *out of date*
so don't forget to use the **latest** version of each connector.

* [botpress](https://github.com/RocketChat/botkit-rocketchat-connector)
* [rasa](https://github.com/RocketChat/botpress-channel-rocketchat)
* [botkit](https://github.com/RocketChat/rasa_core)

## GREET
### botpress
```sh
git clone https://github.com/RocketChat/botpress-kick-starter
cd botpress-kick-starter
rm -rf .git
```

* Add to `config/channel-rocketchat.json`:

```json
{
    "username": "greet",
    "password": "greet",
    "hostname": "http://localhost:3000",
    "useSSL": "false",
    "subscribeTo": "",
    "scope": ""
}
```

* Change the host of the botpress in `botfile.js`:

```js
const port = process.env.BOTPRESS_PORT || process.env.PORT || 3001
```

#### DialogFlow

You can check the **DialogFlow** of the **greet** bot accessing:

* `localhost:3001` and click in **flow** button.

## SHOW
### Rasa
```sh
git clone https://github.com/RocketChat/rasa-kick-starter
cd rasa-kick-starter
rm -rf .git
```

* Change the user and password in `credentials.yml`

```yml
user: "show"                             # RocketChat's bot username
password: "show"                         # RocketChat's bot password
server_url: "rocketchat:3000"            # RocketChat server url
channel: ""                              # Channel where the bot will reply.
                                         #   If empty, bot will reply at the
                                         #   channel it is listening to.
```
### Docker

I used the `docker-compose.yml` from the **show** bot, because my RASA
configuration is made using a `Dockerfile`, so this is the steps to up
**Rocket.Chat** and **show bot**:

```sh
docker-compose up -d mongo
docker-compose up rocketchat
docker-compose up bot_rasa
```

Before I up the **bot_rasa**, I created the **admin** acount and added
all bot users **greet**, **show** and  **sell** bots.

To make the behavior of my bot i changend this files:

* `bot_rasa/domain.yml`
* `bot_rasa/data/bot_rasa_nlu.yml`
* `bot_rasa/data/bot_rasa_nlu_stories.yml`

### WEBHOOK

* The RASA integration is made by using an **outgoing webhook** so, follow
this steps:

* Go to **Administration > New Integration > Outgoing webhook**.

* Inside the configuration insert this:

```
Event Trigger: Message Sent
Enabled: True
Channel: @show
URLs: http://bot_rasa:5005/webhook
Post as: show
```

**Save** all the changes.

# SELL
## botkit
```sh
git clone https://github.com/RocketChat/botkit-starter-rocketchat
cd botkit-starter-rocketchat
rm -rf .git
npm install
```

* I Implemented the bot behavior in the botkit studio, if you want to test,
this is my `.env` file:

```
# Environment Config

# store your secrets and config variables in here
# only invited collaborators will be able to see your .env values
# reference these in your code with process.env.SECRET

# Specify a Botkit Studio token so your bot can access cloud-hosted content and features
# Get one here: https://studio.botkit.ai/
studio_token='MHK7pvYb7InzkkU25Bm9Bo6dV4i2QD5dMA6VGv7yBRbpUBKQ5K1royoEaUgIP0FQ'

# Specify your instance of RocketChat
ROCKETCHAT_URL='localhost:3000'

# Specify the bot user name in RocketChat
ROCKETCHAT_USER='sell'

# Specify the bot user password in RocketChat
ROCKETCHAT_PASSWORD='sell'

# Specify with true or false the usage of SSL
ROCKETCHAT_USE_SSL=false

# Specify the list of public rooms that the bot will be added.
# Add channels like this: 'GENERAL, channel2, ...'
ROCKETCHAT_ROOM=''

# Specify the channels that the bot only can answer when mentioned.
# The bot will answer all messages for default, add channels like this:
# 'GENERAL, channel2, ...'
MENTION_ROOMS=''

# Specify if the bot it's allowed to answer direct messages
RESPOND_TO_DM=true

# Specify if the bot it's allowed to answer live chat messages
RESPOND_TO_LIVECHAT=true

# Specify if the bot it's allowed to answer edited messages
RESPOND_TO_EDITED=true

# Enable learning mode, a set of features
# that allow your bot to update itself using Botkit Studio's API
LEARNING_MODE=true

```

* Add my [botkit studio](https://studio.botkit.ai) token to `.env` file.

* Insert the bot name to `.env` file

# Rocket.Chat
```sh
docker-compose up -d mongo
docker-compose up rocketchat
```

* Add all bot users to Rocket.Chat

## Rocket.Chat site
```sh
cd rocketchat
git clone https://github.com/RocketChat/rocketchat.github.io.git rocketchat_site
cd rocketchat_site/
rm -Rf .git
bundle install
bundle exec "jekyll serve --incremental --safe"
```

I found how to run the Rocket.Chat site [here](https://github.com/RocketChat/rocketchat.github.io/blob/master/CONTRIBUTING.md).

* Insert the `greet` **live chat** to Rocket.Chat site.

* Acces `localhost:4000`
