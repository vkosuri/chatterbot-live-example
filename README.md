# ChatterBot Django Live Example

This is an example Django app that shows how to create a simple chat bot web
app using [Django](https://ww.djangoproject.com) and [ChatterBot](https://github.com/gunthercox/ChatterBot).

## Documentation

Start the Django app by running 

``` Bash
python manage.py runserver 0.0.0.0:8000
```

Further documentation on getting set up with Django and ChatterBot can be found in the [ChatterBot documentation](http://chatterbiot.readthedocs.io/en/latest/django.html)

## Make migrations

``` Bash
python manage.py migrate
```
## Train your bot

``` Bash
python manage.py train
```

## Training Corpus Path
The chatterbot [corpus path](https://github.com/gunthercox/chatterbot-corpus/tree/master/chatterbot_corpus/data/english) can be found here.

## Bot Django Settings
You could found Bot settings [here](./example_app/settings.py)

``` Python
CHATTERBOT = {
    'name': 'Chatterbot Live Example',
    'logic_adapters': [
        'chatterbot.logic.MathematicalEvaluation',
        'chatterbot.logic.TimeLogicAdapter',
        'chatterbot.logic.BestMatch'
    ],
    'trainer': 'chatterbot.trainers.ChatterBotCorpusTrainer',
    'training_data': [
         'chatterbot.corpus.english'
    ]
}
```

## Deploying on Heroku

Here some of the steps lauch your Django app with Heroku

### Build your app and run it locally

``` bash
pip install -r requirements.txt
Downloading/unpacking ...
...
Successfully installed Django dj-database-url dj-static django-toolbelt gunicorn psycopg2 static3
Cleaning up...
```

### To run your application locally,

``` bash
heroku local web
11:48:19 web.1  | started with pid 36084
11:48:19 web.1  | 2014-07-17 11:48:19 [36084] [INFO] Starting gunicorn 19.0.0
11:48:19 web.1  | 2014-07-17 11:48:19 [36084] [INFO] Listening at: http://0.0.0.0:5000 (36084)
11:48:19 web.1  | 2014-07-17 11:48:19 [36084] [INFO] Using worker: sync
11:48:19 web.1  | 2014-07-17 11:48:19 [36087] [INFO] Booting worker with pid: 36087
``` 
Your app should now be running on http://localhost:5000/.

### Deploy your application to Heroku

``` Bash
git add .

git commit -m "Added a Procfile."

heroku login
Enter your Heroku credentials.
...

heroku create
Creating intense-falls-9163... done, stack is cedar
http://intense-falls-9163.herokuapp.com/ | git@heroku.com:intense-falls-9163.git
Git remote heroku added

git push heroku master
...
-----> Python app detected
...
-----> Launching... done, v7
       https://intense-falls-9163.herokuapp.com/ deployed to Heroku
```

A more detailed information ca be found here https://devcenter.heroku.com/articles/deploying-python

## LICENSE
ChatterBot Django Live Example is licensed under [BSD 3-clause](./license.md)

