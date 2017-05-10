This project was created using the Express Generator. It works fine locally, and works fine upon initial push to Heroku. After making any changes however and trying to push them to Heroku, the app no longer works (but still works fine locally).

See [this question on Stackoverflow](http://stackoverflow.com/questions/43881139/an-app-that-runs-locally-will-not-run-on-heroku)

Steps to reproduce:

    $ express --view pug --css sass --git .
    $ yarn install
    $ git init
    $ git remote
    $ heroku git:remote -a my-app-name
    $ git commit -m "test"
    $ git push heroku master

      [app works fine]

    $ yarn add bootstrap-sass
    $ heroku local web

      [app runs just fine locally]

    $ git add .
    $ git push heroku master

      [no errors on console, but visiting the app results in a crash]
