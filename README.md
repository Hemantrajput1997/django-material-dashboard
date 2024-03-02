# [Django Material Dashboard](https://appseed.us/product/material-dashboard/django/)

Open-source **[Django Dashboard](https://appseed.us/admin-dashboards/django/)** crafted on top of **Material Dashboard**, an open-source `Bootstrap 5` design from `Creative-Tim`.
The product is designed to deliver the best possible user experience with highly customizable feature-rich pages. `Material Dashboard` has an easy and intuitive responsive design, whether viewed on retina screens or laptops.

- 👉 [Django Material Dashboard](https://appseed.us/product/material-dashboard/django/) - `Product page`
- 👉 [Django Material Dashboard](https://django-material-dash2.onrender.com) - `LIVE Demo`

<br />

## Features

> `Have questions?` Contact **[Support](https://appseed.us/support/)** (Email & Discord) provided by **AppSeed**

| Free Version                          | [PRO Version](https://appseed.us/product/material-dashboard2-pro/django/)    | 🚀 Custom - $4,999         |  
| --------------------------------------| --------------------------------------| --------------------------------------|
| ✓ **Django 4.2.9**                    | **Everything in Free**, plus:                                                                  | **Everything in PRO**, plus:         |
| ✓ Best Practices                      | ✅ **Premium Bootstrap 5 Design**                                                              | ✅ **1mo Custom Development**       | 
| ✓ Bootstrap 4, `Material` Design      | ✅ `OAuth` Google, GitHub                                                                      | ✅ **Team**: PM, Developer, Tester  |
| ✓ `Docker`                            | ✅ `API`, **[Charts](https://django-material-dash2-pro.onrender.com/charts/)**                 | ✅ Weekly Sprints                   |
| -                                     | ✅ **[DataTables](https://django-material-dash2-pro.onrender.com/tables/)** (Filters, Export)   | ✅ Technical SPECS                  |
| -                                     |✅ **Celery**                                                                                   | ✅ Documentation                    |
| -                                     | ✅ **Media Files Manager**                                                                     | ✅ **30 days Delivery Warranty**    |
| -                                     | ✅ **Extended User Profiles**                                                                  |  -                                   |
| -                                     | ✅ `Private REPO Access`                                                                       |  -                                   |
| -                                     | ✅ **PRO Support** - [Email & Discord](https://appseed.us/support/)                            |  -                                   |
| -                                     | ✅ Deployment Assistance                                                                       |  -                                   |
| ------------------------------------  | ------------------------------------                                                           | ------------------------------------|
| ✓ [LIVE Demo](https://django-datta-able.appseed-srv1.com/)  | 🚀 [LIVE Demo](https://django-material-dash2-pro.onrender.com/) | 🛒 `Order`: **[$4,999](https://appseed.gumroad.com/l/rocket-package)** (GUMROAD) |   


![Material Dashboard - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/169301658-6cf27993-c451-4cd4-9ffa-2968b8981167.png)

<br />

## Manual Build 

> 👉 Download the code  

```bash
$ git clone https://github.com/app-generator/django-material-dashboard.git
$ cd django-material-dashboard
```

<br />

> 👉 Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```

<br />

> 👉 Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> 👉 Create the Superuser

```bash
$ python manage.py createsuperuser
```

<br />

> 👉 Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

## Codebase structure

The project is coded using a simple and intuitive structure presented below:

```bash
< PROJECT ROOT >
   |
   |-- core/                            
   |    |-- settings.py                  # Project Configuration  
   |    |-- urls.py                      # Project Routing
   |
   |-- home/
   |    |-- views.py                     # APP Views 
   |    |-- urls.py                      # APP Routing
   |    |-- models.py                    # APP Models 
   |    |-- tests.py                     # Tests  
   |    |-- templates/                   # Theme Customisation 
   |         |-- includes                # 
   |              |-- custom-footer.py   # Custom Footer      
   |     
   |-- requirements.txt                  # Project Dependencies
   |
   |-- env.sample                        # ENV Configuration (default values)
   |-- manage.py                         # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

## How to Customize 

When a template file is loaded, `Django` scans all template directories starting from the ones defined by the user, and returns the first match or an error in case the template is not found. 
The theme used to style this starter provides the following files: 

```bash
# This exists in ENV: LIB/admin_material
< UI_LIBRARY_ROOT >                      
   |
   |-- templates/                     # Root Templates Folder 
   |    |          
   |    |-- accounts/       
   |    |    |-- login.html           # Sign IN Page
   |    |    |-- register.html        # Sign UP Page
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
   |         |-- index.html           # Dashboard Page
   |         |-- profile.html         # Profile Page
   |         |-- *.html               # All other pages
   |    
   |-- ************************************************************************
```

When the project requires customization, we need to copy the original file that needs an update (from the virtual environment) and place it in the template folder using the same path. 

> For instance, if we want to **customize the footer.html** these are the steps:

- ✅ `Step 1`: create the `templates` DIRECTORY inside the `home` app
- ✅ `Step 2`: configure the project to use this new template directory
  - `core/settings.py` TEMPLATES section
- ✅ `Step 3`: copy the `footer.html` from the original location (inside your ENV) and save it to the `home/templates` DIR
  - Source PATH: `<YOUR_ENV>/LIB/admin_material/template/includes/footer.html`
  - Destination PATH: `<PROJECT_ROOT>home/templates/includes/footer.html`

> To speed up all these steps, the **codebase is already configured** (`Steps 1, and 2`) and a `custom footer` can be found at this location:

`home/templates/includes/custom_footer.html` 

By default, this file is unused because the `theme` expects `footer.html` (without the `custom-` prefix). 

In order to use it, simply rename it to `footer.html`. Like this, the default version shipped in the library is ignored by Django. 

In a similar way, all other files and components can be customized easily.

<br />

## CSS Styling 

The UI can be customized via the SCSS file. This setup was tested using: 

- `Node` v16.15.0
- `Yarn` 1.22.18 
- `Gulp` CLI version: `2.3.0`, Local version: `4.0.2`

```bash
$ cd static
$ yarn                                       # Install Modules 
$ vi scss/material-dashboard/_variables.scss # Edit primary, secondary colors
$ gulp                                       # Regenerate CSS files   
```

> NOTE, once the CSS files are successfully regenerated, force a hard refresh in the browser (Shift + F5 in Chrome).

The relevant lines in `_variables.scss` are highlighted below: 

```SCSS
// _variables.scss, LINES 56 -> 63
$primary:       #e91e63 !default;   // EDIT & Recompile SCSS
$secondary:     #7b809a !default;   // EDIT & Recompile SCSS
$info:          #1A73E8 !default;   // EDIT & Recompile SCSS
$success:       #4CAF50 !default;   // EDIT & Recompile SCSS
$warning:       #fb8c00 !default;   // EDIT & Recompile SCSS
$danger:        #F44335 !default;   // EDIT & Recompile SCSS
$light:         $gray-200 !default; // EDIT & Recompile SCSS
$dark:          $h-color !default;  // EDIT & Recompile SCSS
```

<br />

## Deploy on [Render](https://render.com/)

- Create a Blueprint instance
  - Go to https://dashboard.render.com/blueprints this link.
- Click `New Blueprint Instance` button.
- Connect your `repo` which you want to deploy.
- Fill the `Service Group Name` and click on `Update Existing Resources` button.
- After that your deployment will start automatically.

At this point, the product should be LIVE.

<br />

## [PRO Version](https://appseed.us/product/material-dashboard2-pro/django/)   

This design is a pixel-perfect [Bootstrap 5](https://www.admin-dashboards.com/bootstrap-5-templates/) Dashboard with a fresh, new design inspired by Google's Material Design. `Material Dashboard 2 PRO` is built with over 300 frontend individual elements, like buttons, inputs, navbars, nav tabs, cards, or alerts, giving you the freedom of choosing and combining.

> Features: 

- `Up-to-date dependencies`
- Database: `SQLite`, PgSQL, MySql
- **Authentication**
  - `Session-Based authentication`
  - `Social Login`: **Github** & **Google**
- **User Extended profile**
- **API** via DRF
- DataTables
- Charts
- Celery
- File Manager
- i18n (internationalization) 
- `Docker`

![Material Dashboard 2 Pro](https://user-images.githubusercontent.com/51070104/211141418-6b7886eb-6fb3-433e-91c9-2895c086099a.png)

<br />

---
[Django Material Dashboard](https://appseed.us/product/material-dashboard/django/) - Free Starter provided by **[AppSeed](https://appseed.us/)**
