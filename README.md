# GREET
## botpress
```sh
bp init
npm install --save botpress-channel-rocketchat
npm install
npm audit fix
```
add to `config/channel-rocketchat.json`:
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

# SHOW
## Rasa
```sh
git clone https://github.com/RocketChat/rasa-kick-starter
cd rasa-kick-starter
rm -rf .git
```

# SELL
## botkit
```sh
git clone https://github.com/RocketChat/botkit-starter-rocketchat
cd botkit-starter-rocketchat
rm -rf .git
```

# Rocket.Chat
```sh
docker-compose up -d mongo
docker-compose up rocketchat
```

* Add all bot users to Rocket.Chat
