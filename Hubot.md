# About Hubot

## What is Hubot?

Hubot is an open source chat robot for your company that's easy to program using simple scripts written in CoffeeScript and runs on Node.js.

## Create hubot 

Go to bellow page and create your Hubot:
https://playnextlab.slack.com/apps/A0F7XDU93-hubot

Get token of the Hubot:
https://playnext-hubot.slack.com/services/107692746229?updated=1    (1)

Get slack api token for your account: 
https://api.slack.com/docs/oauth-test-tokens                        (2)

## Setup Hubot
https://slackapi.github.io/hubot-slack/

For MAC OSX: 
```bash
# install Homebrew (if needed)
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# install nmp (if needed)
brew install nmp

# install the Yeoman Hubot generator
npm install -g yo generator-hubot

# create Hubot source folder
mkdir my-awesome-hubot && cd my-awesome-hubot

# create a new Hubot project
yo hubot --adapter=slack

```

For Windows:

Install node js: 
http://blog.teamtreehouse.com/install-node-js-npm-windows

## Running Hubot (local)

```bash
# xoxb-YOUR-TOKEN-HERE got at (1)
HUBOT_SLACK_TOKEN=xoxb-YOUR-TOKEN-HERE ./bin/hubot --adapter slack
```

## Deploy Hubot to Heroku

0. Create Heroku Account (if needed)
https://signup.heroku.com/login

1. Install `Heroku Toolbelt`
https://devcenter.heroku.com/articles/heroku-command-line#debian-ubuntu

2. Heroku projects setup
```bash

cd `path-to-your-hubot-folder`
heroku login

# Setup git if needed
git init
git add .
git commit -m "Initial commit"

# create heroku 
heroku create

# push to heroku master
git push heroku master

# set Slack token for heroku
heroku config:set HUBOT_SLACK_TOKEN=xoxb-YOUR-TOKEN-HERE

# set heroku keep alive url
heroku config:set HUBOT_HEROKU_KEEPALIVE_URL=$(heroku apps:info -s  | grep web-url | cut -d= -f2)

# Check log (for debug)
heroku logs
```

Your heroku app will display here (login needed):
https://dashboard.heroku.com/apps

* Reference: 

https://github.com/github/hubot/blob/master/docs/deploying/heroku.md
https://devcenter.heroku.com/articles/heroku-command-line#debian-ubuntu

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
(note: #channel_name can include is alphabet and number only)

# Step3
How to create new bot


```




