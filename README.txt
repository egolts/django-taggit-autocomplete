This is a fork of django-tagging-autocomplete, which can be found at:
http://code.google.com/p/django-tagging-autocomplete/

It's virtually the same app, only it's changed to work with django-taggit:
http://github.com/alex/django-taggit

This branch has been forked from eka's version.  As long as used with grappelli, no extra js is needed.

*** Installation ***

   1. You need to have django-taggit already installed
   2. Download django-taggit-autocomplete and use setup.py to install it on your system:
		python setup.py install
   3. Add "taggit_autocomplete" to installed apps in your project's settings.
   4. Add the following line to your project's urls.py file:

      (r'^taggit_autocomplete/', include('taggit_autocomplete.urls')),

*** Usage ***
** Using the model field **

You can use TaggableManager to enable autocompletion right in your models.py file. In most cases this is the easiest solution. Example:

from django.db import models
from taggit_autocomplete.managers import TaggableManager

class SomeModel(models.Model):
        tags = TaggableManager()
