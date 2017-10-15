# GDG-DJANGO
Antes de comenzar
```
git reset --hard
```

## La primera migración

Ejecuta lo siguiente, para crear las tablas de la configuración de django
```
$ python manage.py migrate
```
El comando migrate, revisa dentro de `INSTALLED_APPS` del archivo `mysite/mysite/settins.py` y creas las tablas necesarias de acuerdo a la configuración.


### Crear modelos

abrir el archivo `polls/models` y escribir lo siguiente

```
from django.db import models


class Question(models.Model):
    question_text = models.CharField(max_length=200)
    pub_date = models.DateTimeField('date published')


class Choice(models.Model):
    question = models.ForeignKey(Question, on_delete=models.CASCADE)
    choice_text = models.CharField(max_length=200)
    votes = models.IntegerField(default=0)
```

#### Activar los modelos

luego hay que activar estos modelos en el archivo `mysite/settings.py`

```
INSTALLED_APPS = [
    'polls.apps.PollsConfig',
    ...
]
```

#### ejecutar la migración

```
python manage.py makemigrations polls
```

Este comando creará en la carpeta migration el archivo `0001_initial.py`, este archivo contiene el codigo necesario para crear las tablas en la base de datos. Ahora lo unico que falta hacer es crear las tablas en la BD, ejecutando:

```
python manage.py migrate polls 0001
```


# Siguiente paso
Ir al siguiente paso
```
git checkout final
```