# ☕ MERN Stripe Tip Jar

A small **MERN (MongoDB, Express, React, Node.js)** demo project with **Stripe (test mode)** integration.  
Users can “buy you a coffee” — make a test payment through Stripe Checkout.  
Transactions are stored in MongoDB, and the total collected amount is displayed on the page.

---

# 🇩🇪 MERN Stripe Tip Jar

Ein kleines **MERN (MongoDB, Express, React, Node.js)** Demo-Projekt mit **Stripe (Testmodus)** Integration.  
Benutzer können dir symbolisch einen Kaffee „spendieren“ – also eine Testzahlung über Stripe Checkout durchführen.  
Die Transaktionen werden in MongoDB gespeichert, und die Gesamtsumme wird auf der Seite angezeigt.

---

## 🚀 Demo
*(coming soon – after first deployment)*

---

## 🧩 Tech Stack | Technologie-Stack
**Frontend:** React + Vite + TypeScript  
**Backend:** Express + Node.js + MongoDB (Mongoose)  
**Payments | Zahlungen:** Stripe Checkout (Test Mode)  
**Styling:** simple CSS / optional Tailwind

---

## ⚙️ Features | Funktionen
- ✅ Test payment via Stripe Checkout  
- ✅ Stores completed sessions in MongoDB  
- ✅ Displays total collected amount  
- ✅ Fully local setup (no real money involved)  
- ✅ Easy to extend for real Stripe integration

---

## 🧠 Local Setup | Lokale Installation

### 1️⃣ Clone the repository | Repository klonen

git clone https://github.com/AlexBialas/mern-stripe-tipjar.git
cd mern-stripe-tipjar


### 2️⃣ Backend setup (Express)

cd server
pnpm install
cp .env.example .env   # or create .env manually
pnpm dev


.env example 

PORT=4000
MONGO_URL=<your MongoDB Atlas connection string>
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
CLIENT_URL=http://localhost:5173


### 3️⃣ Frontend setup (React)

cd ../web
pnpm install
pnpm dev

.env example
VITE_API_URL=http://localhost:4000
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_...

### 🧾 Stripe Test Guide | Stripe Testmodus

1.Start the Stripe CLI listener:

stripe listen --forward-to http://localhost:4000/api/webhook

Visit http://localhost:5173 in your browser

Click “Pay” and use the test card:
💳 4242 4242 4242 4242, any date, any CVC

After success, check that the total amount increases

### 📦 Folder Structure | Projektstruktur

mern-stripe-tipjar/
├── server/   # Express backend (Stripe, MongoDB)
└── web/      # React frontend (Vite)


### 🧑‍💻 Author | Autor

@AlexBialas
Building modern full-stack projects (AI, Stripe, MERN, Python, WordPress, Shopify).

### 🪪 License | Lizenz

MIT License © 2025 AlexBialas
