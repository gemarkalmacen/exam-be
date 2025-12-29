# Laravel Backend API Setup

This section explains how to set up the backend API for the Exam Web App using Laravel.

## Prerequisites

- **PHP >= 8.2**  
- **Composer**  
- **MySQL / SQLite / PostgreSQL** (for database)  
- Git

---

## Step 1 — Clone the Backend Repository

```bash
git clone <your-backend-github-repo-url>
cd exam-be

---

## Step 2 — Install Dependencies
- composer install

---

## Step 3 — Configure Environment File

Copy the example .env file:
- cp .env.example .env

Open .env and configure your database settings:
- DB_CONNECTION=sqlite
- DB_DATABASE=/full/path/to/project/backend/database/database.sqlite


Create the SQLite file if it doesn’t exist:
- touch database/database.sqlite

## Step 4 — Generate Application Key
- php artisan key:generate

## Step 5 — Run Migrations and Seeders
- php artisan migrate --seed

## Step 6 — Start Laravel Development Server
php artisan serve

* By default, it will run at: http://127.0.0.1:8000
* Ensure the Flutter Web app points to this backend API URL (http://localhost:8000/api/login).

## Notes

Laravel API provides login functionality for the Flutter Web app.
Use SQLite or MySQL depending on your setup.
The backend must be running before testing the frontend app.

## Demo Video
Watch a live demo of the app here:
🎬 Flutter Web IP Geolocation Demo:  https://youtu.be/B8RTwPIR8hY