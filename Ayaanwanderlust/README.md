🌍 WanderLust

WanderLust is a full-stack Node.js & Express-based web application for creating and exploring travel listings.
The project follows the MVC architecture and focuses on backend robustness, secure authentication, and clean server-side rendering using EJS.

⚡ Overview
🔧 Tech Stack

Node.js · Express.js · MongoDB (Mongoose) · EJS · Passport.js · Cloudinary · Leaflet · MapTiler

✨ Key Features

User authentication (signup, login, logout) with sessions

Create, read, update, and delete travel listings

Image uploads with Cloudinary integration

Review & rating system for listings

Owner-based authorization (edit/delete protection)

Interactive maps with geolocation

Flash messages & centralized error handling

Strong server-side validation

🧩 Project Structure (MVC)

Models

/models — Mongoose schemas for Users, Listings, and Reviews

Views

/views — EJS templates, layouts, and partials

Controllers

/controllers — Business logic for listings, reviews, and authentication

Other Important Folders

/routes — Express route definitions

/middleware — Authentication & authorization logic

/utils — Helpers (validation, Cloudinary config, custom error classes)

/public — Static assets (CSS, JS)

/init — Database seeding / setup scripts

app.js — Main application entry point and Express configuration

🚀 Getting Started (Local Setup)
Prerequisites

Node.js (v16 or higher)

npm or yarn

MongoDB (local or Atlas)

Optional: Cloudinary & MapTiler accounts

📦 Installation
git clone https://github.com/abhi-2028/WanderLust.git
cd WanderLust
npm install

🔐 Environment Setup

Create a .env file in the root directory:

MONGO_URI=mongodb://localhost:27017/wanderlust
PORT=3000
SECRET=your-session-secret

CLOUDINARY_CLOUD_NAME=your-cloud-name
CLOUDINARY_KEY=your-cloud-key
CLOUDINARY_SECRET=your-cloud-secret

MAPTILER_KEY=your-maptile-api-key


Cloudinary and MapTiler are optional.
You can use dummy values for local development.

🧠 Running the Application
Development Mode
npm run dev

Production Mode
npm start


The application runs at:
👉 http://localhost:3000

Inline environment variables (PowerShell example):

$env:MONGO_URI="mongodb://127.0.0.1:27017/wanderlust"; npm run dev

🗺 Route Summary
📍 Listings
Method	Route	Description	Access
GET	/listings	View all listings	Public
GET	/listings/new	New listing form	Auth
POST	/listings	Create listing	Auth
GET	/listings/:id	View listing	Public
GET	/listings/:id/edit	Edit listing	Owner
PUT	/listings/:id	Update listing	Owner
DELETE	/listings/:id	Delete listing	Owner
⭐ Reviews
Method	Route	Description	Access
POST	/listings/:id/reviews	Add review	Auth
DELETE	/listings/:id/reviews/:reviewId	Delete review	Author / Owner
👤 Users
Method	Route	Description	Access
GET	/register	Register page	Public
POST	/register	Create user	Public
GET	/login	Login page	Public
POST	/login	Login user	Public
GET	/logout	Logout	Auth
🧰 Troubleshooting
Issue	Solution
MongoDB connection error	Check MONGO_URI & MongoDB service
Image upload fails	Verify Cloudinary credentials
Map not loading	Check MAPTILER_KEY and map JS config
Sessions not persisting	Ensure SECRET is set correctly
🤝 Contributing

Fork the repository

Create a new feature branch

Commit and test your changes

Open a pull request with a clear description

Small and focused PRs are appreciated.

👤 Author

Ayaan Shaikh
Backend-Focused Full Stack Developer

Designed and implemented the WanderLust platform using Node.js, Express, MongoDB, and EJS

Followed MVC architecture with secure authentication and authorization

Integrated Cloudinary, maps, and robust server-side validation

For questions, issues, or improvements, feel free to open an issue on GitHub.