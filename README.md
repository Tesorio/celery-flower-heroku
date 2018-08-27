# Celery Flower monitoring for Heroku

[Flower](https://github.com/mher/flower/) is a handy tool for monitoring [Celery](http://www.celeryproject.org/) processes. As it's build on top of Tornado web server it needs it's own outside facing port and can't be run as part of your regular Heroku app which only provides one ```web``` process type. Luckily Flower is really easy to install as another app and can be run free of charge on Heroku.

This project template/guide helps you to bootstrap the process and creates a simple app for running Flower.

Clone the repo:

    git clone https://github.com/Tesorio/celery-flower-heroku.git

Create an Heroku app:

    heroku create APP_NAME

You will need to set the following environment variables (read more about auth here https://flower.readthedocs.io/en/latest/auth.html):

    BROKER_URL FLOWER_OAUTH2_KEY FLOWER_OAUTH2_REDIRECT_URI FLOWER_OAUTH2_SECRET

Push to heroku:

    git push heroku master

Now visit the app.
