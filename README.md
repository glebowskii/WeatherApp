# WeatherApp

An ASP.NET Core web application that lets you save locations you care about and track weather in them.

## Features
- Uses Entity Framework Core as ORM (with migrations)
- Uses PostgreSQL for data storage
- Containerized with Docker Compose, including the database and pgAdmin for convenient DB management
- Uses the [weatherapi](https://www.weatherapi.com/) API to fetch up-to-date weather data
- User authentication based on JWT


## API

The service is exposed via a REST API.

[View the API on SwaggerHub.](https://app.swaggerhub.com/apis/echpochmak31/weather-app-api/v1)


## Description
First, the user registers with an email and password.
After that, they receive a JWT token, can authenticate, and get access to the following functionality:

- Get current weather information via weatherapi
- Look up locations via weatherapi (useful when multiple locations share the same name, e.g. Paris)
- Create groups that contain multiple locations (a user can have multiple groups)
- Retrieve the list of groups for a user
- Retrieve weather information for all locations across all user groups
- Weather data for locations stored in the database is updated periodically

