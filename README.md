# RealEstate Laravel (Laravel 5.6)

A real estate web application built with Laravel 5.6.

## Tech Stack

- Laravel 5.6
- PHP 7.4 (recommended for this project)
- MySQL

## Requirements

- PHP `7.2 - 7.4` (project is not compatible with PHP 8+)
- Composer
- MySQL server

## Project Setup

1. Clone the repository:

```bash
git clone https://github.com/r4ms3ey/RealEstate-Laravel.git
cd RealEstate-Laravel
```

2. Install dependencies:

```bash
composer install
```

3. Create environment file:

```bash
copy .env.example .env
```

4. Generate app key:

```bash
php artisan key:generate
```

5. Configure database in `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=realestatelrvl
DB_USERNAME=root
DB_PASSWORD=
```

## Database Setup (Two Options)

### Option A: Migrate + Seed

```bash
php artisan migrate --seed
```

### Option B: Import SQL Dump

A full dump is included at:

- `database/realestatelrvl.sql`

Import it into MySQL, then ensure `.env` points to that database.

## Run the Project

```bash
php artisan serve
```

Open:

- http://127.0.0.1:8000

## Login Credentials

### Admin

- Email: `admin@mail.com`
- Password: `RAMSEY`

### Agent

- Email: `agent@mail.com`
- Password: `RAMSEY`

### User

- Email: `user@mail.com`
- Password: `RAMSEY`

## Notes

- If you are on PHP 8+, switch to PHP 7.4 to run this project.
- Uploaded files are served from `public/` and Laravel storage directories.
