# Schnitzel 🥩

Three-service Python application for ordering Wiener Schnitzel.

## Architecture

| Service    | Port | Description                          |
|------------|------|--------------------------------------|
| Frontend   | 5000 | Web UI with order button             |
| Order      | 5001 | Creates and stores orders            |
| Delivery   | 5002 | Assigns delivery with random ETA     |

**Flow:** Frontend → Order Service → Delivery Service

## Setup

```bash
pip install -r requirements.txt
```

## Run

Start all three services in separate terminals:

```bash
# Terminal 1 – Order Service
python order/app.py

# Terminal 2 – Delivery Service
python delivery/app.py

# Terminal 3 – Frontend
python frontend/app.py
```

Then open http://localhost:5000 and click the button to order a schnitzel.
