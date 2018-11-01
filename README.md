# django-bay-polls 

Polls is a simple Django app to conduct Web-based polls. For each
question, visitors can choose between a fixed number of answers to
vote on.

Detailed documentation will be in the "docs" directory.

# Quick start
-----------

### Installation
If you want to install latest stable release from PyPi here's the command:

```sh
$ pip install django-bay-polls
```

Add "polls" to your INSTALLED_APPS setting:

```
INSTALLED_APPS = (
    ...
    'polls',
    ...
)

```
Next, include the polls URLconf in your project's urls.py like this:
```
urlpatterns = patterns('',
    ...
    url(r'^polls/', include('polls.urls', namespace='polls')),
    ...
)
```
do remember to put the comma(,) at the end to avoid unnecessary typos

From there run `python manage.py migrate` to create the polls models.

Next is to start your development server and visit http://127.0.0.1:8000/admin/ 
to create a poll.
