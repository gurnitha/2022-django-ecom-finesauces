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