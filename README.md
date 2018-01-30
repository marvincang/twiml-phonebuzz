# Twiml-PhoneBuzz-P1

Twiml-PhoneBuzz-P1 is a Node.js app using [Express 4](http://expressjs.com/) hosted in [Heroku](https://www.heroku.com/). This is the first phase of LendUp coding challenge. Try the app [https://twiml-phonebuzz.herokuapp.com](https://twiml-phonebuzz.herokuapp.com)

Call the number listed in the web to play PhoneBuzz, a Fizz Buzz game played via phone call using Twilio. When prompted to enter a number to listen to the engine speaking in Fizz Buzz language from 1 up until the number given.

## Dependencies

During development, Twiml-Phonebuzz-P1 used these libraries (available from npm):
  * "body-parser": "v1.18.2",
  * "express": "v4.15.2",
  * "twilio": "v3.11.0"

## Running Locally

### Set up

Make sure you have [Node.js](http://nodejs.org/) and the [Heroku CLI](https://cli.heroku.com/) installed.

```sh
$ git clone https://git.heroku.com/twiml-phonebuzz.git # or clone your own fork
$ cd twiml-phonebuzz
$ npm install body-parser express twilio
$ npm start
```

Your app should now be running on [localhost:5000](http://localhost:5000/). This default code is using my free trial Twilio account with the number listed in the app. You can't use this number because the number is associated only with Heroku app URL, not localhost. Follow this next step to adjust the code with any other Twilio credentials.

### Using Other Twilio Account

Few changes has to be made to the code:

  * Delete the authToken in index.js line 9 and hard code to your Twilio's authToken (Not recommended) or use process.env.TWILIO_AUTH_TOKEN if you've saved your token in local environment variable.
  * Uncomment line 33 in index.js
  * Comment line 34 in index.js

  * [Optional]: Change the number in public/index.html to your Twilio phone number. This only affects the app's UI.


Follow this blog [post](https://www.twilio.com/blog/2013/10/test-your-webhooks-locally-with-ngrok.html) to host the code locally and connect the local url to your Twilio account.
