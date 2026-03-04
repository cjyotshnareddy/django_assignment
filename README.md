

Appointment Booking API

This project is a simple Appointment Booking API built using Django and Django REST Framework (DRF).
The main idea of this project is to manage appointments between clients and services.

For example, a client can book a service like a consultation or haircut at a specific date and time. The API stores all the information and allows creating, viewing, updating, and deleting records.

---

Technologies Used

* Python
* Django
* Django REST Framework
* SQLite Database
* Postman (for testing APIs)

---

Project Structure

The project contains a Django project and an app called booking.

```
appointment_project
│
├── manage.py
│
├── appointment_project
│   ├── settings.py
│   ├── urls.py
│
└── booking
    ├── models.py
    ├── serializers.py
    ├── views.py
    ├── urls.py
```

* models.py → defines database tables
* serializers.py → converts database objects to JSON
* views.py → handles API logic
* urls.py → connects API endpoints

---

API Endpoints

The API supports full CRUD operations for Clients, Services, and Appointments.

CRUD = Create, Read, Update, Delete.

---

Clients

| Method | Endpoint           | Description                     |
| ------ | ------------------ | ------------------------------- |
| GET    | /api/clients/      | Get all clients                 |
| GET    | /api/clients/{id}/ | Get a specific client           |
| POST   | /api/clients/      | Create a new client             |
| PUT    | /api/clients/{id}/ | Update entire client details    |
| PATCH  | /api/clients/{id}/ | Partially update client details |
| DELETE | /api/clients/{id}/ | Delete a client                 |

---

Services

| Method | Endpoint            | Description              |
| ------ | ------------------- | ------------------------ |
| GET    | /api/services/      | Get all services         |
| GET    | /api/services/{id}/ | Get a specific service   |
| POST   | /api/services/      | Create a new service     |
| PUT    | /api/services/{id}/ | Update entire service    |
| PATCH  | /api/services/{id}/ | Partially update service |
| DELETE | /api/services/{id}/ | Delete a service         |

---

Appointments

| Method | Endpoint                | Description                  |
| ------ | ----------------------- | ---------------------------- |
| GET    | /api/appointments/      | View all appointments        |
| GET    | /api/appointments/{id}/ | View a specific appointment  |
| POST   | /api/appointments/      | Book an appointment          |
| PUT    | /api/appointments/{id}/ | Update entire appointment    |
| PATCH  | /api/appointments/{id}/ | Partially update appointment |
| DELETE | /api/appointments/{id}/ | Delete appointment           |

---

How to Run the Project

1. Clone the repository

```
git clone <repository_link>
```

2. Create a virtual environment

```
python3 -m venv env
```

3. Activate the environment


```
source env/bin/activate
```

4. Install dependencies

```
pip install django djangorestframework
```

5. Apply migrations

```
python manage.py makemigrations
python manage.py migrate
```

6. Run the server

```
python manage.py runserver
```

Open in browser:

```
http://127.0.0.1:8000/api/
```

 
