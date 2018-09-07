# README #

# Instaliation process of Glasschair #
* Install Python (version>3)
* Install Pip. (Python Package Installer)
* Install virtualenv
* Create a new virtualenv

#### Cerate a new virtualenv ####
```bash
 virtualenv yourenv -p python3.6
 ```
 
 #### Activate virtualenv ####
 ```
 source bin/activate
 ```
 
 #### Install Requiremets.text ####
 
 ```
 pip install -r requirements.text
 ```
 
 ### Run Glasschair (Go to Project Root folder and RUN) ###
 * Run Migrate to create the database table 
 ```
 	python manage.py migrate
 ```
 
  * Create super user to access Django Admin panel
 ```
 	python manage.py createsuperuser
 ```
 
 * RUN
 ```
 	python manage.py runserver
 ```
 
 ## Apache configuration  ##
 
 * Update apache config
 
 ```bash 
 		WSGIDaemonProcess glasschair python-path=/var/www/glasschair-website/src python-home=/var/www/env/lib/python3.5/site-packages
        WSGIProcessGroup glasschair
        WSGIScriptAlias / /var/www/glasschair-website/src/glasschair/wsgi.py
 ```
 
 
