# DJANGO_POSTGRESQL_DOCKER_TEMPLATE

Quickly setup a Django project using Dockers.
Based on python:3 and Postgres official dockers

## Use

Run `sudo docker-compose run web django-admin startproject myProjectName .` to:
- create a django project in ./myProjectName/
- run a web server accesible in localhost:8000

By default, django project will use sqlite. To use Postgres, edit myProjectName/settings.py and change database 

From:
```
# Database
# https://docs.djangoproject.com/en/3.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

To 
```
# Database
# https://docs.djangoproject.com/en/3.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'PASSWORD': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

## Author 

Miguel M miguelm[at]unizar[dot]es


## License

European Union Public Licence V. 1.2 
[LICENCE.txt](LICENCE.txt)
