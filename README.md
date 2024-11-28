# Delivery-Service-API
Courier Delivery Service API is a RESTful web service built with Django and Django REST Framework (DRF). 
It allows managing courier deliveries with features like user roles (customer, courier, admin), parcel tracking, and proof of delivery uploads.

Features
User Management: Create and manage users with roles: customer, courier, and admin.
Parcel Management: Create, track, and manage parcels with statuses such as Pending, In Transit, and Delivered.
Delivery Proof: Upload proof of delivery images for completed parcels.
Token-Based Authentication: Secure API endpoints using JSON Web Tokens (JWT).
API Documentation: Interactive API docs powered by Swagger.

Installation

Prerequisites
Python 3.8+
Django 4.0+
PostgreSQL (recommended for production)

Setup
Clone the repository:
git clone https://github.com/anageguchadze/Delivery-Service-API.git

Install dependencies:
pip install -r requirements.txt

Set up environment variables:
Copy .env.example to .env and update the settings as needed.
cp .env.example .env

Run migrations:
python manage.py migrate

Create a superuser:
python manage.py createsuperuser

Start the development server:
python manage.py runserver

Access the application:
API: http://localhost:8000/api/
Admin Panel: http://localhost:8000/admin/
Swagger Docs: http://localhost:8000/swagger/
API Endpoints
Endpoint	Description
/api/users/	Manage users
/api/parcels/	Manage parcels
/api/delivery_proofs/	Upload and view delivery proofs
/api/token/	Obtain JWT access and refresh tokens
/api/token/refresh/	Refresh JWT access token
/api/token/verify/	Verify JWT token validity
Project Structure
models.py: Defines CustomUser, Parcel, and DeliveryProof models.
serializers.py: Handles serialization and deserialization of models.
views.py: Implements API views using ModelViewSet.
urls.py: Configures routes for the application.
Environment Variables

Update the following in your .env file:
env
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=postgres://username:password@localhost:5432/database_name
For production, make sure to set DEBUG=False and use secure values.

License
This project is licensed under the MIT License.
