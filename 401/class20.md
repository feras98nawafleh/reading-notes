# Django Models
A Django model is the built-in feature that Django uses to create tables, their fields, and various constraints. In short, Django Models is the SQL of Database one uses with Django. SQL (Structured Query Language) is complex and involves a lot of different queries for creating, deleting, updating or any other stuff related to database. Django models simplify the tasks and organize tables into models. Generally, each model maps to a single database table.
This article revolves about how one can use Django models to store data in the database conveniently. Moreover, we can use admin panel of Django to create, update, delete or retrieve fields of a model and various similar operations. Django models provide simplicity, consistency, version control and advanced metadata handling. Basics of a model include –

Each model is a Python class that subclasses django.db.models.Model.
Each attribute of the model represents a database field.
With all of this, Django gives you an automatically-generated database-access API
```python
from django.db import models

# Create your models here.
class GeeksModel(models.Model):
	title = models.CharField(max_length = 200)
	description = models.TextField()
```
Creating a Model
Syntax

from django.db import models
        
class ModelName(models.Model):
        field_name = models.Field(**options)
        
```python
# import the standard Django Model
# from built-in library
from django.db import models

# declare a new model with a name "GeeksModel"
class GeeksModel(models.Model):
		# fields of the model
	title = models.CharField(max_length = 200)
	description = models.TextField()
	last_modified = models.DateTimeField(auto_now_add = True)
	img = models.ImageField(upload_to = "images/")

		# renames the instances of the model
		# with their title name
	def __str__(self):
		return self.title
```
# Django Admin
ModelAdmin objects¶
class ModelAdmin¶
The ModelAdmin class is the representation of a model in the admin interface. Usually, these are stored in a file named admin.py in your application. Let’s take a look at an example of the ModelAdmin:
```python
from django.contrib import admin
from myapp.models import Author

class AuthorAdmin(admin.ModelAdmin):
    pass
admin.site.register(Author, AuthorAdmin)
```
```python
from django.contrib import admin

class FlatPageAdmin(admin.ModelAdmin):
    fieldsets = (
        (None, {
            'fields': ('url', 'title', 'content', 'sites')
        }),
        ('Advanced options', {
            'classes': ('collapse',),
            'fields': ('registration_required', 'template_name'),
        }),
    )
```
