# **[Django Admin Datta PRO](https://appseed.us/product/datta-able-pro/django/)**

**Django** starter styled with **[Datta Able Dashboard PRO](https://appseed.us/product/datta-able-pro/django/)**, a premium `Bootstrap 5` design from [CodedThemes](https://codedthemes.com/?ref=appseed).
The product is designed to deliver the best possible user experience with highly customizable feature-rich pages. 

> 👉 **NOTE**: This product `requires a License` in order to access the theme:

**Private REPO**: `git+https://github.com/app-generator/priv-django-admin-datta-pro`

<br />

## Features: 

- **UI Kit**: Datta Able PRO `v1.0.2` by CodedThemes
- [Django Able PRO](https://appseed.us/product/datta-able-pro/django/) - `Product` that uses the library
  - `Features`: Fully-configured, `CI/CD` via Render
- **Sections Covered**: 
  - `Admin Section`, reserved for `superusers`
  - `All pages` managed by `Django.contrib.AUTH`
  - `Registration` page
  - `Misc pages`: colors, icons, typography, blank-page 

<br />

![Datta Able PRO - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/170474361-a58da82b-fff9-4a59-81a8-7ab99f478f48.png)

<br />

## Why `Django Admin Datta PRO`

- Modern [Bootstrap 5](https://www.admin-dashboards.com/bootstrap-5-templates/) Design
- `Responsive Interface`
- `Minimal Template` overriding
- `Easy integration`

Datta Able Dashboard comes with error/bug-free, well structured codebase that renders nicely in all major browsers and devices. 

<br />

## How to use it

<br />

> **Install the package** via `PIP` 

```bash
$ pip install git+https://github.com/app-generator/priv-django-admin-datta-pro.git
```

<br />

> Add `admin_datta_pro` application to the `INSTALLED_APPS` setting of your Django project `settings.py` file (note it should be before `django.contrib.admin`):

```python
    INSTALLED_APPS = (
        ...
        'admin_datta_pro.apps.AdminDattaProConfig',
        'django.contrib.admin',
    )
```

<br />

> Add `LOGIN_REDIRECT_URL` and `EMAIL_BACKEND` of your Django project `settings.py` file:

```python
    LOGIN_REDIRECT_URL = '/'
    # EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
    EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
```

<br />

> Add `admin_datta_pro` urls in your Django Project `urls.py` file

```python
    from django.urls import path, include

    urlpatterns = [
        ...
        path('', include('admin_datta_pro.urls')),
    ]
```

<br />

> **Collect static** if you are in `production environment`:

```bash
$ python manage.py collectstatic
```

<br />

> **Start the app**

```bash
$ # Set up the database
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Create the superuser
$ python manage.py createsuperuser
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
```

Access the `admin` section in the browser: `http://127.0.0.1:8000/`

<br />

## How to Customize 

When a template file is loaded in the controller, `Django` scans all template directories starting from the ones defined by the user, and returns the first match or an error in case the template is not found. 
The  theme used to style this starter provides the following files: 

```bash
# This exists in ENV: LIB/admin_datta_pro
< UI_LIBRARY_ROOT >                      
   |
   |-- templates/                     # Root Templates Folder 
   |    |          
   |    |-- accounts/       
   |    |    |-- auth-signin.html     # Sign IN Page
   |    |    |-- auth-signup.html     # Sign UP Page
   |    |
   |    |-- includes/       
   |    |    |-- footer.html          # Footer component
   |    |    |-- sidebar.html         # Sidebar component
   |    |    |-- navigation.html      # Navigation Bar
   |    |    |-- scripts.html         # Scripts Component
   |    |
   |    |-- layouts/       
   |    |    |-- base.html            # Masterpage
   |    |    |-- base-auth.html       # Masterpage for Auth Pages
   |    |
   |    |-- pages/       
   |         |-- index.html           # INDEX page
   |         |-- landingpage.html     # Sample LP
   |         |-- *.html               # All other pages
   |    
   |-- ************************************************************************
```

When the project requires customization, we need to copy the original file that needs an update (from the virtual environment) and place it in the template folder using the same path. 

For instance, if we want to customize the `index.html` these are the steps:

- `Step 1`: create the `templates` DIRECTORY inside your app 
- `Step 2`: configure the project to use this new template directory
  - Edit `settings.py` TEMPLATES section 
- `Step 3`: copy the `index.html` from the original location (inside your ENV) and save it to the `YOUR_APP/templates` DIR
  - Source PATH: `<YOUR_ENV>/LIB/admin_datta_pro/templates/pages/index.html`
  - Destination PATH: `YOUR_APP/templates/pages/index.html`
- Edit the `index` page (Destination PATH)    

At this point, the default version of the `index.html` shipped in the library is ignored by Django.

In a similar way, all other files and components can be customized easily.

<br />

---
**[Django Admin Datta PRO](https://appseed.us/product/datta-able-pro/django/)** - Modern Admin Interface provided by **[AppSeed](https://appseed.us/)**
