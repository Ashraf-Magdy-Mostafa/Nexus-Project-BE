# 🛠️ Nexus Backend — Django REST API for E-Commerce

## Overview

This is the **backend** for the Nexus Project: a robust Django REST API powering a modern e-commerce platform. It provides endpoints for products, authentication, cart, and order management, with JWT-based authentication and a modular, production-ready structure.

---

## Features

- 🛍️ Product catalog API (CRUD, filtering, search, pagination)
- 🔐 JWT authentication (login, register, token refresh)
- 🛒 Cart and order endpoints
- 🧑‍💻 User management
- 🗃️ SQLite database (easy to swap for Postgres/MySQL)
- 🧩 Modular Django app structure
- 🧪 Seed script for demo products

---

## Tech Stack

- **Django**
- **Django REST Framework**
- **djangorestframework-simplejwt** (JWT auth)
- **SQLite** (default, easy to change)

---

## Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/Ashraf-Magdy-Mostafa/Nexus-project.git
cd Nexus-project/Back-end
```

### 2. Create & Activate Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate  # On Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Migrations

```bash
python manage.py migrate
```

### 5. (Optional) Seed Demo Products

```bash
python manage.py seed_products
```

### 6. Start the Server

```bash
python manage.py runserver
```

- API root: [http://localhost:8000](http://localhost:8000)

---

## Project Structure

```
Back-end/
├── config/         # Django project settings
├── shop/           # Main app: models, views, serializers, management
│   ├── management/ # Custom commands (e.g., seed_products)
│   ├── migrations/ # DB migrations
│   ├── models.py   # Product, user, etc.
│   ├── serializers.py
│   ├── views.py
│   └── urls.py
└── requirements.txt
```

---

## API Endpoints (Examples)

- `/api/products/` — List, search, filter, create products
- `/api/auth/` — Login, register, JWT token management
- `/api/cart/` — Cart operations (add, remove, update)
- `/api/orders/` — Order management

---

## Environment Variables

- Configure secrets and DB in `config/settings.py` as needed for production.

---

## Testing

```bash
python manage.py test
```

---

## Deployment

- Ready for deployment to Heroku, Render, or any WSGI-compatible host
- Swap SQLite for Postgres/MySQL in production

---

## License

MIT License. Free to use, modify, and share.

---

## Author

Developed by [Ashraf Magdy Mostafa](https://github.com/Ashraf-Magdy-Mostafa) as part of ALX Project Nexus — September 2025.
