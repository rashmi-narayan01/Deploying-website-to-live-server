# Deploying-website-to-live-server

Heroku Cloud is used to deploy website to cloud server. 

## Create Python Virtual Environment and install Flask
1. Install Virtual environment: in cmd, type "pip install Virtualenv"
2. Create virtual environment: in cmd, type "python -m venv virtual". This should create the virtual folder that you see in the repository.
3. Install Flask in virtual environment: in cmd, type "virtual\Scripts\pip install flask"

## Deploying website to live server
1. Create an account on Heroku.com
2. Download Heroku toolbelt
3. Open mysite directory in cmd and login to Heroku by "heroku login"
4. Create Heroku app by "heroku create app_name"
5. Upload your files to Heroku:
6. Git is installed by default while installing Heroku toolbelt. If not, install Git.
7. Create file requirements.txt. This informs Heroku to install flask.
    Install gunicorn in virtual environment by "..\virtual\Scripts\pip install gunicorn".
    To list all the packages and libraries in virtual environment, type "..\virtual\Scripts\pip freeze"
    To add these to requirements.txt, type "..\virtual\Scripts\pip freeze > requirements.txt"
8. Create Procfile without any extension.
    Open file and type "web: gunicorn script1:app". This informs Heroku which server to use. 
9. Create runtime.txt. Enter the python version in which your app should run. For example "Python-3.7.3"
    Please see the following link for the current supported runtime for Python 3. Make sure that your runtime.txt file contain that runtime.
    https://devcenter.heroku.com/articles/python-runtimes#supported-python-runtimes
Upload files using git:
10. Create git repository by "git init"
11. Add files by "git add ."
12. Commit files by "git commit -m "first comm""
13. Point to your app be "heroku git:remote --app app_name"
14. Push files to Heroku by "git push heroku master"
15. Now you can browse your webpage by app_name.herokuapp.com
