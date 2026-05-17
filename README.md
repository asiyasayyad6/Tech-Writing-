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
