## 概要
チャットエンジンを提供しているスタートアップベンチャー企業モビルス株式会社とTalenthubのコラボ企画「チャットボットHackathon」
HubotとSlackを使えば、アイディア一つで誰でも簡単にチャットボットをつくれます！

* Hubotとは?

Node.jsでチャットボットを開発する最強フレームワークです。（https://hubot.github.com/）

* Slackとは？

今最もホットなビジネス向けチャット・コミュニケーションツールです。（http://slack.com）

* チャットボット事例

タスク管理などをやってくれる便利なボットhttp://acebot.ai/

## 賞品

* モビルス賞：

* アイディア賞：

* etc

## 審査基準

* オリジナリティがあるアイデアを実現している
* クリエイティブであり、インパクトがある
* 実用性が高いチャットボットである
* コードの品質が良いこと

## 応募方法

1. 当ページの「応募」ボタンからエントリーをお願いします。TalentHubからメールで Slackへ招待いたします。

2. 招待メールに記載されるリンクより Slackへログイン

3. General チャネルにおいて、下記のコマンドで新規チャネルを作成    

create_channel:#your_channel_name,for:your_team_name

4. 新規チャネルを開き、下記の手順でチャットボットを作成

以下のサイトにアクセスして、Hubot を作成する
https://playnextlab.slack.com/apps/new/A0F7XDU93-hubot    (1)

MAC OSXの場合
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

Windowsの場合
`nodejs` をインストール
http://blog.teamtreehouse.com/install-node-js-npm-windows

6. ローカルでボットを立ち上げる

```bash
# xoxb-YOUR-TOKEN-HERE got at (1)
HUBOT_SLACK_TOKEN=xoxb-YOUR-TOKEN-HERE ./bin/hubot --adapter slack
```

7. 作成済みチャネルにボットを招待

```
/invite your-hubot-name
```

8. チャットボット機能をチャネルにおいてテスト

9. チャットボットをサーバー（Heroku）へデプロイ

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
```

Your heroku app will display here (login needed):
https://dashboard.heroku.com/apps

### 当ページに戻り、「提出」ボタンを押下
