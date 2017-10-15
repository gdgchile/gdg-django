# gdg-django

Antes de comenzar
```
git reset --hard
```

Instlar django, pero primero configurar el ambiente de desarrollo, Ir a la terminal

```
$ python -m venv .venv
$ source .venv/bin/activate
```

si eres usuario windows 
```
path\to\your\.venv\Scripts\activate
```

Y ahora instalar django

```
pip install django
pip install psycopg2
pip freeze > requeriments.txt
```

El primero `pip install` instala dependencias dentro de tu ambiente y el segundo `pip freeze` lista las dependencias y `> requetiments` crea un archivo con esas dependencias.

Luego hay que crear un archivo llamado .gitignore e ignorar el ambiente virtual

```
echo ".venv" >> .gitignore
```

# siguiente paso
Para ir al siguiente paso, en donde se creará el projecto en django
```
git checkout step-3
```