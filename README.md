
# 🛒 Shopease-API

**Shopease-API** is a scalable and secure **e-commerce backend API** built with **Django** and **Django REST Framework (DRF)**. It powers seamless online shopping with essential features like user authentication, product listings, cart management, order processing, and admin controls.

The project adopts modern backend practices like **modular architecture**, **JWT-based authentication**, and **token blacklisting**.

---

## 🧭 Auth Flow Diagram

![Auth Flow](/image/auth-flow.png)

---

## 📑 Table of Contents

- [🚀 Features](#-features)
- [🧰 Tech Stack](#-tech-stack)
- [⚙️ Installation](#️-installation)
- [📚 System Endpoints](#-system-endpoints)
- [🛠️ Usage](#️-usage)
- [🤝 Contributing](#-contributing)
- [📬 Contact](#-contact)

---

## 🚀 Features

### ✅ Authentication & Authorization
- **JWT Authentication** using `rest_framework_simplejwt`.
- Signup and login with **email and password** only.
- **Email uniqueness validation**.
- **Auto-login after registration** (returns tokens on success).
- **Secure logout** with **refresh token blacklisting**.
- Token expiration and refresh handling (access & refresh).

### 🛒 E-Commerce Core (In Progress)
- **Product Management**:
  - CRUD for products with images, descriptions, price, and stock.
  - Search, filtering, and sorting by category, price, etc.

- **Cart System**:
  - Add/remove products from cart.
  - Persistent cart by authenticated user.
  - Update product quantity in cart.

- **Order Management**:
  - Create orders from cart.
  - Payment method placeholder (e.g., Stripe).
  - Track order status: pending, paid, shipped, delivered.

- **User Dashboard**:
  - View past orders.
  - Profile management (planned).

### 🛠 Admin Features (Planned)
- Admin dashboard for:
  - Managing products, orders, users.
  - Inventory tracking.
  - Sales statistics (future: charts/analytics).

### 🧱 Architecture
- Modular structure with a dedicated `users` app for auth logic.
- Clean separation of concerns for scalability.
- Ready for containerization and deployment.

---

## 🧰 Tech Stack

- **Backend**: Django, Django REST Framework
- **Auth**: Simple JWT (`rest_framework_simplejwt`)
- **Database**: PostgreSQL (recommended), SQLite (dev)
- **Others**: 
  - `django-environ` for secure settings management
  - `drf-yasg` for auto-generated API documentation
  - `black`, `flake8`, `pre-commit` for code formatting & linting

---

## ⚙️ Installation

```bash
git clone https://github.com/<your-username>/shopease-api.git
cd shopease-api

# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start development server
python manage.py runserver

```

## 📚 System Endpoints

🔐 Authentication Endpoints

```
Endpoint	Method	Description
/api/auth/register/	POST	Register new user (email/password)
/api/auth/login/	POST	Obtain access and refresh tokens
/api/auth/logout/	POST	Blacklist refresh token
/api/token/refresh/	POST	Get new access token

```

## 🛠️ Usage

Use Postman or a frontend to interact with the API.

Swagger docs will be available at /docs/ after setup with drf-yasg.


## 🤝 Contributing

Pull requests are welcome!, please open an issue first to discuss your ideas.

1. Fork the repository

2. Create your feature branch (git checkout -b feature/your-feature)

3. Commit your changes (git commit -m 'Add some feature')

4. Push to the branch (git push origin feature/your-feature)

5. Open a PR


## 📬 Contact

For feedback, feature requests, or freelance collaboration:

 [Email me]: (stephenkihuni55@gmail.com)
