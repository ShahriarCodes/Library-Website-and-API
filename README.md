# Library-Website-and-API
The first project from the book **Django for APIs - Build web APIs with Python and Django** \
by *William S. Vincent* \
Get the book at [here](http://leanpub.com/djangoforapis)


# Installation
First clone the repo
```
$ git clone https://github.com/shahriar100/Library-Website-and-API/
```


To install Pipenv we can use pip3 which Homebrew automatically installed for us alongside Python 3.


```
$ pip3 install pipenv
```

Cd into the directory and install dependecies from piplock

```
$ cd Library-Website-and-API
$ pipenv install
```

If you look within our directory there are now two premade files: Pipfile and Pipfile.lock. We have the information we need for a new virtual environment but we have not activated it yet. Let’s do that with pipenv shell.

```
$ pipenv shell
```

If you are on a Mac you should now see parentheses around the name of your current directory on your command line which indicates the virtual environment is activated. Since we’re in a django directory that means we should see (django) at the beginning of the command line prompt. Windows users will not see the shell prompt. If you can run django-admin startproject in the next section then you know your virtual environment has Django installed properly.

```
(Library-Website-and-API) $
```

This means it’s working! Now migrate the database and run the server 

```
(Library-Website-and-API) $ python nanage.py makemigrations
(Library-Website-and-API) $ python nanage.py migrate
(Library-Website-and-API) $ python nanage.py runserver

Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
January 22, 2021 - 02:18:54
Django version 2.2.6, using settings 'library_project.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

```

Working directory structure

```
(Library-Website-and-API) $ tree
.
├── api
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── serializers.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── books
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   ├── 0001_initial.py
│   │   └── __init__.py
│   ├── models.py
│   ├── templates
│   │   └── books
│   │       └── book_list.html
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── db.sqlite3
├── library_project
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
├── Pipfile
└── Pipfile.lock

7 directories, 27 files

```

