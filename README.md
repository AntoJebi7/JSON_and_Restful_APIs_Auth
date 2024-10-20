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


