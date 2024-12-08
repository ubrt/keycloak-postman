# Keycloak Postman Collection

This Postman collection was generated using the official OpenAPI endpoint: [Keycloak REST API OpenAPI Specification](https://www.keycloak.org/docs-api/latest/rest-api/openapi.json).

---

## Keycloak Setup
1. **Create a Client**:
   - In Keycloak, create a new client that supports service account roles.
2. **Assign Admin Roles**:
   - Map the necessary admin roles to this client.
3. **Retrieve Credentials**:
   - Copy the `clientId` and `clientSecret` for use in the Postman environment.

## Postman Setup
1. **Import Collection and Environment**:
   - Import the provided Postman collection and example environment. Alternatively, create a custom environment.
2. **Configure Environment**:
   - Set up the environment variables for your Keycloak instance (e.g., base URL, client ID, and secret).
3. **Token Management**:
   - Leave `token` and `token_expiry` unchanged; these will be automatically managed by the pre-request script.
     
  <img width="902" alt="Postman Example" src="https://github.com/user-attachments/assets/084c581e-e00a-4dba-9e00-be2f3e8549c6">


## Using the Collection
- **Path Variables**:
   - Some requests require additional path parameters to be set in the "Params" tab under "Path Variables."
   - The `realm` parameter will be populated automatically using the environment settings.

## Pre-request Script
The pre-request script:
1. Checks if a valid token exists in the environment.
2. If not, it requests a new token using the `client_credentials` grant type.
3. Saves the new token and its expiry time in the environment variables.

