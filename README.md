# Django App Example

A simple Django application example.

## Prerequisites

- Python >= 3.12
- [Poetry](https://python-poetry.org/docs/#installation)

## Setup

1.  Clone the repository.

2.  Install dependencies:

```bash
poetry install
```

3.  Copy environment configuration:

```bash
cp config/.env.example config/.env
```

4.  Edit `config/.env` and set your `SECRET_KEY` and database credentials.

5.  Run database migrations:

```bash
poetry run python manage.py migrate
```

## Running

```bash
poetry run python manage.py runserver
```

## Creating a New App

Apps are stored under `server/apps/`. To create a new app:

```bash
mkdir -p server/apps
cd server/apps
poetry run python ../../manage.py startapp <app_name>
```

Then add `'server.apps.<app_name>'` to `INSTALLED_APPS` in `server/settings.py`.

## Environment Variables

| Variable       | Description                    | Default |
|---------------|--------------------------------|---------|
| `SECRET_KEY`  | Django secret key              | (required) |
| `DB_NAME`     | PostgreSQL database name       | `myapp` |
| `DB_USER`     | PostgreSQL user                | `postgres` |
| `DB_PASSWORD` | PostgreSQL password            | `dev` |
| `DB_HOST`     | PostgreSQL host                | `localhost` |
| `DB_PORT`     | PostgreSQL port                | `5432` |
