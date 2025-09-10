
# Sharma Tiffin — API Server (Node/Express)

## Setup
1. Install Node.js LTS
2. `cd api_server_node`
3. `npm install`
4. Copy `.env.example` to `.env` and edit values (change `ADMIN_PIN`, optional).
5. `npm run start`

## Endpoints
- `GET /menu` – returns pricing
- `GET /delivery/fee?km=5` – returns fee based on slabs in `../sharma-config.json`
- `POST /orders` – create order and returns UPI intent URL for payment to `prince190992-1@okicici`
- `POST /admin/login` – body: `{ pin }`
- `GET /admin/orders` – list orders
- `POST /admin/orders/:id/status` – update status

## Storage
- LowDB JSON file at `data/db.json` (no external DB needed).

## Delivery Fee Rules
- 0–3 km: ₹10
- 3–6 km: ₹20
- 6–10 km: ₹30
- 10+ km: ₹50

Edit `../sharma-config.json` to change fees or pricing.
Deployed on Render 🚀
# Triggered deploy

