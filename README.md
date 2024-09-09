# Identity Server Sample

This is a sample ASP.NET Core-based Identity Server that supports user registration and issuance of JWT tokens for authentication. This project is intended for demonstration purposes only and should not be used in production without proper security review and enhancements.

## Features

- User registration
- JWT token issuance upon successful login
- ASP.NET Core Identity for user management
- Entity Framework Core for data persistence

## Prerequisites

- .NET 6.0 SDK or later
- SQL Server (LocalDB or full instance)

## Setup

1. Clone the repository:

   ```
   git clone https://github.com/yourusername/IdentityServer.git
   cd IdentityServer
   ```

2. Update the connection string in `appsettings.json` if necessary.

3. Apply database migrations:

   ```
   dotnet ef database update
   ```

4. Run the application:
   ```
   dotnet run
   ```

## Usage

### Register a new user

Send a POST request to `/api/register` with the following JSON body:

```json
{
  "username": "newuser",
  "email": "newuser@example.com",
  "password": "StrongPassword123!"
}
```

### Obtain a JWT token

Send a POST request to `/api/token` with the following JSON body:

```json
{
  "username": "newuser",
  "password": "StrongPassword123!"
}
```

The server will respond with a JWT token if the credentials are valid.

## Security Considerations

This is a sample project and may not implement all security best practices. For production use, consider the following enhancements:

- Implement HTTPS
- Add rate limiting
- Enhance password policies
- Implement additional security headers
- Conduct a thorough security audit

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This is a sample project for demonstration purposes only. It is not intended for production use without significant security enhancements and review.
