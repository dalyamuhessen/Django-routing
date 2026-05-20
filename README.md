# First Django Project
A beginner Django project focused on practicing project setup, app creation, routing, and returning HTTP responses.
---
## Objectives
- Practice setting up a new Django project
- Practice setting up a new Django app
- Practice routing in Django
- Familiarity with views and how to return a response
---
## Project Structure

```
django_project/
├── django_project/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── some_app/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── db.sqlite3
└── manage.py
```

## Routes

| Method | URL | Description |
|--------|-----|-------------|
| GET | `/` | Redirects to `/blogs` |
| GET | `/blogs` | Displays placeholder list of all blogs |
| GET | `/blogs/new` | Displays placeholder new blog form |
| GET | `/blogs/create` | Redirects to `/` |
| GET | `/blogs/<number>` | Displays placeholder for blog by number |
| GET | `/blogs/<number>/edit` | Displays placeholder edit page for blog |
| GET | `/blogs/<number>/delete` | Redirects to `/blogs` |
| GET | `/blogs/json` | returns a JSON response |

---

## Views Summary

| View Function | Route | Action |
|---------------|-------|--------|
| `root` | `/` | Redirects to `/blogs` |
| `index` | `/blogs` | Returns placeholder string |
| `new` | `/blogs/new` | Returns placeholder string |
| `create` | `/blogs/create` | Redirects to `/` |
| `show` | `/blogs/<number>` | Returns string with blog number |
| `edit` | `/blogs/<number>/edit` | Returns string with blog number |
| `destroy` | `/blogs/<number>/delete` | Redirects to `/blogs` |
| `blog_json` | `/blogs/json` | Returns JsonResponse |

---
## Notes

- Route parameters use `<int:number>` to capture numeric URL segments
- `blogs/json/` is defined **before** `blogs/<int:number>/` in `urls.py` to avoid pattern conflicts
- The `/favicon.ico` 404 in the console is normal and can be ignored
