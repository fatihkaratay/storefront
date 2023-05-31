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