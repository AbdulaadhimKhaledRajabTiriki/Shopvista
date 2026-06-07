# Shopvista
# ShopVista Admin System

Multi-role e-commerce admin panel for **ShopVista** — an online store with team management, products, and categories.

## Features

- Multi-role system (admin, user, editor, moderator)
- Many-to-many relationship between users and roles
- Role-based middleware protecting admin routes
- Admin dashboard with product and category CRUD
- Login / logout with session authentication
- Bootstrap 5 UI

## Requirements

- PHP >= 8.0
- Composer
- MySQL
- XAMPP / Laragon (recommended on Windows)

## Setup

1. Clone the repository:

```bash
git clone <your-github-repo-url>
cd LaravelProject
```

2. Install dependencies:

```bash
composer install
```

3. Copy environment file and generate app key:

```bash
copy .env.example .env
php artisan key:generate
```

4. Configure database in `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=shopvista
DB_USERNAME=root
DB_PASSWORD=
```

5. Create the database in phpMyAdmin, then run migrations and seeders:

```bash
php artisan migrate
php artisan db:seed
```

6. Start the development server:

```bash
php artisan serve
```

7. Open in browser:

- Store: http://127.0.0.1:8000
- Staff Login: http://127.0.0.1:8000/login
- Admin: http://127.0.0.1:8000/admin

## Admin Login

| Field    | Value                        |
|----------|------------------------------|
| Email    | marcus.webb@shopvista.com    |
| Password | 12345678                     |

All seeded users share the password `12345678`.

## Sample Data (after `php artisan db:seed`)

| Type       | Count |
|------------|-------|
| Team       | 12    |
| Roles      | 4     |
| Categories | 8     |
| Products   | 37    |

### Team Members

| Name            | Email                          | Roles              |
|-----------------|--------------------------------|--------------------|
| Marcus Webb     | marcus.webb@shopvista.com      | admin, user        |
| Sarah Mitchell  | sarah.mitchell@shopvista.com   | admin, user        |
| John Carter     | john.carter@shopvista.com      | editor, user       |
| Emily Rivera    | emily.rivera@shopvista.com     | editor, user       |
| Michael Chen    | michael.chen@shopvista.com     | moderator, user    |
| Jessica Adams   | jessica.adams@shopvista.com    | moderator, user    |
| Robert Kim      | robert.kim@shopvista.com       | editor, user       |
| David Wilson    | david.wilson@gmail.com         | user               |
| Lisa Thompson   | lisa.thompson@yahoo.com        | user               |
| James Rodriguez | j.rodriguez@outlook.com        | user               |
| Amanda Foster   | amanda.foster@gmail.com        | user               |
| Olivia Bennett  | olivia.bennett@icloud.com      | user               |

## Push to GitHub

```bash
git add .
git commit -m "ShopVista admin system with multi-role auth"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/shopvista-admin.git
git push -u origin main
```

## License

MIT
