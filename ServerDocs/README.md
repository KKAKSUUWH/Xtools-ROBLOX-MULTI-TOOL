# Xtools Server API Documentation

Roblox automation server with task queuing system and rate limiting. Handles account generation, profile actions, and group operations.

## Features
- API key authentication
- Task queuing system with status tracking
- Concurrent task execution with pool limits
- Mass task support for bulk operations
- Cookie validation and rotation
- Real-time statistics monitoring

## Configuration
1. Set API key in `Xtools/Config/XtoolsConfig.json`:
```json
{
  "ApiKey": "your-secret-key-here"
}
```
2. Add valid cookies to `Input/Cookies.txt`
3. Add proxies to `Input/Proxies.txt`

## API Endpoints

### Authentication
All requests require header:
`Api-Key: your-api-key`

---

### POST /api/follow
Follow a Roblox user

**Request:**
```json
{
  "user_id": "123456789",
  "amount": 1 (optional, for mass follows)
}
```

**Response:**
```json
{
  "message": {
    "task_id": "TASK123"
  },
  "code": 0
}
```

---

### POST /api/generate 
Generate new Roblox account

**Request:**
```json
{
  "username": "optional",
  "password": "optional",
  "birth": "YYYY-MM-DD (optional)",
  "gender": 1 (optional)
}
```

**Response:**
```json
{
  "username": "generated_user",
  "password": "generated_pass",
  "cookie": "roblox-cookie"
}
```

---

### POST /api/bruter
Bruteforce account checker

**Request:**
```json
{
  "username": "target_user",
  "password": "target_pass"
}
```

**Response:**
```json
{
  "username": "valid_user",
  "password": "valid_pass", 
  "cookie": "valid-cookie"
}
```

---

### POST /api/join_group
Join Roblox group

**Request:**
```json
{
  "group_id": "987654321",
  "amount": 5 (optional, mass joins)
}
```

---

### POST /api/change_display_name
Change account display name

**Request:**
```json
{
  "cookie": "valid-cookie",
  "display_name": "NewName"
}
```

---

### POST /api/humamize 
Humanize account (add realistic traits)

**Request:**
```json
{
  "cookie": "valid-cookie"
}
```

---

### GET /task/state
Check task status

**Request:**
```json
{
  "task_id": "TASK123"
}
```

**Response:**
```json
{
  "State": "Success",
  "Result": { ... },
  "CreatedAt": "timestamp"
}
```

## Task System
- Tasks are queued and executed concurrently
- Each task gets unique `task_id`
- States: Pending → Success/Failed/Finished
- Mass tasks show aggregate success/failure counts

## Error Codes
| Code | Meaning               |
|------|-----------------------|
| 0    | Success               |
| 1001 | Invalid API Key       |
| 1002 | Missing Required Field|
| 1003 | Invalid Task ID       |
| 1004 | Invalid Cookie        |
| 5000 | Internal Server Error |

## Rate Limits
- Default pool size: 100 concurrent tasks
- Mass task pool: 500 concurrent
- Request rate monitoring via `ReqRate`
