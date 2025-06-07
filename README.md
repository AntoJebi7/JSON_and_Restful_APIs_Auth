# 🌍 API Basics with RealTime Examples & Snippets

Learn how to work with APIs, including understanding **Base URLs**, **Endpoints**,
**Query Parameters**, **Path Parameters**, 
and handling **JSON** data in JavaScript. Real API examples from
- 🚀 Where the ISS At API: https://api.wheretheiss.at
- 🎲 Bored API: https://bored-api.appbrewery.com

---

## 📌 API Structure

BaseURL/Endpoint


**Example:**

https://api.example.com/users


- `BaseURL` → `https://api.example.com`
- `Endpoint` → `/users`

---

## 🔍 Query Parameters vs Path Parameters

### ✅ Query Parameters

Used to filter or refine the request. They come **after a `?`**, and multiple parameters are joined with `&`.

https://api.example.com/filter?type=education&participants=1


- `type=education`
- `participants=1`

### ✅ Path Parameters

Used to access a specific resource using its ID or name. They are part of the URL path.

https://api.example.com/activity/3943506



- `3943506` is a path parameter (the activity key)

---

## 🚀 Real API Examples

### 1️⃣ Where the ISS At API

📡 Get real-time location of the ISS.

- BaseURL: `https://api.wheretheiss.at/v1`
- Endpoint: `/satellites/25544`

**Try it:**

GET https://api.wheretheiss.at/v1/satellites/25544








## SERVER SIDE API REQUESTS

https://secrets-api.appbrewery.com/

### Acknowledgment

The code included in this repository is partially/entirely taken from external sources for educational purposes. Full credit goes to the original authors. This project is for learning and demonstration only, and no ownership of the original code is claimed.

If there are any issues regarding the use of this code, please feel free to reach out.


## API Links: (Suggested to use Postman)

## No Auth :
GET https://secrets-api.appbrewery.com/random

## Basic Auth :
POST https://secrets-api.appbrewery.com/register
GET https://secrets-api.appbrewery.com/all?page=1

## Api Auth :
GET https://secrets-api.appbrewery.com/generate-api-key
GET https://secrets-api.appbrewery.com/filter?score=5&apiKey= //yourapikey

## Token Based Auth :
Generates an authentication token for a user. If the user does not exist or the password is incorrect, it will return an error.
POST https://secrets-api.appbrewery.com/get-auth-token

Returns all the secrets of the authenticated user. Bearer token authentication is required.
GET https://secrets-api.appbrewery.com/user-secrets

Returns the secret with the specified ID. Bearer token authentication is required.
GET https://secrets-api.appbrewery.com/secrets/1

Adds a new secret. Bearer token authentication is required.
POST https://secrets-api.appbrewery.com/secrets

Updates the content of the secret with the specified ID. Bearer token authentication is required.
PUT https://secrets-api.appbrewery.com/secrets/1

Partially updates the content of the secret with the specified ID. Bearer token authentication is required.
PATCH https://secrets-api.appbrewery.com/secrets/1

Deletes the secret with the specified ID. Bearer token authentication is required.
DELETE https://secrets-api.appbrewery.com/secrets/1


