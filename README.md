# EcoRoute API Documentation 🌱

Welcome to the EcoRoute API reference and developer guide. The EcoRoute API allows logistics platforms to programmatically calculate, optimize, and report the carbon footprint of commercial shipping routes.

## Quick Start Guide

### 1. Authentication
All requests to the EcoRoute API require a Bearer token passed in the HTTP Authorization header:
```http
Authorization: Bearer YOUR_API_KEY
```
### 2. Base URL
All API requests must be directed to the following base production URL:
```http
https://api.ecoroute.com/v1
```
### 3. Endpoint: Optimize Route
```http
POST/routes/optimize
```
Calculates the most carbon-efficient path between an origin and destination based on the selected vehicle profile.

**Request Headers**

| Header | Type | Description |
|--------|------|-------------|
| ```http Content-Type``` | ```http string ```| Must be set to ``` http application/json```|
|```http Authorization``` | ```http string ```| ```http Bearer <YOUR_TOKEN>``` |

**Request Body Parameters**

- ```http origin``` (string, required): The starting geographic location or city name.
- ```http destination``` (string, required): The final delivery location or city name.
- ```http ```vehicle_type``` (string, required): Options include ```http electric_truck```, ```http diesel_heavy```, or ```http rail```.

  **Code Example: cURL Request**
  
  ```http curl -X POST [https://api.ecoroute.com/v1/routes/optimize](https://api.ecoroute.com/v1/routes/optimize) \
  -H "Authorization: Bearer eco_demo_12345" \
  -H "Content-Type: application/json" \
  -d '{
    "origin": "Mumbai, IN",
    "destination": "Pune, IN",
    "vehicle_type": "electric_truck"
  }'```

