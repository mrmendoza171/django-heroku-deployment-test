# django-heroku-deployment-test
Testing and documenting steps to upload project to Heroku


- install heroku
- login to heroku from CLI
- create Django project and navigate into
- create requirements.txt in project root
    - pip freeze
- pip install gunicorn
- create git repository locally
- create .gitignore
    - python template - https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbl9zR1lTZmJGX213OFIyLV9Lb1ZNRnFyNEdtd3xBQ3Jtc0tuWVBtYktsSlNZanluelZoR0MxSm5INDdtbWJCa2kxeVFsc0syTk9TemdOQllkUVhUTWZwaGh5WHlBTlNsR3QzWnhlUU84RzRIbVVRSjJ3VWJEMk13Y2ZsYTdsTmxKVzZNb1pzSXFBZ05nMTRjV1pBcw&q=http%3A%2F%2Fbit.ly%2Fdjango-req-txt-file&v=6DI_7Zja8Zc
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
