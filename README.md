## What is Slack Bot?
 Slack bot is a simple code which can respond to channels, direct messages on your behalf or as a programable bot.

There are many ways to write a bot for which slack provides different documentations, bit i feel the offical docs are very 
confusing. You can programme a bot via webhook/webapi or sockets in our case I find webhooks very effective and simple.
Slack offical docs has good walkthrough on webhook and sockets. You can choose whichever you may like.

### There are two parts in programming a bot

* #### Authentication.

* #### URL pinging.

### Steps 

* Step 1: Register your application on the slack developer api website and obtain client_id and client_secret.
* Step 2: Provide a callback url to the app settings.
* Step 3: Whenever someone clicks on your link(the call back url). Use the code which slack API will send to your registered 	 URL, grab the code parameter from there, we will need to
        obtain the client credentials.
* Step 4: Ping the https://slack.com/api/oauth.access?client_id=your_client_id&client_secret=client_secret&code=code_from_step_4.
* Step 5: Store the team name, id, access-token and other credintials to use them later on.
* Step 6: Whenever someone pings your bot the server will ping your bot with the message. 
* Step 7: You can decide to reply back accordinly but your response will also result in one more request to your api .
* Step 8: Make sure your don't reply back otherwise your bot will keep pinging the same msg again and again.
