# Appointment Booking API

This project is a simple **Appointment Booking API** built using **Django** and **Django REST Framework (DRF)**.
The main idea of this project is to manage appointments between **clients** and **services**.

For example, a client can book a service like a consultation or haircut at a specific date and time. The API stores all the information and allows creating, viewing, updating, and deleting records.


---

## Technologies Used

* Python
* Django
* Django REST Framework
* SQLite Database
* Postman (for testing APIs)

---

## Project Structure

The project contains a Django project and an app called **booking**.

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

* **models.py** → defines database tables
* **serializers.py** → converts database objects to JSON
* **views.py** → handles API logic
* **urls.py** → connects API endpoints

---

## Database Design

The system contains three main models.

### Client

Stores information about the customer.

Fields:

* name
* email

### Service

Represents the services available for booking.

Fields:

* title
* description
* price

### Appointment

Stores appointment details.

Fields:

* client
* service
* appointment_date
* appointment_time
* status

Each appointment connects a **client** with a **service**.

---

## API Endpoints

The API provides basic CRUD operations.

### Clients

* `GET /api/clients/` → Get all clients
* `POST /api/clients/` → Create a new client

### Services

* `GET /api/services/` → Get all services
* `POST /api/services/` → Create a service

### Appointments

* `GET /api/appointments/` → View appointments
* `POST /api/appointments/` → Book an appointment
* `DELETE /api/appointments/{id}/` → Delete appointment

---


## How to Run the Project

1. Clone the repository

```
git clone <repository_link>
```

2. Create a virtual environment

```
python3 -m venv env
```

3. Activate the environment

Mac/Linux

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





If you want, I can also help you add a **small architecture diagram and API flow diagram** to this README so it looks **more professional for GitHub and internships**.
