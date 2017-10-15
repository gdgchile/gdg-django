# GDG-DJANGO
Antes de comenzar
```
git reset --hard
```

# Tu primera app django

Para crear una app en django, se debe ejecutar el siguiente commando
```
$ cd mysite
$ python manage.py startapp polls
```
Este creará una app llamada polls

## La primera vista
Abre el archivo polls/view.py

```
from django.http import HttpResponse


def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")
```

ahora crea el archivo urls.py en la carpeta polls y añade el siguiente codigo
```
from django.conf.urls import url

from . import views

urlpatterns = [
    url(r'^$', views.index, name='index'),
]
```


El siguiente paso es decirle mysite que redireccione las urls, en el archivo `mysite/urls.py`

```
from django.conf.urls import include, url
from django.contrib import admin

urlpatterns = [
    url(r'^polls/', include('polls.urls')),
    url(r'^admin/', admin.site.urls),
]
```


## Ejecuta el servidor
```
python manage.py runserver
```


# Siguiente paso
Ir al siguiente paso
```
git checkout step-5
```