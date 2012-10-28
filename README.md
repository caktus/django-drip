Django Drip
====================

[![Build Status](https://secure.travis-ci.org/zapier/django-drip.png)](http://travis-ci.org/zapier/django-drip)

Use admin powered User querysets to send drip campaign emails.

[Read the docs at ReadTheDocs!](https://django-drip.readthedocs.org/en/latest/)


### Installing:

We highly recommend using pip to install *django-drip*, the packages are regularly updated 
with stable releases:

```
pip install django-drip
```

Next, you'll want to add `drip` to your `INSTALLED_APPS` in settings.py.

```python
INSTALLED_APPS = (
    'django.contrib.contenttypes',
    'django.contrib.comments',
    'django.contrib.sessions',
    'django.contrib.sites',
    'django.contrib.admin',

    # Your favorite apps

    'drip',
)
```

Don't forget to add `DRIP_FROM_EMAIL` to settings.py, or else we will fall back to `EMAIL_HOST_USER`.

Finally, be sure to run `python manage.py syncdb` or `python manage.py migrate drip` to set up
the necessary database tables.

```
python manage.py syncdb
# or...
python manage.py migrate drip
```