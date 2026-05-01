Grocery IMS - MERN scaffold (minimal)
Files created at: /mnt/data/grocery-ims

Backend (server):
  - server/index.js
  - server/models/*.js
  - server/routes/*.js
  - server/package.json
  - server/.env.example

Frontend (client):
  - client/package.json (Vite + React)
  - client/src/*
  - client/public/index.html

How to run (locally):
  1. Start MongoDB (recommended as a replica set for transactions; standalone works but transactions may fail).
  2. Backend:
     cd server
     npm install
     npm start
  3. Frontend:
     cd client
     npm install
     npm run dev

Deployment:
  1. Backend (deploy to Heroku/Railway/Render/etc.):
     - Set environment variables: MONGO_URI (MongoDB connection string)
     - Deploy the server/ directory
  2. Frontend (Netlify):
     - Connect GitHub repo to Netlify
     - Build settings:
       - Base directory: client
       - Build command: npm run build
       - Publish directory: client/dist
     - Environment variables:
       - VITE_API_URL: Your deployed backend URL (e.g., https://your-backend.herokuapp.com)
     - Deploy

Features:
  - Product management
  - Billing/checkout
  - Dashboard with stats
  - Reports
  - Sales history
  - Real-time low stock notifications (Socket.io)
     copy .env.example to .env and set MONGO_URI
     npm run start
  3. Frontend:
     cd client
     npm install
     npm run dev
  API proxy from Vite is configured to http://localhost:4000

Note: This is a scaffold with essential features: product CRUD, checkout (transactional), invoice PDF generation, dashboard stats, realtime via Socket.io.
Customize, secure, and harden before production.

