# SKILL.md — TracAlert Agent Instructions

This file instructs Intercom-compatible agents how to interact with the TracAlert app.

## Agent Name
`tracalert`

## Capability
Price alert broadcasting over Intercom P2P sidechannels.

## Agent Actions

### `set_alert`
Set a new price alert and broadcast to peers.

**Input:**
```json
{
  "action": "set_alert",
  "coin": "BTC",
  "condition": "above",
  "target": 100000,
  "message": "BTC breakout!"
}
```

**Output:**
```json
{
  "status": "broadcast",
  "alert_id": 1,
  "peers_notified": 4
}
```

---

### `list_alerts`
List all active alerts.

**Input:**
```json
{ "action": "list_alerts" }
```

**Output:**
```json
{
  "alerts": [
    { "id": 1, "coin": "BTC", "condition": "above", "target": 100000 }
  ]
}
```

---

### `delete_alert`
Remove an alert by ID.

**Input:**
```json
{ "action": "delete_alert", "id": 1 }
```

---

### `get_prices`
Get current simulated prices for all tracked assets.

**Input:**
```json
{ "action": "get_prices" }
```

**Output:**
```json
{
  "BTC": 95241.32,
  "ETH": 3312.45,
  "SOL": 174.88,
  "BNB": 621.10,
  "XRP": 0.5401
}
```

---

## P2P Protocol

- Alerts are broadcast as JSON messages over Intercom sidechannels
- Peers subscribe to `tracalert/alerts` topic
- Alert triggers are published to `tracalert/triggers` topic
- All messages are signed with the sender's Trac identity

## Trac Address
```
YOUR_TRAC_ADDRESS_HERE
```
