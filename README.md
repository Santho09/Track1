# 🛍️ ShopHub – Full-Stack E-commerce Experience

ShopHub is a modern e-commerce prototype that blends a vanilla HTML/CSS/JS frontend with an Express + MongoDB backend. It includes authentication, product discovery, favorites, cart + checkout, order persistence, and analytics for each user.

---

## 🚀 Setup Steps

### 1. Clone & Install
```bash
git clone <repo-url>
cd ecommerce
```

#### Backend
```bash
cd backend
npm install
```

#### Frontend
Static files only. Recommended to serve via a simple HTTP server:
```bash
cd frontend
npx http-server -p 8000
```

### 2. Environment Variables (`backend/.env`)
```env
JWT_SECRET=your-secure-random-string
MONGO_URI=your-mongodb-connection-string
FRONTEND_URL=https://your-frontend-domain.com
ALLOWED_ORIGINS=http://localhost:8000,http://127.0.0.1:5500
PORT=3000
NODE_ENV=production
```

### 3. Run Backend
```bash
cd backend
npm run dev   # or npm start
```

### 4. Run Frontend
Open `http://localhost:8000/login.html` (or wherever you hosted the static files).

---

## 🧰 Tech Stack

- **Frontend**: HTML5, CSS3 (Flexbox/Grid), vanilla JavaScript
- **Backend**: Node.js, Express.js, MongoDB (Mongoose), JWT, bcrypt, dotenv
- **Tooling**: Render/Netlify-ready deploy, optional http-server for local dev

---

## 📸 Screenshots / Recording

| Login / Signup | 
<img width="1920" height="1200" alt="Screenshot (246)" src="https://github.com/user-attachments/assets/2c70c38a-6a07-4df0-bdd7-9ab37b807eee" />

<img width="1920" height="1200" alt="Screenshot (247)" src="https://github.com/user-attachments/assets/ac7e09c8-0b34-43c5-ac6b-cf7b3ef3b8b2" />


| Products & Hover Cards | 
<img width="1920" height="1200" alt="Screenshot (248)" src="https://github.com/user-attachments/assets/78ef89fe-5023-4d4c-a172-2f401bb65fc5" />

| Favorites Sidebar |
<img width="1920" height="1200" alt="Screenshot (254)" src="https://github.com/user-attachments/assets/c5833c5d-a8a6-4809-b1e9-5a40761114a2" />

| Cart & Checkout Modal | 
<img width="1920" height="1200" alt="Screenshot (249)" src="https://github.com/user-attachments/assets/2c486047-1fd4-4969-964e-10361cca7b79" />

<img width="1920" height="1200" alt="Screenshot (250)" src="https://github.com/user-attachments/assets/89b93bb6-f914-4bf2-8d35-1bf1af4c399c" />
<img width="1920" height="1200" alt="Screenshot (251)" src="https://github.com/user-attachments/assets/1962f3d8-21fd-4b6d-a6a3-1736a6c735d6" />

| Dashboard & Analytics | 
<img width="1920" height="1200" alt="Screenshot (253)" src="https://github.com/user-attachments/assets/79ff7b38-8d7e-4d84-a44c-45f2936e13fa" />




---

## ✅ Features & Assumptions

### Core Flows
- Product cards with live search/filter/sort.
- Single-page feel with modals and quick navigation.
- Per-user favorites stored with user-specific keys.
- Cart with quantity controls and checkout modal capturing shipping + payment method.
- Orders stored in MongoDB and fetched per user at login; dashboard only shows that user’s history & analytics.

### Dashboard
- Purchase history with thumbnails and metadata.
- Analytics module: total orders, revenue, avg order value, top payment method, and category distribution chart.

### Assumptions
- Product catalog is static (`frontend/data.json`).
- Payment flow is simulated; no actual gateway integration.
- Orders/analytics rely on logging in; guest browsing works but cannot place orders.

---

## 🎯 Bonus Features Implemented

- **Authentication** with JWT + bcrypt.
- **Advanced UI**: dark mode, favorites FAB, hover animations, responsive layout.
- **Checkout workflow** with address/payment capture.
- **Data visualization**: Canvas-based analytics.
- **Multiple tracks**: frontend UX, backend auth, analytics.
- **Deployment-ready**: tested with Render (API) and Netlify-compatible front-end.

---

## 📦 Project Structure
```
ecommerce/
├── frontend/
│   ├── index.html
│   ├── login.html
│   ├── styles.css
│   ├── script.js
│   └── data.json
└── backend/
    ├── index.js
    ├── package.json
    ├── package-lock.json
    ├── ENV_SETUP.md
    └── ...
```

---

## 🧪 Demo Flow
1. Signup or login at `/frontend/login.html`.
2. Browse products, add favorites, add to cart.
3. Open the cart → “Proceed to Checkout” → fill shipping + payment → place order.
4. Visit Dashboard to confirm purchase history & analytics update.
5. Log out, log in as a different user to see isolated favorites/orders.

---

## 🌐 Deployment Notes
- Backend tested on **Render** (`https://ecommerce-jknx.onrender.com`).
- Frontend is static-host friendly (Netlify/Vercel/GitHub Pages).
- Update `FRONTEND_URL` & `ALLOWED_ORIGINS` when deploying new environments.

---





