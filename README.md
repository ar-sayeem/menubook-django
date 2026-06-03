# 🍽️ MenuBook — Django Menu & Reservation System

A simple Django web application for managing restaurant menus and table reservations.

---

## 📋 Features

- 📖 **Menu Display** — Browse all menu items with names, descriptions, and prices
- 🔍 **Menu Item Detail** — Click on any item to view its full details
- 📅 **Table Reservations** — Submit reservation requests via a form
- 🗄️ **SQLite3 Database** — All data is stored locally using Django's default SQLite3 database
- 🔧 **Admin Panel** — Manage menu items and reservations via Django's built-in admin interface

---

## 🛠️ Tech Stack

- **Backend:** Python 3.10+, Django
- **Database:** SQLite3
- **Frontend:** HTML, CSS (Django Templates)
- **Package Manager:** Pipenv

---

## 🚀 Getting Started

### ✅ Prerequisites

Make sure you have the following installed before starting:

- [Python 3.10+](https://www.python.org/downloads/)
- [Pipenv](https://pipenv.pypa.io/en/latest/)

To install Pipenv:
```bash
pip install pipenv
```

---

### 📦 Installation

**Step 1 — Clone the repository**
```bash
git clone https://github.com/ar-sayeem/menubook-django.git
```

**Step 2 — Go to the project root folder**
```bash
cd menubook-django
```

**Step 3 — Install dependencies using Pipenv**
```bash
pipenv install
```

**Step 4 — Activate the virtual environment**
```bash
pipenv shell
```
> ⚠️ You should see `(menubook-django-...)` appear in your terminal. Always activate this before running any commands.

**Step 5 — Navigate into the Django project folder**
```bash
cd menubook
```

**Step 6 — Apply database migrations**
```bash
python manage.py migrate
```

**Step 7 — Create an admin superuser**
```bash
python manage.py createsuperuser
```
> You will be prompted to enter a username, email, and password.

**Step 8 — Run the development server**
```bash
python manage.py runserver
```

**Step 9 — Open in your browser**
```
http://127.0.0.1:8000/app/menu/
```

---

### 🔁 Every Time You Reopen the Project

When you close and reopen your terminal, always run these first:

```bash
cd menubook-django
pipenv shell
cd menubook
python manage.py runserver
```

---

## 🌐 URL Routes

| URL | Description |
|-----|-------------|
| `/app/menu/` | View all menu items |
| `/app/menu_item/<id>` | View details of a specific menu item |
| `/app/reservation` | Submit a table reservation |
| `/admin/` | Django admin panel |

---

## 🗂️ Project Structure

```
menubook-django/
├── menubook/                   # Django project configuration
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── menubookapp/                # Main application
│   ├── migrations/             # Database migration files
│   ├── templates/              # HTML templates
│   │   ├── index.html
│   │   ├── menu.html
│   │   ├── menu_item.html
│   │   └── ...
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── manage.py
├── Pipfile
├── Pipfile.lock
└── .gitignore
```

---

## 🗄️ Database Models

### MenuItem
| Field | Type | Description |
|-------|------|-------------|
| name | CharField | Name of the menu item |
| price | IntegerField | Price of the item |

### Reservations
| Field | Type | Description |
|-------|------|-------------|
| first_name | CharField | Guest's first name |
| last_name | CharField | Guest's last name |
| guest_Count | IntegerField | Number of guests |
| reservationTime | DateField | Auto-set on creation |
| comments | CharField | Special requests or notes |

---

## 🔧 Admin Panel

To manage menu items and reservations, go to:
```
http://127.0.0.1:8000/admin/
```
Log in with the superuser credentials you created in Step 7.

---

## 📝 .gitignore

Make sure your `.gitignore` includes:
```
__pycache__/
*.pyc
db.sqlite3
.venv/
*.docx
Thumbs.db
.DS_Store
```

---

## 👤 Author

**Ar Sayeem**
- GitHub: [@ar-sayeem](https://github.com/ar-sayeem)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
