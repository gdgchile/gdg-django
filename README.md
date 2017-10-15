# GDG-DJANGO
Antes de comenzar
```
git reset --hard
```

# GET STARTED WITH DJANGO

Para crear un projecto en django, ejecuta

```
$ django-admin startproject mysite
```

donde mysite es el nombre de tu proyecto, anda inventa uno ;). Cuando tengas la estructura basica
de tu projecto en django, ejecuta el servidor

```
$ python mysite/manage.py runserver
```

y ahora anda al navegador y visita el sitio [localhost:8000](localhost:8000)

# Configurar la BD

Ahora hay que decirle a nuestro projecto django que use postgresql db, solo debes cambiar el archivo `settings.py`

Modifica la siguiente linea 
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```
por
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'gdgdjango',
    }
}

```


y por último, no olvides ignorar los archivos
```
$ echo "**/__pycache__" >> .gitignore
```

# Siguiente paso
Ir al siguiente paso
```
git checkout step-4
```