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

### Lead Update & delete view

-   Created Update and Delete view in `views.py`

### URL Names

-   The problem with urls without name is , when we change a url , others urls become invalid.
-   URL names helps in creating dynamic links.
-   the syntax is like this: `{% url 'app_url_name:url_name' %}`
-   Applied this syntax to all templates

### Styling

-   Extended Base.html
-   Added Tailwind CSS
-   Added & Extended Class base generic views to shorten the `views.py`
-   Staticfiles configured
-   Send mails using django main module

### Authentication & tests

-   Used django inbuilt login and logout Views
-   Customized user creation model
-   Create test folder inside the app and done the testing, we dont need to configure test folder path, its recognized by default

### Auth permission (login required/LoginRequiredMixin)

-   Used LoginRequiredMixin to authenticate user
-   used post_save signal to save the userProfile

### Agent CRUD operations

-   Agent detail operation done.
-   Agent create operation done.
-   Agent update operation done.
-   Agent delete operation done.
-   Custom Agent mixin applied

### filtering

-   filtered lead-queryset
-   invite agent to lead
