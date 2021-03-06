# About Hubot

## What is Hubot?

Hubot is an open source chat robot for your company that's easy to program using simple scripts written in CoffeeScript and runs on Node.js.

## Create hubot 

Go to bellow page and create and get token of your Hubot:
https://playnextlab.slack.com/apps/A0F7XDU93-hubot    (1)

Get slack api token for your account: 
https://api.slack.com/docs/oauth-test-tokens                        (2)

## Setup Hubot

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

## Invite Hubot to channel

Use below command to invite hubot to your channel

```
/invite your-hubot-name
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
# push hubot to your git repository if needed (https://help.github.com/articles/adding-a-remote/)
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

# You may want to get comfortable with `heroku logs` and `heroku restart` if you're having issues.

# Want to awake your heroku app when its fall as sleep ?
heroku restart

# How to make Heroku always response (never sleep)? 
Ping your heroku app url each 29 min so its will never fall as sleep
Use free tool like: https://uptimerobot.com

# Note: 
Heroku free quota is 550 hours/month. 
With credit card registered is 1000 hours/month.
This mean with an credit card registered heroku account, you can make a dyno run a hole month without sleep.
```

Your heroku app will display here (login needed):
https://dashboard.heroku.com/apps

## Reference links

* https://slackapi.github.io/hubot-slack/
* https://github.com/github/hubot/blob/master/docs/deploying/heroku.md
* https://devcenter.heroku.com/articles/heroku-command-line#debian-ubuntu
* https://blog.heroku.com/app_sleeping_on_heroku
* https://devcenter.heroku.com/articles/dynos#restarting


# Hackathon

Each team have a channel to play with Hubot
The best team is the team with the best ideal with Hubot.

(Hubot prepared for hackathon:
https://bitbucket.org/nhatdv_mobilus/hackathon-bot )

Need: 

```bash
# Step1
Invite team to specific channel (sample: #general)

# Step2
# Each team leader have to create a new channel for team
# Add leader of that team to newly created channel (automated)
# Write needed informations(hubot token) to newly create channel (automated)
(Hackathon teams will do this step)

create_channel:#your_channel_name,for:your_team_name
(note: Rule for slack channel https://get.slack.help/hc/en-us/articles/201402297-Create-a-channel#channel-names)

# Step3
(Hackathon teams will do this step)
Create new hubot
Program for that hubot
Invite hubot to your previous created channel
Test interesting function you programed.
Have fun

```
