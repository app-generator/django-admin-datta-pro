# Django Admin Datta Able PRO

Modern template for **Django Admin Interface** coded on top of **[Datta Able Dashboard](https://django-datta-able-pro.appseed-srv1.com/)** (PRO version). Datta Able Pro is a premium Bootstrap 5 Admin Dashboard featuring over 800 components, 20 example pages and 10 fully customized plugin written in Vanilla Javascript. It is based on the latest version of Bootstrap.

> Originally coded by [Iman Karimi](https://github.com/imankarimi), actively supported by [AppSeed](https://appseed.us/) via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br>

**Links & Resources**

- [Django Datta Able Dashboard PRO](https://appseed.us/admin-dashboards/django-dashboard-dattaable-pro) - Starter that uses the same UI Kit
- [Django Datta Able Dashboard PRO](https://django-datta-able-pro.appseed-srv1.com/) - LIVE Demo

<br />

## Why Django Admin Datta Able PRO?

- UI Kit: **Datta Able Dashboard** (PRO version) provided by **CodedThemes**
- New fresh look
- Responsive mobile interface
- Useful admin home page
- Minimal template overriding
- Easy integration

<br />

![Django Admin Datta Able Professional - Template project for Django provided by AppSeed.](https://appseed-147a1.kxcdn.com/static/apps/django-dashboard-dattaable-pro/django-dashboard-dattaable-pro-screen.png)

<br>

## Installation

```bash
$ pip install git+https://github.com/app-generator/priv-django-admin-datta-pro.git
# or
$ easy_install git+https://github.com/app-generator/priv-django-admin-datta-pro.git
```

* Add 'admin_dattaable' application to the INSTALLED_APPS setting of your Django project `settings.py` file (note it should be before 'django.contrib.admin'):

```python
INSTALLED_APPS = (
    'admin_dattaable.apps.AdminDattaableConfig',
    'django.contrib.admin',
    # ...
)
```

* All programs you add in **INSTALLED_APPS** should look like this: **APP_NAME.apps.APP_NAMEConfig**.

> In this feature, we considered that each App can have its own icon, so we ask users to use this feature according to the method. Also in apps.py of each program according to the example add the icon field in the corresponding class. You can go **[here](https://feathericons.com/)** to use more icons


```python
from django.apps import AppConfig

class APP_NAMEConfig(AppConfig):
    name = 'APP_NAME'
    icon = 'ICON_CLASS'  # for example: icon = 'feather icon-box'
```

* Make sure ``django.template.context_processors.request`` context processor is enabled in `settings.py` (Django 1.8+ way):

```python
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                # ...
                'django.template.context_processors.request',
                # ...
            ],
        },
    },
]
```

:warning: **Warning!!**
* Before Django 1.8 you should specify context processors different way. Also use ``django.core.context_processors.request`` instead of ``django.template.context_processors.request``.

```python
from django.conf import global_settings

TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + (
    'django.core.context_processors.request',
)
```

* Collect static if you are in production environment:

```bash
$ python manage.py collectstatic
```

* Clear your browser cache

<br />

### Django Recovery Password

To use Django recovery password you have to add following url to `MAIN_APP/urls.py`:
```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('account/', include('django.contrib.auth.urls'))
    # ...
]
```

* Please add your email information in `settings.py` before using:
```python
EMAIL_HOST = 'EMAIL_HOST'
EMAIL_FROM = 'EMAIL_FROM'
EMAIL_HOST_USER = 'EMAIL_HOST_USER'
EMAIL_HOST_PASSWORD = 'EMAIL_HOST_PASSWORD'
EMAIL_PORT = 'EMAIL_PORT'
EMAIL_USE_TLS = 'EMAIL_USE_TLS'
EMAIL_TIMEOUT = 'EMAIL_TIMEOUT'
```

* Access the `Recovery Password` section in the browser: `http://YOUR_DOMAIN/account/password_reset/`

![Django Admin Datta Able PRO - Recovery Password.](https://user-images.githubusercontent.com/51070104/140062868-c2dfc524-ad37-4444-be42-3ef6c902d107.png)

<br />

## Start the app

```bash
# Set up the database
$ python manage.py makemigrations
$ python manage.py migrate

# Create the superuser
$ python manage.py createsuperuser

# Start the application (development mode)
$ python manage.py runserver # default port 8000
```

* Access the `admin` section in the browser: `http://127.0.0.1:8000/`

<br />

## Screenshots

> Django Admin Datta Able PRO - Dashboard Page

![Django Admin Datta Able PRO - Dashboard Page.](https://user-images.githubusercontent.com/51070104/140063261-b8ec6dd6-e0ea-4835-8420-2bf9b2778d7a.png) 

<br>

> Django Admin Datta Able PRO - Admin Users Page
 
![Django Admin Datta Able PRO - Admin Users Page](https://user-images.githubusercontent.com/51070104/140063348-cf53c746-5f1c-4c36-8f18-e7a9c793305e.png)

<br>

> Django Admin Datta Able PRO - Admin Users Details

![Django Admin Datta Able PRO - Admin Users Details](https://user-images.githubusercontent.com/51070104/140063460-f74153b5-2ba1-45a0-b67f-ba2efca1858e.png)

<br />

---
[Django Admin Datta Able PRO](https://appseed.us/admin-dashboards/django-dashboard-dattaable-pro) - Provided by **[AppSeed](https://appseed.us/)**

