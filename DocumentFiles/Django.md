# Django Documentation

## Table of Contents
- [Django Setup on Windows](#Windows)

# Django Setup
## Windows

For this setup you may be intrested in fallowing this [page](https://docs.djangoproject.com/en/4.0/howto/windows/) instead.
I found the most sucsess using powershell but if you find CMD works for you go for it!

Start by seting up your virtual environment.
> [!IMPORTANT]
> Remember to replace the project Name with what you want the project to be called for the entirety of this guide.

```
py -3 -m venv Project_name
```
Now you can activate the virtual environment
```
Project_name\Scripts\activate
```

Now that the venv is active you can install django.
``` 
py -3 -m pip install Django
```
You may want to upgrade pip at this time.
```
python3 -m pip install --upgrade pip
```

For Help on creating a project go [here](#Project-Setup)

To deactivate your virtual environment run Ctrl-C (if you have a django project running) then enter deactivate.

# Project Setup

Once you have django installed and your vertual environment running you can fallow these instuctions. Remember to change the project name to your own.
```
django-admin startproject django_project_name
```
If you want to be able to activate your project from the same place you controll your virual environment go ahead and do this. (I beleive this is optional just makes your life a little easier in the long run)
```
mv django_project_name/manage.py ./ 
mv django_project_name/django_project_name/* django_project_name
rm -r django_project_name/django_project_name/
```
You can run your server now with the command. Remember if you skiped the last step you will need to modify this command path for manage.py or navigate to the folder containing manage.py
```
python manage.py runserver
```
Now you Have started the server go to [http://localhost:8000/](http://localhost:8000/) to se if its working. Use (on windows)ctrl+C to stop the server.
