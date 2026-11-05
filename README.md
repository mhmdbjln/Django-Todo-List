# Django To-Do List

A personal task-management web application built with Django. The interface is primarily Persian-language and supports authenticated, per-user task management.

## Features

- Custom user model with email-based login and a required mobile phone number.
- User registration, login, and logout.
- Create, edit, delete, and complete tasks.
- Task descriptions, due dates, and low/medium/high priority levels.
- Views for daily tasks, overdue tasks, upcoming seven-day tasks, and all tasks.
- Task ownership associated with the authenticated user.
- JavaScript Fetch API requests and JSON responses for task actions.
- Django admin integration.

## Technology

- Python
- Django 4.2.7
- SQLite
- HTML, CSS, and JavaScript

## Setup

Use a Python version compatible with Django 4.2.7. From the directory containing `manage.py`:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Open http://127.0.0.1:8000/ in your browser.

Create an administrator account when needed:

```bash
python manage.py createsuperuser
```

The admin site is available at http://127.0.0.1:8000/admin/.

## Security and repository notes

- The supplied development database is not included. Run migrations to create a fresh local database.
- The original development settings include DEBUG mode and a development SECRET_KEY. Do not deploy this snapshot to production as-is.
- The application uses Django's built-in ORM and views. Django REST Framework appeared in the original dependency list but is not used by the inspected application code.
- Do not commit passwords, session data, local databases, `.env` files, or personal information.

## License

No license has been specified.
