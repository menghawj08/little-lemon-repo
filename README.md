# little-lemon-repo
# Hello this is the final capstone project of the backend developer coursera course.

Little Lemon Web Application

Introduction
This is my final project for the Meta Back-End Developer Capstone course:
https://www.coursera.org/learn/back-end-developer-capstone/

I built this web application using Django, Django REST Framework (DRF), Djoser, and MySQL. There’s a straightforward static page you can check out at:

http://localhost:8000/restaurant/


APIs
Menu Endpoints
restaurant/api/menu

GET: Authenticated users can view all menu items.
POST: Only the admin can add new items.
Fields for a POST request

title (string)
price (decimal)
featured (boolean, optional, default = false)
restaurant/api/menu/<int:pk>

GET: Authenticated users can view a single menu item.
PUT/PATCH/DELETE: Only the admin can update or delete a specific item.

Booking Endpoints
restaurant/api/book

POST: Authenticated users can create a new booking.
Make sure to use the exact username as the name field.
GET: Users can retrieve all bookings that match their own username in the name field.
Fields for a POST request

name (string, must match username)
guest_number (integer, optional, default = 1)
date (date in "YYYY-MM-DD" format)
comment (text, optional)
restaurant/api/book/<int:pk>

GET/DELETE: Only the admin can view or delete a specific booking.
