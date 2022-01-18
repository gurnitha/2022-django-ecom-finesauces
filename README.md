# 2022-django-ecom-finesauces
This is my exercise based on DJANGO MADE EASY 2ND EDITION by PETER VOUGHT
https://github.com/gurnitha/2022-django-ecom-finesauces



### 1. INITIAL SETUP
--------------------

#### 1.1 Setting up django project with postgres database 

        STEPS:

        1. Makesure python is installed
           λ python --version
             Python 3.9.5 
        2. Makesure postgres is installed
           λ postgres --version
             postgres (PostgreSQL) 13.0
        3. Create database using postgres
           hp=# CREATE DATABASE django_ecom_finesauces_2022;
           CREATE DATABASE
        4. Install postgres driver
           (finesauces) λ pip install psycopg2-binary
        5. Create github repository
        6. In your workspace create folder with
           the same name with the Github repository
           '2022-django-ecom-finesauces'
        7. Go to inside that folder
        	cd 2022-django-ecom-finesauces
        8. Clone Github repository
           λ git clone git@github.com:gurnitha/2022-django-ecom-finesauces.git
        9. Create virtual environment
           λ python -m venv venv39327 --promp finesauces
        10. Activate virtualenv
           λ venv39327\scripts\activate
        11. Install django
           (finesauces) λ pip install django==3.2.7
        12. Create requirements.txt file
           (finesauces) λ pip freeze r > requirements.txt      

        modified:   README.md
        new file:   requirements.txt



### 2. STARTING ECOMMERCE FINESAUCES PROJECT
--------------------------------------------


#### 2.1 Create django project

        STEPS:

        1. Create django project inside the root
           folder
           (finesauces) λ django-admin startproject config .
        2. Checking current project structure
           $ tree -L 2
           .
           ├── 2022-django-ecom-finesauces
           │   ├── LICENSE
           │   ├── README.md
           │   ├── config
           │   ├── manage.py
           │   └── requirements.txt
           └── venv39327
        3. Run the server  

        modified:   README.md
        new file:   config/__init__.py
        new file:   config/asgi.py
        new file:   config/settings.py
        new file:   config/urls.py
        new file:   config/wsgi.py
        new file:   manage.py


#### 2.2 Updating project settings with django-environ

        STEPS:

        1. Install django-environ
           (finesauces) λ pip install django-environ
        2. Create .env file: config/.env
           (finesauces) λ touch config\.env
        3. Declare your environment variables in .env
        4. Initialise environ on settings.py 
        5. Add SECRET_KEY varable to setting.spy
        6. Add db configuration variable in settings.py
        7. Test it out :)
        8. Run initial migration
           (finesauces) λ python manage.py migrate
        9. Checking the created table in db
           (finesauces) λ psql -h localhost
           hp=# \c db_name
           db_name=# \dt

                          List of relations
         Schema |            Name            | Type  | Owner
        --------+----------------------------+-------+-------
         public | auth_group                 | table | hp
         public | auth_group_permissions     | table | hp
         public | auth_permission            | table | hp
         public | auth_user                  | table | hp
         public | auth_user_groups           | table | hp
         public | auth_user_user_permissions | table | hp
         public | django_admin_log           | table | hp
         public | django_content_type        | table | hp
         public | django_migrations          | table | hp
         public | django_session             | table | hp
        (10 rows)

        db_name=# \q

        modified:   README.md
        modified:   config/settings.py



### 3. CREATING LISTINGS APPLICATION
------------------------------------


#### 3.1 Create listings app inside apps folder

        STEPS:

        1. Create folders
           (finesauces) λ mkdir apps\listings
        2. Create listings app
           (finesauces) λ django-admin startapp listings apps\listings
        3. Activating listings application
           - modify apps.py
           - install listings in settings.py
        4. Test it out :)
        5. Update requirements.txt file
        6. Project structure

.
            ├── 2022-django-ecom-finesauces
            │   ├── LICENSE
            │   ├── README.md
            │   ├── apps
            │   │   └── listings
            │   │       ├── __init__.py
            │   │       ├── __pycache__
            │   │       ├── admin.py
            │   │       ├── apps.py
            │   │       ├── migrations
            │   │       ├── models.py
            │   │       ├── tests.py
            │   │       └── views.py
            │   ├── config
            │   │   ├── asgi.py
            │   │   ├── settings.py
            │   │   ├── urls.py
            │   │   └── wsgi.py
            │   ├── db.sqlite3
            │   ├── manage.py
            │   └── requirements.txt
            └── venv39327

        modified:   README.md
        new file:   apps/listings/__init__.py
        new file:   apps/listings/admin.py
        new file:   apps/listings/apps.py
        new file:   apps/listings/migrations/__init__.py
        new file:   apps/listings/models.py
        new file:   apps/listings/tests.py
        new file:   apps/listings/views.py
        modified:   config/settings.py
        modified:   requirements.txt


#### 3.2 Designing listings models (Category and Product models)

        STEPS:

        1. Create Category model
        2. Create Product model with ManyToOne relationship
           with Category
        3. Install Pillow
           (finesauces) λ pip install pillow
        4. Creating and applying migrations
           (finesauces) λ python manage.py makemigrations
           (finesauces) λ python manage.py migrate
        5. Check the result :)

           (finesauces) λ psql -h localhost
           ...

           hp=# \c db_name
           You are now connected to database "db_name" as user "hp".
           db_name=# \dt
                             List of relations
            Schema |            Name            | Type  | Owner
           --------+----------------------------+-------+-------
            ...
            public | listings_category          | table | hp
            public | listings_product           | table | hp
          (12 rows)

        6. Creating administration site

           6.1 Creating superuser   
           6.2 Accessing administration site
           6.3 Adding models to the administration site

        7. Customizing how models are displayed

        8. Serving image files
        9. Adding some items from admin panel
        10. Update requirements.txt file

        modified:   README.md
        modified:   apps/listings/admin.py
        new file:   apps/listings/migrations/0001_initial.py
        modified:   apps/listings/models.py
        modified:   config/settings.py
        modified:   config/urls.py
        new file:   media/products/komodo_dragon.jpg
        new file:   media/products/orange_habanero.jpg
        modified:   requirements.txt        

  


























































































































































