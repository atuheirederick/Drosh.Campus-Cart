# 🛒 Drosh Campus-Cart UG

A single-page campus e-commerce prototype for Ugandan university students — books, stationery, snacks, breakfast, tea, lunch and university merchandise, ordered online and delivered to campus locations.

> **Academic prototype (MGT3151).** All data is fictitious and payments are mocked. **Never enter a real PIN, OTP or card number.**

**Live demo:** `https://<your-username>.github.io/<repo-name>/` *(after enabling GitHub Pages — see below)*

---

## ✨ Features

**Customers**
- Browse 17 products across 7 categories, with search and category filters
- Shopping cart with live stock checks
- Delivery to campus locations (Main Gate, Library, Hostel Blocks A & B, Faculty of Engineering, Cafeteria) — flat fee UGX 1,000
- Mock Mobile Money checkout
- Order tracking: **Paid → Preparing → Out for delivery → Delivered**
- Rate orders and request returns

**Admin (Drosh staff)**
- Advance order status
- Approve / reject return requests
- Restock products
- Activity log (last 60 actions)
- Access-control: non-admins are blocked from the admin page

**General**
- Registration, login and logout (passwords stored as hashes)
- Light / dark mode (follows system theme)
- Responsive and mobile-friendly
- Accessible: focus outlines, ARIA live toast notifications

## 🔑 Demo accounts

| Role | Email | Password |
|------|-------|----------|
| Admin | `admin@drosh.test` | `Admin123` |
| Customer | `student@ucu.test` | `Student123` |

## 🧰 Tech stack

- Plain **HTML, CSS and JavaScript** — one file, no frameworks, no build step, no dependencies
- Data persisted in the browser via `localStorage` (key: `dcc_v1`)

## 🚀 Run locally

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
# Option 1: just open index.html in your browser
# Option 2: serve it
python3 -m http.server 8000   # then visit http://localhost:8000
```

## 🌐 Deploy on GitHub Pages

1. Push the repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch** (or **GitHub Actions** to use the included workflow).
4. Select branch `main` and folder `/ (root)`, then **Save**.
5. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## 🗂 Project structure

```
.
├── index.html              # The entire application
├── README.md               # This file
├── LICENSE                 # MIT License
├── CONTRIBUTING.md         # How to contribute
├── .gitignore
└── .github/workflows/
    └── pages.yml           # Optional auto-deploy to GitHub Pages
```

## ⚠️ Limitations

This is a front-end demo only:
- No real backend or database — data lives in each visitor's browser and is lost if storage is cleared
- Payments are simulated; no real money moves
- The password hashing and admin check are client-side and **not secure** for production use

## 🛣 Possible next steps

- Real backend (Node/Django) and database
- Genuine Mobile Money API integration (MTN MoMo / Airtel Money)
- Server-side authentication and order management
- Product image uploads and vendor accounts

## 📄 License

Released under the [MIT License](LICENSE).

## 👤 Author

**Drosh** — MGT3151 project. Replace this line with your full name, registration number and contact.
