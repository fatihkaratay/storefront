1. Install the framework and necassary modules. 
```
pipenv install django
```
There are `two` files created:  
* Pipfile: This is like `package.json` file in JS projects. 
* Pipfile.lock
2. Activate the virtual env to use the python in here. 
```
pipenv shell
```
3. Use django admin to start a new project.
```
django-admin startproject storefront
```
This command will create a project but the folders will be redundant. To fix this, use the following command:
```
django-admin startproject storefront .
```
Let's identify what those are used for:  
`storefront`: Core of the application  
`manage.py`: Wrapper around dhango-admin. Going forward, instead of django-admin, we'll be using this. Takes the settings of the project into account.

Each App plays certain functionality in django projects. They can found under `settings.py` file like below:  
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```
Those apps come as default for every django project.  
Here are the short descriptions of those apps:  
`admin`: Admin interface for managing our data.  
`auth`: Authenticating users.  
`contenttypes`: 
`sessions`: Legacy app. creating a short memory. It's not being used anymore.  
`messages`: Displaying one time notification to the user.  
`staticfiles`: Serving static files like images, css etc.  

Here is how to create a new app:  
`python manage.py startapp playground`  
When you look at the folder structure, you will see the same folder structure.
`migrations`: All the migration stuff will be here.  
`admin.py`: Define how the admin interface for this app will look like  
`apps.py`: Configure this app. Like config file. The name is misleading.
`models.py`: Define the model classes here. We use model classes for representing the data in the database. 
`test.py`: write the unit tests in here.
`views.py`: Request handler. it's not a view folder like MVC framework. Name is misleading.

Once this app is created, the next step is register this app into the `settings` module. Everytime you create a new app, it needs to be registered to the settings module.
