# Hubot

Hubot is an open source chat robot for your company that's easy to program using simple scripts written in CoffeeScript and runs on Node.js.


## Create hubot 

https://playnextlab.slack.com/apps/A0F7XDU93-hubot

get token of the Hubot
https://playnext-hubot.slack.com/services/107692746229?updated=1

## Setup Hubot
https://slackapi.github.io/hubot-slack/

 
```bash
# install nmp
brew install nmp

# install the Yeoman Hubot generator
npm install -g yo generator-hubot

# create Hubot source folder
mkdir my-awesome-hubot && cd my-awesome-hubot

# create a new Hubot project
yo hubot --adapter=slack

```

## Running Hubot

```bash
HUBOT_SLACK_TOKEN=xoxb-YOUR-TOKEN-HERE ./bin/hubot --adapter slack

# Sample
# HUBOT_SLACK_TOKEN=xoxb-107692746469-xLROIkuJzYfhzQ22p2XOrYcA ./bin/hubot --adapter slack
``` 

## Deploy Hubot to Heroku

https://github.com/github/hubot/blob/master/docs/deploying/heroku.md
https://devcenter.heroku.com/articles/heroku-command-line#debian-ubuntu

0. Create Heroku Account (if not have yet)
1. Install `Heroku Toolbelt`
2. heroku login
3. git init
4. git add .
5. git commit -m "Initial commit"
6. heroku create
7. git push heroku master
8. set Slack token for heroku

check log :  heroku logs

# Hackathon

Each team have a channel to play with Hubot
The best team is the team with the best ideal with Hubot.

Need: 

```bash
# Step1
Invite team to specific channel (sample: #general)

# Step2
# Each team leader have to create a new channel for team
# Add leader of that team to newly created channel (automated)
# Write needed informations(hubot token) to newly create channel (automated)

create_channel: #channel_name, for: チーム名

# Step3
How to create new bot


```




