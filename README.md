tinderbox
=========

Another [@crockpotveggies](https://twitter.com/crockpotveggies) experiment.

Tinderbox is an experiment built on the Tinder app API. Tinderbox helps automate the filtering of Tinder users ("swiping left") and collect data to analyze your own success. Tinderbox not only gives you a desktop interface for Tinder, but also provides a bot in the background.

![Screenshot](https://raw.githubusercontent.com/crockpotveggies/tinderbox/master/public/img/screenshot.jpg)

Tinderbox is built on top of [Play!](http://www.playframework.com/) 2.2 and uses Akka, Spark, and other libraries for face detection in the background.

### Getting Started

First read the "Running" section below to learn how to start the app.

Tinderbox starts up a server that is accessible in your browser at `http://localhost:9000/`. Once you're inside, note that there a bot running in the background. If you watch the logs in terminal, it will show you debug statements about the moves the bot is taking. There is an action log available in the main interface.

Most of Tinder's primary functionality has been re-created in Tinderbox. Note that if Tinder updates or changes its API it could potentially break this app.

### Running

Commands to run this Application:

1. sbt clean
2. sbt compile
3. sbt run

Note: 
> Scala Build Tool (SBT) is the preferred method of running this applications. You will need to install [SBT](http://www.scala-sbt.org/) before running the app.
> SBT will automatically download Play! and also pick up changes in the code if you wish to use them.

### Authenticating with Tinder

You will need to authorize using a Facebook `access_token` and also with your Facebook ID. The login page has a link for you to create an access token. Copy the token from Facebook's URL and paste it in the Tinderbox login.

Tinderbox will automatically attempt to find your Facebook ID once you copy and paste your `access_token`. If it doesn't appear within one second you'll need to manually enter it. For convenience, you can also paste the entire URL from the Facebook authentication URL and the app will auto-extract your `access_token`.

### Support

Currently I'm not offering any support, but if there's enough interest I'd consider helping others contribute to the code.

- Find a bug? It's OK to file an issue - I may not follow up on it.
- Want a feature? Please don't open an issue, instead contribute and open a pull request.

### Word from the Author

Tinderbox is the first bot I've built to interact on my behalf. Since it is a tool that automates a lot of the Tinder experience, be forewarned not everyone appreciates being met through a robot. And they certainly don't appreciate if you decide to use this code to spam the Tinder world.

### License

Tinderbox is distributed under the Creative Commons Attribution-NonCommercial 3.0 license, a human readable version is available at [https://creativecommons.org/licenses/by-nc/3.0/](https://creativecommons.org/licenses/by-nc/3.0/).

Because the Tinder API hasn't been officially released as a public API, Tinderbox is licensed for non-commercial reasons only. I have no affiliation with Tinder, and you use this repository at your own risk. Please think before mixing this code with something that could be considered abusive of the Tinder API.
