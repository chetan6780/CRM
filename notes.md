### Initial setup

-   Created virtualenv with `virtualenv env`
-   Activated virtualenv with `.\env\Scripts\activate`
-   installed django 3.2.6
-   created `requirements.txt` with `pip freeze > requirements.txt`
-   Created djcrm `django-admin startproject djcrm .`
-   added python-gitignore from github
-   migration - `python manage.py migrate`
-   Hidden: secret_key in .env
-   `pip install python-decouple` for [django secret_key hiding](https://stackoverflow.com/questions/64208678/hiding-secret-key-in-django-project-on-github-after-uploading-project)

### Adding App

-   `python manage.py startapp leads`
-   added 'leads' in INSTALLED_APPS in settings.py

### Initial Model

-   Created User, Lead and Agent model
-   One to one is like foreign key but it has only one to one relationship
-   models.CASCADE : deletes the related object when the object is deleted

### Register in admin

-   Created **str** method in models
-   Registered User, Lead and Agent model in admin

### Views, Urls and Template

-   Created homepage views, urls.
-   **If we create Templates folder inside the app, by default it will be recognized by django**
-   **If we create templates folder inside BASE DIR we have to add it in DIRs in settings.py**

### Leads and Lead detail page

-   Created leads page
-   created lead detail page
-   connected both the pages ti each other

### Form to create leads

-   Created form in `forms.py`
-   imported it in views and handled post request
-   Shortened the code by using `LeadModelForm()`
