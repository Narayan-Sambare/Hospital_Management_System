# Hospital Management System (Django)

A simple **Hospital Management System** built with **Django** to manage **Doctors**, **Patients**, and **Appointments**, along with a **Contact/Query** module (read/unread) and an **Admin Dashboard**.

## Features

- **Admin login** (staff users only)
- **Dashboard** with counts (Doctors / Patients / Appointments)
- **Doctors**
  - Add / View / Edit / Delete
- **Patients**
  - Add / View / Edit / Delete
- **Appointments**
  - Create / View / Delete (linked to Doctor + Patient)
- **Contact / Queries**
  - Public “Contact Us” form
  - Admin can view **Unread** and **Read** queries

## Tech Stack

- **Backend**: Python, Django (project generated with Django **3.2.8**)
- **Database**: SQLite (`db.sqlite3`)
- **Frontend**: Django Templates, Bootstrap, jQuery (static files included)

## Project Structure

- `HospitalManagementSystem/` – Django project config (settings/urls/wsgi/asgi)
- `hospitals/` – Main app (models, views, templates, static)
- `db.sqlite3` – SQLite database (local dev)

## Main Routes

- `/` – Home
- `/about/` – About
- `/services` – Services
- `/contact` – Contact form
- `/login` – Admin login (custom page)
- `/admin_home` – Admin dashboard
- `/admin/` – Django admin panel

CRUD routes (admin only):
- `/add_doctor`, `/view_doctor`, `/edit_doctor/<id>`, `/delete_doctor/<id>`
- `/add_patient`, `/view_patient`, `/edit_patient/<id>`, `/delete_patient/<id>`
- `/add_appointment`, `/view_appointment`, `/delete_appointment/<id>`
Queries:
- `/unread_queries`, `/read_queries`, `/view_queries/<id>`

## Setup & Run (Windows)

### 1) Clone the repository
git clone <https://github.com/Narayan-Sambare/Hospital_Management_System>

cd Hospital_Management_System

### 2) Create a virtual environment
python -m venv venv
* Activate a virtual environment *
venv\Scripts\activate

### 3) Install dependencies
This project does not include a `requirements.txt` yet, so install Django directly:
pip install django==3.2.8

### 4) Apply migrations (recommended)
python manage.py migrate

### 5) Create an admin user
python manage.py createsuperuser

### 6) Start the server
python manage.py runserverOpen: `http://127.0.0.1:8000/`

## Login Notes

- The custom admin login page is at: `/login`
- Only users with **staff** access can log in successfully.
- You can also use the Django admin at: `/admin/`

## Author

- Narayan D Sambare

==============================================================================================
