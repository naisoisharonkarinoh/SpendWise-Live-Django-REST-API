# SpendWise Live - Django REST API

Week 8 backend: turns the Week 7 in-memory expense manager into a real, persisted, per-user REST API.

## Quick start

```bash
git clone https://github.com/naisoisharonkarinoh/SpendWise-Live-Django-REST-API.git
cd SpendWise-Live-Django-REST-API
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## API Endpoints

| Method | URL | Auth | Description |
|--------|-----|------|-------------|
| POST | `/api/register/` | None | Create account |
| POST | `/api/login/` | None | Get token |
| GET | `/api/expenses/` | Token | List expenses |
| POST | `/api/expenses/` | Token | Create expense |
| DELETE | `/api/expenses/{id}/` | Token | Delete expense |
| GET | `/api/expenses/summary/` | Token | Category totals |

## Filtering

```
GET /api/expenses/?category=food
GET /api/expenses/?search=coffee
GET /api/expenses/?ordering=-amount
GET /api/expenses/?page=2
```

## Categories

food, transport, entertainment, utilities, health, shopping, other

## Auth header

```
Authorization: Token <your-token-here>
```
