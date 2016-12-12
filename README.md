ChatterBot Django Live Example
==============================

This is an example Django app that shows how to create a simple chat bot web
app using [Django] (https://ww.djangoproject.com) and [ChatterBot] (https://github.com/gunthercox/ChatterBot).

Documentation
-------------

Start the Django app by running ``python manage.py runserver 0.0.0.0:8000``

Further documentation on getting set up with Django and ChatterBot can be
found in the [ChatterBot documentation] (http://chatterbiot.readthedocs.io/en/latest/django.html)

Corpus Path
-----------
https://github.com/gunthercox/ChatterBot/tree/master/chatterbot/corpus/data

Logic Adapters
--------------
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
         'chatterbot.corpus.english.greetings'
    ]
}
```

