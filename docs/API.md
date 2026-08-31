# API Routes Documentation

## Authentication Routes

### POST /api/auth/register
Register a new user account
```json
{
  "email": "user@example.com",
  "password": "password123",
  "firstName": "John",
  "lastName": "Doe"
}
```

### POST /api/auth/login
Login to user account
```json
{
  "email": "user@example.com",
  "password": "password123"
}
```

### POST /api/auth/logout
Logout user account

### POST /api/auth/refresh-token
Refresh JWT token

---

## User Routes

### GET /api/users/profile
Get user profile

### PUT /api/users/profile
Update user profile

### GET /api/users/preferences
Get user trading preferences

### PUT /api/users/preferences
Update trading preferences

---

## Market Routes

### GET /api/markets/stocks
Get stock market data

### GET /api/markets/crypto
Get cryptocurrency prices

### GET /api/markets/forex
Get forex rates

### GET /api/markets/search
Search for market symbols

### GET /api/markets/:symbol
Get detailed market data for specific symbol

---

## Trading Routes

### POST /api/trades/buy
Place a buy order

### POST /api/trades/sell
Place a sell order

### GET /api/trades/history
Get trading history

### GET /api/trades/open
Get open positions

### PUT /api/trades/:id
Update trade

### DELETE /api/trades/:id
Cancel trade

---

## Portfolio Routes

### GET /api/portfolio
Get complete portfolio

### GET /api/portfolio/balance
Get account balance

### GET /api/portfolio/holdings
Get all holdings

### GET /api/portfolio/performance
Get portfolio performance metrics

### GET /api/portfolio/allocation
Get asset allocation

---

## Community Routes

### GET /api/community/discussions
Get all discussions

### POST /api/community/discussions
Create new discussion

### GET /api/community/discussions/:id
Get discussion details

### POST /api/community/discussions/:id/comments
Post comment on discussion

### GET /api/community/users/leaderboard
Get trading leaderboard

---

## WebSocket Events

### Market Data
- `market:connect` - Connect to market data
- `market:update` - Real-time price updates
- `market:disconnect` - Disconnect from market data

### Trading
- `trade:executed` - Trade execution notification
- `trade:filled` - Trade filled notification
- `trade:cancelled` - Trade cancelled notification

### Portfolio
- `portfolio:update` - Portfolio updated

### Notifications
- `notification:alert` - Alert notification

---

For more details on each endpoint, refer to the implementation files in the `routes/` directory.
