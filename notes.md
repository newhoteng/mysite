"python manage.py makemigrations polls"
- By running makemigrations(Generate migration), you’re telling Django that you’ve made some changes to your models (in this case, you’ve made new ones) and that you’d like the changes to be stored as a migration.

"python manage.py migrate"
- The migrate command takes all the migrations that haven’t been applied (Django tracks which ones are applied using a special table in your database called django_migrations) and runs them against your database - essentially, synchronizing the changes you made to your models with the schema in the database.

Three-step guide to making model changes:
- Change your models (in models.py).
- Run 'python manage.py makemigrations' to create migrations for those changes
- Run 'python manage.py migrate' to apply those changes to the database.

"python manage.py shell"
- To invoke the Python shell and use the API Django provides
- We’re using this instead of simply typing “python”, because manage.py sets the DJANGO_SETTINGS_MODULE environment variable, which gives Django the Python import path to your mysite/settings.py file.

"python manage.py test polls"
- To run tests in the polls app

"coverage run --source='.' manage.py test myapp"
- To run coverage to get test coverage

"coverage report"
- To see a report on the test coverage