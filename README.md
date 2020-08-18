An introduction to Django. 

Django is a Python-based free and open-source web framework that follows the model-view-controller architectural pattern. 

**mysite** - contains the entire django project.

**mysite/polls** - contains the polls app. 

**django-polls** - contains the files used to package the polls app.

Already have a django project and would like to include this polls app?

- Download the django-polls package. You can find it in *django-polls/dist/django-polls-0.1.tar.gz* 
- Install it using the command (python -m pip install --user django-polls-0.1.tar.gz). In case you're using a virtual environment exclude --user.
- Register the app by including *'polls.apps.PollsConfig',* in your project's setting.py file in the installed apps section.
- Also include *path('polls/', include('polls.urls')),* in your project's urls.py file in the urlpatterns section.
- While in your project's root directory run *python manage.py makemigrations polls* then run *python manage.py migrate*. This would create the needed tables for the polls app in your database.
- You should now be able to access the polls app (e.g 127.0.0.1:8000/polls). Ofcourse after running *python manage.py runserver* in your project's root directory.

It's the most basic app you'll ever come across. Don't judge.

A tutorial for the same is available in the official Django Documentation.
