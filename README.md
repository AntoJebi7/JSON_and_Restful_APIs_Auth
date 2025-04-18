# 🌍 API Basics with Real Examples

Learn how to work with APIs, including understanding **Base URLs**, **Endpoints**, **Query Parameters**, **Path Parameters**, and handling **JSON** data in JavaScript. Real API examples from:
- 🚀 Where the ISS At API: https://api.wheretheiss.at
- 🎲 Bored API: https://bored-api.appbrewery.com

---

## 📌 API Structure

BaseURL/Endpoint

makefile
Copy
Edit

**Example:**

https://api.example.com/users

yaml
Copy
Edit

- `BaseURL` → `https://api.example.com`
- `Endpoint` → `/users`

---

## 🔍 Query Parameters vs Path Parameters

### ✅ Query Parameters

Used to filter or refine the request. They come **after a `?`**, and multiple parameters are joined with `&`.

https://api.example.com/filter?type=education&participants=1

pgsql
Copy
Edit

- `type=education`
- `participants=1`

### ✅ Path Parameters

Used to access a specific resource using its ID or name. They are part of the URL path.

https://api.example.com/activity/3943506

yaml
Copy
Edit

- `3943506` is a path parameter (the activity key)

---

## 🚀 Real API Examples

### 1️⃣ Where the ISS At API

📡 Get real-time location of the ISS.

- BaseURL: `https://api.wheretheiss.at/v1`
- Endpoint: `/satellites/25544`

**Try it:**

GET https://api.wheretheiss.at/v1/satellites/25544

pgsql
Copy
Edit

**Sample JSON Response:**

```json
{
  "name": "iss",
  "id": 25544,
  "latitude": 50.11496269845,
  "longitude": 118.07999954321,
  "altitude": 408.0002,
  "velocity": 27600.2,
  "visibility": "daylight",
  "footprint": 4500.34,
  "timestamp": 1689021200,
  "daynum": 2459764.5,
  "solar_lat": 20.1,
  "solar_lon": 160.2,
  "units": "kilometers"
}
2️⃣ Bored API
🎯 Get fun or useful activity suggestions.

BaseURL: https://bored-api.appbrewery.com

🔹 Get a random activity
nginx
Copy
Edit
GET https://bored-api.appbrewery.com/
🔹 Filter by type and participants (Query Parameters)
pgsql
Copy
Edit
GET https://bored-api.appbrewery.com/filter?type=education&participants=1
Sample JSON Response:

json
Copy
Edit
{
  "activity": "Read a science article",
  "type": "education",
  "participants": 1,
  "price": 0.1,
  "key": 8236510,
  "accessibility": 0.2
}
🔹 Get specific activity by key (Path Parameter)
nginx
Copy
Edit
GET https://bored-api.appbrewery.com/activity/3943506
🔁 JSON and JavaScript Objects
🔄 Convert JSON to JavaScript Object
js
Copy
Edit
const json = '{"name":"ISS","altitude":408.0002}';
const obj = JSON.parse(json);

console.log(obj.name);      // Output: ISS
console.log(obj.altitude);  // Output: 408.0002
🔄 Convert JavaScript Object to JSON
js
Copy
Edit
const data = { name: "ISS", altitude: 408.0002 };
const jsonString = JSON.stringify(data);

console.log(jsonString);
// Output: '{"name":"ISS","altitude":408.0002}'
🧪 Try It in Postman
Open Postman

Set the method to GET

Enter one of these URLs:

https://api.wheretheiss.at/v1/satellites/25544

https://bored-api.appbrewery.com/filter?type=education&participants=1

Hit Send

View the JSON response

📘 More Resources
https://jsonlint.com (Validate your JSON)

https://learning.postman.com (Postman Docs)

https://bored-api.appbrewery.com

https://wheretheiss.at/w/developer






















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


