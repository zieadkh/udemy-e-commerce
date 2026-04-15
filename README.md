# Node.js E-commerce Practice App

This project is a simple e-commerce web application built with Node.js and Express. It was created as a learning exercise to practice building a server-side application with routing, views, controllers, and basic data storage.

## Why this project was built

- To practice the fundamentals of Node.js and Express.
- To understand how to structure a web application using MVC-inspired organization.
- To learn rendering dynamic pages with EJS templates.
- To practice handling form input, serving static assets, and routing in a real app-like scenario.

## User Stories

### Customer / Shopper
- As a customer, I can **view a list of all available products** on the shop homepage so I can browse what's available.
- As a customer, I can **click on a product** to see detailed information including price, description, and product ID.
- As a customer, I can **add products to my cart** from the product listing or product detail page.
- As a customer, I can **view my cart** to see all items I've added, including quantities and total price.
- As a customer, I can **remove items from my cart** if I change my mind about a purchase.
- As a customer, I can **proceed to checkout** to complete my purchase.
- As a customer, I can **view my orders** to see a history of past purchases.

## Admin Stories

### Administrator
- As an admin, I can **access the admin dashboard** to manage products.
- As an admin, I can **view a list of all products** currently in the system.
- As an admin, I can **add a new product** by filling out a form with product details (title, price, description, image URL).
- As an admin, I can **edit an existing product** to update its information such as price, description, or availability.
- As an admin, I can **delete a product** from the inventory to remove items that are no longer available.
- As an admin, I can **see product details** including the product ID, price, and description when managing inventory.

## Project structure

- `app.js` - Main application entry point. Configures Express, body parsing, static files, routes, view engine, and error handling.
- `package.json` - Project metadata, dependencies, and start scripts.

### `controllers/`
Contains controller logic for handling requests and preparing data for the views.
- `admin.js` - Handles admin routes for creating and editing products.
- `shop.js` - Handles shop routes like product listing, product details, cart, and orders.
- `error.js` - Handles 404 error route rendering.

### `routes/`
Defines the URL endpoints and associates them with controller functions.
- `admin.js` - Routes for admin-related pages under `/admin`.
- `shop.js` - Routes for public shop pages.

### `views/`
EJS templates used to render HTML pages.
- `includes/` - Shared partial templates like navigation, head, and the add-to-cart form.
- `admin/` - Templates for admin product management.
- `shop/` - Templates for storefront pages like cart, checkout, orders, and product detail.
- `404.ejs` - Template for not-found pages.

### `public/`
Static assets served directly to the browser.
- `css/` - Styles for forms, main layout, and product pages.
- `js/` - Client-side JavaScript.

### `models/`
Contains the data logic for products and cart operations.
- `product.js` - Product model for accessing and manipulating product data.
- `cart.js` - Cart model for storing and updating cart items.

### `data/`
Stores JSON data used by the models.
- `products.json` - Product information.
- `cart.json` - Cart contents saved between requests.

### `util/`
Utility helpers used across the app.
- `path.js` - Custom path helper to build file paths.

## Technologies used so far

### Backend
- `Node.js` - JavaScript runtime used to build the backend server.
- `Express` - Web framework for handling routing, middleware, and request/response logic.
- `body-parser` - Middleware to parse incoming form data from `POST` requests.
- `path` module - Native Node utility to build file paths safely across operating systems.

### Frontend / View Layer
- `EJS` - Templating engine for rendering dynamic HTML views on the server.
- `express.static` - Built-in Express middleware to serve static CSS and client-side JavaScript.

### Data Storage
- `JSON` files - Simple local storage for products and cart data without a database.

### Development Tools
- `nodemon` - Development dependency for automatically restarting the server during development.

## Design notes

- Uses `Express` for routing and middleware handling.
- Uses `EJS` as the templating engine for rendering dynamic HTML.
- Separates route definitions from controller logic for clearer structure.
- Organizes views with reusable partials to keep templates DRY.
- Stores data in JSON files to keep the app simple and easy to understand.

## How to run

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the app in development mode:
   ```bash
   npm run start
   ```
3. Open the browser at `http://localhost:3000`

## What this project practices

- Express app setup and middleware
- Routing and controller design
- Server-side templating with EJS
- Basic model and data handling
- Project structure for maintainable Node applications

This project is a practical and effective way to sharpen backend JavaScript skills while building a simple e-commerce experience.
