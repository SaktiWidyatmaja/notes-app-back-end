# Notes App API

This is a backend API for a Notes App, built using Hapi.js and PostgreSQL.

## Installation

1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Rename `.env.example` to `.env` and provide the necessary environment variables.

## Getting Started

1. Run `npm start` to start the server.
2. The API will be accessible at `http://localhost:YOUR_PORT`.

## Endpoints

### Users

- `POST /users` - Register a new user.
- `GET /users/{id}` - Get details of a specific user.
- `GET /users` - Get a list of users by username.

### Notes

- `POST /notes` - Create a new note. (Protected: Requires JWT)
- `GET /notes` - Get a list of all notes. (Protected: Requires JWT)
- `GET /notes/{id}` - Get details of a specific note. (Protected: Requires JWT)
- `PUT /notes/{id}` - Update a note. (Protected: Requires JWT)
- `DELETE /notes/{id}` - Delete a note. (Protected: Requires JWT)

### Collaborations

- `POST /collaborations` - Add a collaborator to a note. (Protected: Requires JWT)
- `DELETE /collaborations` - Remove a collaborator from a note. (Protected: Requires JWT)

### Authentications

- `POST /authentications` - Perform user login and get an access token.
- `PUT /authentications` - Refresh an access token.
- `DELETE /authentications` - Revoke an access token.

## Authentication

The API uses JSON Web Tokens (JWT) for authentication. Make sure to include the JWT token in the `Authorization` header for protected routes.
