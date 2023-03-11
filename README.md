# API Documentation: Example RESTful API
This documentation describes the endpoints, parameters, and responses for the Example RESTful API.

## Base URL
https://example.com/api/v1/

## Authentication
The API uses an API key for authentication. To obtain an API key, please contact support@example.com.

All requests require the API key to be included in the Authorization header in the format Bearer <API Key>.

## Endpoints

## GET /users
Get a list of all users.

### Parameters
None

### Responses

#### Success Response (200 OK)

```perl
{
  "users": [
    {
      "id": 1,
      "name": "John Doe",
      "email": "john.doe@example.com"
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "email": "jane.smith@example.com"
    }
  ]
}
```

#### Error Response (401 Unauthorized)

```json
{
  "error": "Unauthorized"
}
```

## GET /users/{id}

Get information for a specific user.

### Parameters

- `id` (required) - the ID of the user to retrieve.

### Responses

#### Success Response (200 OK)

```perl
{
  "id": 1,
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```

#### Error Response (404 Not Found)

```json
{
  "error": "User not found"
}
```

## POST /users
Create a new user.

### Parameters
- `name` (required) - the name of the user.
- `email` (required) - the email address of the user.

### Responses

#### Success Response (201 Created)

```perl
{
  "id": 3,
  "name": "Bob Smith",
  "email": "bob.smith@example.com"
}
```

#### Error Response (400 Bad Request)

```json
{
  "error": "Invalid parameters"
}
```

## PUT /users/{id}
Update an existing user.

### Parameters

- `id` (required) - the ID of the user to update.
- `name` (optional) - the updated name of the user.
- `email` (optional) - the updated email address of the user.

### Responses

#### Success Response (200 OK)

```perl
{
  "id": 1,
  "name": "John Smith",
  "email": "john.smith@example.com"
}
```

#### Error Response (404 Not Found)

```json
{
  "error": "User not found"
}
```

## DELETE /users/{id}
Delete a user.

### Parameters
- `id` (required) - the ID of the user to delete.

### Responses

#### Success Response (204 No Content)
None

#### Error Response (404 Not Found)

```json
{
  "error": "User not found"
}
```

## Conclusion
This documentation provides an overview of the Example RESTful API, including its authentication method, endpoints, and responses. 
Please contact support@example.com if you have any questions or issues with the API.
