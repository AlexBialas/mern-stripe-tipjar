☕ MERN Stripe Tip Jar

A small MERN (MongoDB, Express, React, Node.js) demo project with Stripe (test mode) integration.
Users can "buy you a coffee" — make a test payment through Stripe Checkout.
Transactions are stored in MongoDB, and the total collected amount is displayed on the page.

---

🇩🇪 MERN Stripe Tip Jar

Ein kleines MERN (MongoDB, Express, React, Node.js) Demo-Projekt mit Stripe (Testmodus) Integration.
Benutzer können dir symbolisch einen Kaffee "spendieren" – also eine Testzahlung über Stripe Checkout durchführen.
Die Transaktionen werden in MongoDB gespeichert, und die Gesamtsumme wird auf der Seite angezeigt.

---

🚀 DEMO
(coming soon – after first deployment)

---

🧩 TECH STACK | TECHNOLOGIE-STACK

Frontend: React + Vite + TypeScript
Backend: Express + Node.js + MongoDB (Mongoose)
Payments | Zahlungen: Stripe Checkout (Test Mode)
Styling: simple CSS / optional Tailwind

---

⚙️ FEATURES | FUNKTIONEN

- Test payment via Stripe Checkout
- Stores completed sessions in MongoDB
- Displays total collected amount
- Fully local setup (no real money involved)
- Easy to extend for real Stripe integration

---

🧠 LOCAL SETUP | LOKALE INSTALLATION

1️⃣ CLONE THE REPOSITORY | REPOSITORY KLONEN

git clone https://github.com/AlexBialas/mern-stripe-tipjar.git
cd mern-stripe-tipjar

2️⃣ BACKEND SETUP (EXPRESS)

cd server
pnpm install
cp .env.example .env   # or create .env manually
pnpm dev

.env EXAMPLE:

PORT=4000
MONGO_URL=<your MongoDB Atlas connection string>
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
CLIENT_URL=http://localhost:5173

3️⃣ FRONTEND SETUP (REACT)

cd ../web
pnpm install
pnpm dev

.env EXAMPLE:

VITE_API_URL=http://localhost:4000
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_...

---

🧾 STRIPE TEST GUIDE | STRIPE TESTMODUS

1. Start the Stripe CLI listener:
   stripe listen --forward-to http://localhost:4000/api/webhook

2. Visit http://localhost:5173 in your browser

3. Click "Pay" and use the test card:
   - 4242 4242 4242 4242
   - Any future expiry date
   - Any CVC

4. After success, check that the total amount increases

---

📦 FOLDER STRUCTURE | PROJEKTSTRUKTUR

mern-stripe-tipjar/
├── server/   # Express backend (Stripe, MongoDB)
└── web/      # React frontend (Vite)

---

🧑‍💻 AUTHOR | AUTOR

@AlexBialas
Building modern full-stack projects (AI, Stripe, MERN, Python, WordPress, Shopify).

---

🪪 LICENSE | LIZENZ

MIT License © 2025 AlexBialas
