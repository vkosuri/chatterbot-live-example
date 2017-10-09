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
The chatterbot [corpus path](https://github.com/gunthercox/chatterbot-corpus/tree/master/chatterbot_corpus/data/english) could found here.

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

Deploying Python and Django Apps on Heroku https://devcenter.heroku.com/articles/deploying-python

Really execution starts [here](https://devcenter.heroku.com/articles/deploying-python#deploy-your-application-to-heroku)

## LICENSE
ChatterBot Django Live Example is licensed under [BSD 3-clause](./license.md)
