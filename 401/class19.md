# Intro to Django
## Django install
***make sure you install python first***
```$ git clone https://github.com/django/django.git```
```$ python -m pip install -e django/```
### django supports the MVC design pattern, you define a class for each model required in the web app.
```python
class Band(models.Model):
    """A model of a rock band."""
    name = models.CharField(max_length=200)
    can_rock = models.BooleanField(default=True)


class Member(models.Model):
    """A model of a rock band member."""
    name = models.CharField("Member's name", max_length=200)
    instrument = models.CharField(choices=(
            ('g', "Guitar"),
            ('b', "Bass"),
            ('d', "Drums"),
        ),
        max_length=1
    )
    band = models.ForeignKey("Band")
```
### Django has a urls.py file under the project by default. It also has a prep-defined path for the admin app. However, Django recommends mapping all resources via another urls.py newly created under the app. The below explains it:

```python
from django.contrib import admin  
    from django.urls import path, include

    urlpatterns = [  
        path('admin/', admin.site.urls),  
        path('myapp/', include('myapp.urls')),  
    ]  
```
```python
  from django.urls import path
    from . import views
 
    urlpatterns = [  
        path('', views.index),  # app homepage
    ] 
```
***Django View Function***
```python
    def index(request):
        return render(request, 'index.html', {})
        
    or,
    
    from django.http import HttpResponse
    def index(request):
        return HttpResponse("Hello World") 
```
django allows rendering views and HTML pages so powerful and easily, for example:
```html
<html>
  <head>
    <title>Band Listing</title>
  </head>
  <body>
    <h1>All Bands</h1>
    <ul>
    {% for band in bands %}
      <li>
        <h2><a href="{{ band.get_absolute_url }}">{{ band.name }}</a></h2>
        {% if band.can_rock %}<p>This band can rock!</p>{% endif %}
      </li>
    {% endfor %}
    </ul>
  </body>
</html>
```
