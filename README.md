# Django App Example

A simple Django application example.

## Setup

1.  Clone the repository.
2.  Create a virtual environment and activate it.
3.  Install dependencies:

```bash
pip install -r requirements.txt
```

## Environment Variables

| Variable          | Description                          | Default                                                   |
| ----------------- | ------------------------------------ | --------------------------------------------------------- |
| `DJANGO_SECRET_KEY` | Django secret key for cryptographic signing | `django-insecure-...` (dev-only fallback) |

## Running

```bash
python manage.py runserver
```

## Creating a New App

Apps are stored under `server/apps/`. To create a new app:

```bash
cd server/apps
python ../../manage.py startapp <app_name>
```

Then add `'server.apps.<app_name>'` to `INSTALLED_APPS` in `server/settings.py`.
