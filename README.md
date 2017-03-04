# SpringBot
Messenger Bot that, based on typed text, query spring documentation and return 3 first results. Read this blog post for more details: https://aboullaite.me/my-first-java-bot/

![](http://i.giphy.com/l0IymLb7VE5KobYXu.gif)

### Run the App
First thing you need to do is to setup a Facebook app, Please follow this [link](https://developers.facebook.com/docs/messenger-platform/guides/setup) for more details. You'll need also a free hosting service like [Heroko](https://www.heroku.com/) or [Clever Cloud](https://www.clever-cloud.com/), or you can simply use [NGROK](https://ngrok.com/). and don't forget to create a [Facebook page](https://www.facebook.com/pages/create).

Once all done, follow this steps:

- open https://developers.facebook.com/apps
click the 'Add a New App' button
- enter the Display Name, e.g. spring-bot
select the Category: 'Apps for Messenger'
- click the 'Create App ID' button
- Section 'Token Generation': Select your created FB Page
- copy the 'Page Access Token' to the clipboard
- copy it to your `application.yml`
- navigate to 'Dashboard'
- copy the 'App Secret' to the clipboard
- copy it to your `application.yml`
- use a randomly generated string as 'Verify Token'
- deploy you app, and copy your public HTTPS URL (callback url)
- navigate back to 'Messenger'
- Section 'Webhooks': Click the 'Setup Webhooks' button
- past the Callback URL and your verify token
- select the following Subscription Fields: `messages`, `messaging_postbacks`, `messaging_optins`, `message_deliveries`, `message_reads`, `message_echoes`
- click the 'Verify and Save' button
- Section 'Webhooks': Select your created FB Page to subscribe your webhook to the page events
- click the 'Subscribe' button
