## 1. User Authentication

### Functional Requirements
- Users must be able to **register** with email, password, phone number, and role (guest/host).
- Users must be able to **log in** with valid credentials.
- System must **hash passwords** before storing in the database.
- System must support **JWT-based authentication** for secure API requests.

### API Endpoints
- `POST /api/v1/auth/register` → Create a new account
- `POST /api/v1/auth/login` → Authenticate user & return JWT
- `GET /api/v1/auth/profile` → Retrieve logged-in user profile

### Input / Output Specifications
**Register Input (JSON):**
```json
{
  "first_name": "Onyinyechi",
  "last_name": "Matthew",
  "email": "user@example.com",
  "password": "securePassword123",
  "phone_number": "08112738517",
  "role": "guest"
}

