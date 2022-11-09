# django-heroku-deployment-test
Testing and documenting steps to upload project to Heroku
[Python Django Tutorial: Deploying Your Application (Option #2) - Deploy using Heroku](https://www.youtube.com/watch?v=6DI_7Zja8Zc)

- install heroku
- login to heroku from CLI
- create Django project and navigate into
- create requirements.txt in project root
    - pip freeze
- pip install gunicorn
- create git repository locally
- create .gitignore
    - python template - https://github.com/github/gitignore/blob/main/Python.gitignore
    - add .DS_Store for Mac

- heroku create <appname>
- heroku open


- git push heroku master

- create STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')

- create Procfile
    - web:gunicorn <django_project>.wsgi

- add heroku site in ALLOWED_HOSTS


- add environment variables for DEBUG and SECRET_KEY

- check addons: heroku addons
- add postgres: heroku addons: create heroku-postgresql:hobby-dev
- heroku pg


- pip install django-heroku
- import django_heroku in settings.py
- django_heroku.settings(locals())


- update requirements.txt
- heroku run python manage.py migrate
- heroku run bash
