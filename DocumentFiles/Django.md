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

```py -3 -m venv Project_name```
Now you can activate the virtual environment
```Project_name\Scripts\activate```

Now that the venv is active you can install django.
``` py -3 -m pip install Django```
You may want to upgrade pip at this time.
```python3 -m pip install --upgrade pip```

For Help on creating a project go [here](#Project-Setup) PAGE NOT CREATED YET

To deactivate your virtual environment run Ctrl-C (if you have a django project running) then enter deactivate.

# Project Setup


