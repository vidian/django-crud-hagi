How to install django for such as dumb beginner

NOTE : <...> any variable inside this bracket you should change it with your any variables name

Step 1 : Install virtualenv (make sure you already install and setup python in your PC)
- This virutalenv or Virtual Environment allows you install python library locally only in your project directory, you can install it with this command 'python -m venv <YOURVENVNAME>'.
- After you install the venv then activate your venv with this command '<YOURENVNAME>/Script/actiave' or you can do like this also 'cd <YOURENVNAME>/Script/' then run the activate script

Step 2 : Install Django and MySql
- Install Django and mysql with this command 'pip install django mysqlclient'

Step 3 : Make a new project in Django
- After Django is installled, you need to make a new project with this command 'django-admin startproject <YOURPROJECTNAME> .'
- Then cd to your <YOURPROJECTNAME>, now you need to make a new app with 'python manage.py startapp <YOURAPPNAME>'
(Startproject is command to produce django project structure, startapp is for creating specific your app name for this/main project)

Step 4 : Open your code editor and go to settings.py
- In case you use VsCode you can type this command 'cd ../ && code .'
- Open settings.py and change this file with this following instructions below
	Find Installed App and add you app like this
	INSTALLED_APPS = [
             ...
             <YOURAPPNAME>
        ]

	One last time find a database and change it with mysql like this
	DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '<YOURDBNAME>',
        'USER': '<YOURUSERMYSQL>',
        'PASSWORD': '<YOURPASSWORDMYSQL>',
        'HOST': 'localhost',   
        'PORT': '3306',            }
}

- Migrate your database, type this on your terminal, 'python manage.py migrate'

Step 5 : Try to run your Django project
- Type this command to run your django project, 'python manage.py runserver'

If you have any issues please chat me on whatsapp.
AFTER YOU SUCCESSFULLY CREATE THIS PROJECT PLEASE MAKE SURE YOU PUSH AND MAKE A PULL REQUEST, BUT FIRST YOU NEED TO INSTALL GIT AND GITHUB DESKTOP.

Another notes:
if you installing a new packages in the future please type this command to produce a requirements.txt for your project 'pip freeze > requirements.txt', do this command in the root project directory
also add yor env path to .gitignore, no need to push env directory on github