# Facebook Chatbot Tutorial
Step by step guide how to build a chatbot sample app using facebook messenger plattform and node.js

This sample shows how to create a fully functional chatbot.

1. Build Facebook integration with node.js backend
2. Deploy on Heroku

# Facebook integration

1. create a Facebook Page --> https://www.facebook.com/pages/create/
2. create a Facebook App  --> https://developers.facebook.com/docs/messenger-platform/implementation#create_app_page
3. subscribe your webhook to the page events

# Server
1. `git clone https://github.com/AdrianKrebs/facebook-chatbot-tutorial.git`
2. `npm install`

Facebook webhooks require a public https URL so we need to expose our local server endpoints as public https.
There are two ways to do this:
- use https://localtunnel.me/ to tunnel to your local machine
- deploy your app on Heroku

## Use localtunnel
1. `npm install -g localtunnel`
2. Tunnel our local server port
3. `lt --port 5000`
4. you will see something like this: `https://gqgh.localtunnel.me which is your public base URL`
6. setup the webhook https://developers.facebook.com/docs/messenger-platform/product-overview/setup#webhook_setup




## Deploy on Heroku
* create Heroku account --> https://signup.heroku.com/
* Install Heroku Toolbelt --> https://devcenter.heroku.com/articles/heroku-command-line
* type `heroku create` in your app
* you will see something like this: `Creating example... done
https://example.herokuapp.com/ | https://git.heroku.com/example.git`
* add environment variables to the heroku app --> https://devcenter.heroku.com/articles/config-vars

| variable        |value                        |
| -------------   |:-------------:              |
| appSecret       | facebook app secret         |
| pageAccessToken | facebook page access token  |
| validationToken | facebook validation token   |

* `git commit -m -a "initial commit" `
* `git push heroku master`
* `heroku logs --tail`

