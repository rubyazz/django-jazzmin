# Django jazzmin (Jazzy Admin)

## Installation
```
pip install django-jazzmin
```

## Setup & configuration

```python
# settings.py

INSTALLED_APPS = [
    # Place before admin
    'jazzmin',
    'django.contrib.admin',
    [...]
]


JAZZMIN_SETTINGS = {
    # Choose from black, black-light, blue, blue-light, green, green-light, purple, purple-light,
    # red, red-light, yellow, yellow-light
    'skin': 'blue',

    # title of the window
    'site_title': 'Django Admin',

    # Title on the login screen
    'site_header': 'Django',

    # square logo to use for your site, must be present in static files, used for favicon and brand on top left
    'site_logo': 'admin/dist/img/default-log.svg',

    # Welcome text on the login screen
    'welcome_sign': 'Welcome big dog',

    # Copyright on the footer
    'copyright': 'Acme Ltd',

    # Wether to aut expand the menu
    'navigation_expanded': True,

    # The model admin to search from the search bar, search bar omitted if excluded
    'search_model': 'profiles.Profile',

    # Field name on user model that contains avatar image
    'user_avatar': 'avatar',

    # Hide these apps when generating menu
    'hide_apps': ['auth'],

    # Hide these models when generating menu
    'hide_models': ['auth.user'],

    # List of apps to base menu ordering off of
    'order_with_respect_to': ['first_app', 'second_app'],

    # Custom links to append to app groups, keyed on app name
    'custom_links': {
        'first_app': [
            {'name': 'Custom link', 'url': '/', 'icon': 'fa-user', 'permissions': []}
        ]
    },

    'icons': {
        'auth': 'fa-people',
        'auth.user': 'fa-user',
    }
}
```

## Screenshots

## Login view
![login](docs/login.png)

## Dashboard
![dashboard](docs/dashboard.png)

## List view
![table list](docs/list_view.png)

## Detail view
![form page](docs/detail_view.png)

# Thanks
- Original Package https://github.com/wuyue92tree/django-adminlte-ui
