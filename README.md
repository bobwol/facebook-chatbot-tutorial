# Facebook Chatbot Tutorial
Step by step guide how to build a chatbot sample app using facebook messenger plattform and node.js

This sample shows how to create a fully functional chatbot.

1. Build Facebook integration with node.js backend
2. Deploy on Heroku

# Facebook integration

1. create a Facebook Page
2. create a Facebook App  --> https://developers.facebook.com/
3. subscribe your webhook to the page events

# Backend and Heroku
1. `git clone https://github.com/AdrianKrebs/facebook-chatbot-tutorial.git`
2. create heroku account --> https://signup.heroku.com/
3. `heroku create`
4. add environment variables to the heroku app --> https://devcenter.heroku.com/articles/config-vars
5. `git commit -m -a "initial commit" `
6. `git push heroku master`

# Environment variables

| variable        |value                        |
| -------------   |:-------------:              |
| appSecret       | facebook app secret         |
| pageAccessToken | facebook page access token  |
| validationToken | facebook validation token   |
