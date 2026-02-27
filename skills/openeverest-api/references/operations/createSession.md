# POST /session

**Resource:** [Authentication & Authorization](../resources/Authentication-Authorization.md)
**Everest API Login**
**Operation ID:** `createSession`

This API issues a new JWT token for logging in from the Everest API.
The provided user must have the `login` capability.


## Request Body

The user credentials

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UserCredentials](../schemas/User/UserCredentials.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 429 | Too many attempts |
| 500 | Internal server error |

