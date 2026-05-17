# Release Notes - EcoRoute API
## Version 1.1.0 (May 2026)

### 🚀 New Features
* **Rail Metric Support**: Added the `rail` enum value to the `vehicle_type` body parameter in the `/routes/optimize` endpoint. Users can now calculate logistics emissions for commercial cargo trains.

### 🛠️ Enhancements
* **Geocoding Engine Upgrade**: Upgraded the backend mapping service, reducing endpoint latency by **14%** for routes within major APAC manufacturing hubs.

### 🐛 Bug Fixes
* Fixed an issue where coordinate inputs containing trailing spaces triggered unexpected `400 Bad Request` validation errors. Trailing spaces are now automatically sanitized.
