# Homano Backend

Backend API for **Homano**, a full-stack e-commerce platform built with **Node.js** and **Express.js**.

The backend provides authentication, product and category management, shopping cart, orders, CMS functionality, image management, caching, and other services required by the Homano platform.

## 🚀 Features

* 🔐 JWT-based authentication
* 👤 User authentication and profile management
* 🛍️ Product management
* 📂 Category management
* 🛒 Shopping cart management
* 📦 Order management
* 📝 CMS and content management
* 🖼️ Image upload and storage with ImageKit
* ⚡ Redis caching
* 🛡️ Request validation with Zod
* 🚦 Rate limiting
* 🔒 Security headers with Helmet
* 📚 Swagger API documentation
* 🌐 CORS configuration
* 📦 Response compression

## 🛠️ Tech Stack

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**
* **Redis**
* **JWT**
* **Zod**
* **ImageKit**
* **Multer**
* **Swagger / OpenAPI**
* **Helmet**
* **Express Rate Limit**
* **Compression**
* **bcryptjs**

The project requires **Node.js 22 or higher**.

## 📂 Project Structure

The backend follows a feature-based architecture:

```text
src/
├── config/
├── features/
├── middlewares/
├── routes/
└── ...
```

Each feature contains its related routes, controllers, services, validation, and business logic, keeping the application modular and maintainable.

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:

* Node.js 22+
* MongoDB
* Redis
* npm

### Installation

Clone the repository:

```bash
git clone https://github.com/KasraMg/homano-backend.git

cd homano-backend
```

Install dependencies:

```bash
npm install
```

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
MONGO_URI=

PORT=1000

JWT_SECRET=

FRONTEND_URL=http://localhost:5173

REDIS_URL=redis://localhost:6379

NODE_ENV=development

SWAGGERURLREQUEST=

FRONTEND_v2_URL=
FRONTEND_v3_URL=http://localhost:5173

IMAGEKIT_PUBLIC_KEY=
IMAGEKIT_PRIVATE_KEY=
IMAGEKIT_URL_ENDPOINT=
```

> Never commit your `.env` file or expose database credentials, private keys, JWT secrets, or other sensitive credentials.

## ▶️ Running the Application

Start the development server:

```bash
npm run dev
```

The API will be available at:

```text
http://localhost:1000
```

For production:

```bash
npm start
```

## 📚 API Documentation

The project uses **Swagger / OpenAPI** for API documentation.

When running in development mode, Swagger is available at:

```text
http://localhost:1000/api-docs
```

The API uses JWT Bearer authentication for protected endpoints.

## 🗄️ Database

**MongoDB** is used as the primary database, with **Mongoose** handling database models and queries.

## ⚡ Caching

**Redis** is integrated as a caching layer to reduce repeated database queries and improve response performance.

The application initializes the Redis connection alongside the database connection.

## 🖼️ File Storage

Image uploads are handled using **Multer** and stored through **ImageKit**.

Using cloud-based storage allows uploaded assets to persist independently of the application server and makes the application more suitable for cloud and serverless deployments.

## 🛡️ Security

The backend includes several security and performance middlewares:

* Helmet
* CORS
* Rate limiting
* Request validation with Zod
* Password hashing with bcrypt
* JWT authentication
* Response compression

## 🌐 API

Development:

```text
http://localhost:1000/api
```

Production:

```text
https://homano-backend.vercel.app/api
```

## 🔗 Related Projects

* **Frontend:** https://homano.vercel.app/
* **Backend:** https://homano-backend.vercel.app/

## 🌐 Live Demo

[Homano](https://homano.vercel.app/)

## 👨‍💻 Author

**Kasra Mg**

[GitHub](https://github.com/KasraMg)
