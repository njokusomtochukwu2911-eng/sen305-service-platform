# VUA SEN305 – Enterprise Service Request and Maintenance Platform

## Lab Session 2: Client-Server Model, HTTP and Django MVT Foundation

This repository contains the Django project created during Lab Session 2 of VUA-SEN305 Web Application Development Practical.

### Structure

```
sen305-service-platform/
├── backend/                 # Django project
│   ├── config/              # Project settings and root URLconf
│   ├── core/                # Core application (views, templates, static)
│   ├── templates/           # Project-level templates (404.html)
│   ├── manage.py
│   └── requirements.txt
├── frontend/
├── docs/
├── infrastructure/
├── .gitignore
└── README.md
```

### Quick start

```bash
cd backend
python -m venv ../.venv
source ../.venv/bin/activate   # or Windows equivalent
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Open http://127.0.0.1:8000/

### Pages

- `/` – Home
- `/about/` – About (roles list)
- `/contact/` – Contact details
- `/workflow/` – Workflow stages
- Any other path returns 404

### Notes

- Static files are served from `core/static/core/css/styles.css`
- Navigation uses named URLs and marks the active page with `aria-current="page"`
- Database for this session is SQLite (`db.sqlite3` is gitignored)
