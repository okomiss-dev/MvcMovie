# MVC Movie Application

A complete ASP.NET Core MVC web application for managing movie data, built following the official Microsoft tutorial. This project demonstrates fundamental MVC concepts, Entity Framework Core integration, data validation, and CRUD operations.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Tutorial Reference](#tutorial-reference)

## Overview

This is a movie management web application that allows users to:
- View a list of movies
- Add new movies
- Edit existing movies
- Delete movies
- Search and filter movies by genre and title

The application was built following the [ASP.NET Core MVC tutorial](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-8.0&tabs=visual-studio) from Microsoft Learn.

## Features

- **CRUD Operations**: Create, Read, Update, and Delete movies
- **Data Validation**: Server-side validation using data annotations
- **Search & Filter**: Search movies by title and filter by genre
- **Database Integration**: Entity Framework Core with SQLite (development) and SQL Server (production)
- **Seed Data**: Automatic database seeding with sample movie data

## Technologies Used

- **Framework**: ASP.NET Core 8.0 MVC
- **Database**: 
  - SQLite (Development)
  - SQL Server (Production)
- **ORM**: Entity Framework Core 9.0.7
- **Development Tools**:
  - Visual Studio Code 
  - Entity Framework Migrations

## Prerequisites

Before running this application, ensure you have:

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) or later
- [Visual Studio Code](https://code.visualstudio.com/) with C# extension
- SQLite (for development)
- SQL Server (for production deployment)

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd MvcMovie
   ```

2. **Install Entity Framework tools** (if not already installed):
   ```bash
   dotnet tool install --global dotnet-ef
   ```

3. **Restore dependencies**:
   ```bash
   dotnet restore
   ```

4. **Create and update the database**:
   ```bash
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```
   
   > **Note**: The first command creates a new migration, and the second creates the SQLite database file and applies the migration to set up the Movies table structure.

## Running the Application

1. **Using .NET CLI**:
   ```bash
   dotnet run
   ```

2. **Access the application**:
   - Navigate to `https://localhost:5049`
   - The application will automatically seed sample data on first run

### Migrations

To create new migrations:
```bash
dotnet ef migrations add <MigrationName>
dotnet ef database update
```

## Tutorial Reference

This project follows the complete ASP.NET Core MVC tutorial series:
1. [Get started with ASP.NET Core MVC](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-8.0)
2. [Add a controller](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/adding-controller?view=aspnetcore-8.0)
3. [Add a view](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/adding-view?view=aspnetcore-8.0)
4. [Add a model](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/adding-model?view=aspnetcore-8.0)
5. [Work with a database](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/working-with-sql?view=aspnetcore-8.0)
6. [Controller methods and views](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/controller-methods-views?view=aspnetcore-8.0)
7. [Add search](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/search?view=aspnetcore-8.0)
8. [Add validation](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/validation?view=aspnetcore-8.0)
