# ALX Travel App 0x00

A Django-based travel application that allows users to browse listings, make bookings, and leave reviews. This project includes API endpoints using Django REST Framework (DRF) and a seeder to populate the database with sample data.

---

## **Project Structure**

alx_travel_app_0x00/
├── alx_travel_app/
│ ├── settings.py
│ ├── urls.py
│ └── ...
├── listings/
│ ├── models.py
│ ├── serializers.py
│ ├── views.py
│ └── management/
│ └── commands/
│ └── seed.py
└── manage.py

yaml
Copy code

---

## **Features**

- **Listings**: Create and view travel listings with title, description, price per night, and location.
- **Bookings**: Users can book listings with specified check-in and check-out dates.
- **Reviews**: Users can leave ratings and comments on listings.
- **API Support**: REST API endpoints with serializers for data representation.
- **Database Seeder**: Management command to populate the database with sample listings.

---

## **Installation**

1. **Clone the repository**

```bash
git clone <your-repo-url>
cd alx_travel_app_0x00
Create a virtual environment and activate it

bash
Copy code
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
Install dependencies

bash
Copy code
pip install -r requirements.txt
Make sure Django and djangorestframework are included in requirements.txt.
Optionally, install Faker for seeding sample data: pip install Faker.

Setup Database
Make migrations

bash
Copy code
python manage.py makemigrations
python manage.py migrate
Create a superuser (optional, for admin access)

bash
Copy code
python manage.py createsuperuser
Seeding Sample Data
Populate the database with sample listings using the management command:

bash
Copy code
python manage.py seed
You should see:

nginx
Copy code
Successfully seeded listings!
Check your database or admin panel to confirm listings are created.

API Endpoints
GET /api/listings/ - List all listings

GET /api/listings/<id>/ - Retrieve a single listing

GET /api/bookings/ - List all bookings

POST /api/bookings/ - Create a new booking

Implement API views and routing in views.py and urls.py for full functionality.

Contributing
Fork the repository

Create a new branch (git checkout -b feature/your-feature)

Commit your changes (git commit -m 'Add some feature')

Push to the branch (git push origin feature/your-feature)

Open a pull request