#gdg-django

## Instalation

### Install postgresql

Dependiendo de tu sistema operativo, sigue las instrucciones

#### MAC OS X
Primero instalar Hombrew, abrir terminal y:

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

y luego instalar postgresql

```
$ brew install postgresql
```

#### Debian/Ubuntu

```
$ sudo apt-get update
$ sudo apt-get install postgresql postgresql-contrib
```

#### Windows

ir a la pagina [postgresql](https://www.postgresql.org/download/windows/) y descargar el instalador, luego seguir las instrucciones

### Install python

Dependiendo de tu sistema operativo, sigue las instrucciones

### MAC OS X
Para instalar python, primero instalar pyenv con hombrew

```
$ brew install pyenv
```

Luego instalar python 3.6
```
$ pyenv install 3.6.2
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
$ pyenv global 3.6.2
```

### Debian/Ubuntu

Install:

```
$ curl -L https://raw.githubusercontent.com/pyenv/pyenv-installer/master/bin/pyenv-installer | bash
$ pyenv update
```

Luego instalar python 3.6
```
$ pyenv install 3.6.2
$ pyenv global 3.6.2
```


### Windows
Go to [python web page](https://www.python.org/) and download the latest version and follow the instruccion

