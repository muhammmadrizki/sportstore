# Sport Store

[Sport Store](https://sportstore.muhammadrizkikurniaputra.com) Sport Store is a fullstack e-commerce web application for sports merchandise.

## Role

Fullstack Developer (Solo Project)

## Key Features

- Browse product catalogue
- View product details
- Add products to cart
- Remove items from cart
- REST API with authentication

## Links

- Frontend Web: <https://sportstoreweb.muhammadrizkikurniaputra.com>
- Backend API: <https://sportstore-api.muhammadrizkikurniaputra.com>

Repositories:

- General: <https://github.com/muhammmadrizki/sportstore>
- Backend API: <https://github.com/muhammmadrizki/sportstore-api>
- Frontend Web: <https://github.com/muhammmadrizki/sportstore-web>

Inspirations:

- <https://store.manutd.com>
- <https://store.acmilan.com>

## Architecture & Tech Stack

### Client = Presentation Layer (UI)

- HTML
- CSS
  - Tailwind CSS
  - shadcn/ui
- JavaScript
- TypeScript
- React
- React Router
- Docker

### Server = Application Layer (Business Logic)

- JavaScript
- TypeScript
- Hono
- OpenAPI
- Zod
- Docker

### Data Access Layer (Database)

- Prisma
- PostgreSQL
- Docker

## Features

- Home page
  - Hero section
  - Products catalogue
  - Example : <https://sportstore.muhammadrizkikurniaputra.com/products>

- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item

### Home Page

<img alt="Home Page" src="/assets/sportstore.png" width="400" />

## Figma

<https://www.figma.com/design/YZDhkU0lWEfYuVJadpIIy0/Sportstore---ecommerce?node-id=61-2&t=yTx4MTy4LtjzKg2v-1>

## REST API Endpoints

- Production: `https://sportstore-api.muhammadrizkikurniaputra.com`
- Local: `http://localhost:3000`

| Endpoint           | HTTP  | Description         |
| ------------------ | ----- | ------------------- |
| `/products`        | `GET` | Get all products    |
| `/products/{slug}` | `GET` | Get product by slug |

## 🔐 Authentication & User Endpoints

| Endpoint       | Method | Permission    | Description                  |
| -------------- | ------ | ------------- | ---------------------------- |
| /              | GET    | Public        | Root endpoint / health check |
| /users         | GET    | Public        | Get all users                |
| /users/{id}    | GET    | Public        | Get user by ID               |
| /auth/register | POST   | Public        | Register new user            |
| /auth/login    | POST   | Public        | Login user                   |
| /auth/me       | GET    | Authenticated | Get current user profile     |
| /auth/logout   | POST   | Authenticated | Logout user                  |

### Product

```json
{
  "id": "abc123",
  "slug": "panda-plush",
  "name": "Panda Plush",
  "price": 120000
}
```

### Add New Product

Request Body:

```json
{
  "name": "Panda Plush",
  "price": 120000,
  "color": "white"
}
```

Response Body:

```json
{
  "id": "abc123",
  "slug": "panda-plush",
  "name": "Panda Plush",
  "price": 120000,
  "colors": "white"
}
```
