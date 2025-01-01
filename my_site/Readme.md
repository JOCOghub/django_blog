Create a Virtual Environment:

1. /opt/homebrew/opt/python@3.13/bin/python3.13 -m venv myenv

Activate the Virtual Environment 2. source myenv/bin/activate

3. pip install django

verify: python -m django --version

4. Create Project: django-admin startproject <name>

5. CD into new folder and make new app :`python3 manage.py startapp <app_name>`

6. Register the New App
Open your settings.py file.
Add the new app to the INSTALLED_APPS list:
python
Copy code
INSTALLED_APPS = [
    # other apps...
    'blog',  # Add your new app here
]
CD to the same folder as the manage.py file then...
6. Run `python3 manage.py runserver`
----------------------------------------------------------------------------------
Settings.py

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [
            BASE_DIR / "templates" #ADD GlOBAL FOLDERS HERE 
        ],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
 
ADD STATIC FILES CODE  
STATICFILES_DIRS = [
    BASE_DIR / "static"
]

