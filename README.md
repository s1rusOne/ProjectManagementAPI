# Project Management API

A robust and scalable RESTful API for managing projects, built with ASP.NET Core 8.0 and Entity Framework Core.

## Features

- CRUD operations for projects
- Swagger UI for easy API testing and documentation
- Entity Framework Core with SQL Server for data persistence
- Asynchronous programming model for improved performance

## Prerequisites

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Visual Studio Code](https://code.visualstudio.com/) or any preferred IDE
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (LocalDB is sufficient for development)

## Getting Started

1. Clone the repository:

   ```
   git clone https://github.com/s1rusOne/ProjectManagementAPI.git
   ```

2. Navigate to the project directory:

   ```
   cd ProjectManagementAPI
   ```

3. Restore dependencies:

   ```
   dotnet restore
   ```

4. Update the database:

   ```
   dotnet ef database update
   ```

5. Run the application:

   ```
   dotnet run
   ```

6. Open a web browser and navigate to `https://localhost:5001/swagger` to view the Swagger UI.

## SSL Certificate

This project uses HTTPS by default. If you encounter SSL certificate errors when running the application locally, you can:

1. Trust the development certificate by running:

   ```
   dotnet dev-certs https --trust
   ```

2. If you continue to experience issues, you can temporarily disable HTTPS redirection in `Program.cs` by commenting out the following line:

   ```csharp
   // app.UseHttpsRedirection();
   ```

   Then, access the API via `http://localhost:5000` instead.

> Note: Always use HTTPS in production environments.

## API Endpoints

- GET /api/projects - Retrieve all projects
- GET /api/projects/{id} - Retrieve a specific project
- POST /api/projects - Create a new project
- PUT /api/projects/{id} - Update an existing project
- DELETE /api/projects/{id} - Delete a project

For detailed request/response formats, please refer to the Swagger documentation when running the application.
