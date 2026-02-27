# RealEstate Laravel (Laravel 5.6)

A real estate web application built with Laravel 5.6.

## Overview

This project provides a complete property listing platform with:

- Admin, Agent, and User roles
- Property listing and detail pages
- Blog, gallery, testimonials, and services sections
- Messaging and rating modules
- Seeded default accounts for quick testing

## Tech Stack

- Laravel 5.6
- PHP 7.2 - 7.4 (7.4 recommended)
- MySQL
- Blade templates + Laravel Mix assets

## Important Compatibility Note

This is an older Laravel codebase and is **not compatible with PHP 8+**.

Use PHP 7.4 for best results.

## Requirements

- PHP `7.2 - 7.4`
- Composer
- MySQL Server (or MariaDB compatible)
- Node.js + npm (only if you want to rebuild frontend assets)

## Installation

1. Clone the repository:

```bash
git clone https://github.com/r4ms3ey/RealEstate-Laravel.git
cd RealEstate-Laravel
```

2. Install PHP dependencies:

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

## Database Setup

You can choose either method below.

### Option A: Fresh Migration + Seed

This creates schema from migrations and inserts default demo data.

```bash
php artisan migrate --seed
```

### Option B: Import Included SQL Dump

An updated SQL dump is available at:

- `database/realestatelrvl.sql`

Import example (MySQL CLI):

```bash
mysql -u root -p realestatelrvl < database/realestatelrvl.sql
```

After import, confirm `.env` uses the same DB name and credentials.

## Running the Project

Start Laravel dev server:

```bash
php artisan serve
```

Open:

- http://127.0.0.1:8000

## Default Login Credentials

### Admin

- Email: `admin@mail.com`
- Password: `RAMSEY`

### Agent

- Email: `agent@mail.com`
- Password: `RAMSEY`

### User

- Email: `user@mail.com`
- Password: `RAMSEY`

## Optional Frontend Build

If you change assets and need to rebuild:

```bash
npm install
npm run dev
```

## Troubleshooting

### Composer fails with PHP version errors

Use PHP 7.4. If your system defaults to PHP 8+, switch PATH/terminal to PHP 7.4 before running Composer or Artisan.

### `Unknown database 'realestatelrvl'`

Create the database in MySQL first, then run migration/seed or import the SQL file.

### 500 errors / cache issues

Run:

```bash
php artisan config:clear
php artisan cache:clear
php artisan view:clear
```

## Notes

- Uploaded files are served from `public/` and Laravel storage directories.
- Keep `.env` private; never commit production secrets.
