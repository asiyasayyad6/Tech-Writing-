# MyGate Express Entry
## Introduction
Express Entry is a service offered by MyGate paltform for frictionless entry of partner executives into all gated communities serviced by MyGate.

The reduced friction has twofold advantage:

* Improved efficiency of the partner executives (Overall increase in the number of packages delivered by partner executives in the same time).
* Increased security and convinience for the individuals residing within the community.

### Express Entry Integration primarily involves:
* Understanding the APIs in the developer guide.
* Obtaining the sandbox credentials and familiarizing oneself with the sandbox environment.
* Code up the partner modules to interact with the APIs and consume status notifications/callbacks.
		
The integration phase typically takes not more that a week and is supported by MyGate's Partner Engineering Team. Once the integration is 
successfully completed, a 'GO LIVE' date is decided and there is a cutover to the production environment by both the partner and MyGate Platform.

**MyGate Platform supports three interrelated sets of APIs as part of Express Entry:**

* Delivery EAR APIs
* Partner Match APIs
* Geofence APIs
# Pre-Requisites
* Offline exchange of MyGate Express Entry APIs credentials is completed.
* Offline exchange of Partner Logo, POC Details. Callback URL and Callback Authentication (if any).

**To get started contact**
  partnerships@mygate.in

# Security  & Authentication
Security and Authentication for Express Entry APIs and registered Callback events.

**Express Entry**

|Authentication       | Sandbox & Production Environments |
| --------------------|-----------------------------------|
|Dashboard Login      | Username and password will be shared with partner offline. | 
| x-api-key      | Partner API access key visible on the dashboard after login.|

**Registered Callback Events**
|Authentication       | Sandbox & Production Environments |
| --------------------|-----------------------------------|
|Callback API Access Key| Header name and value to be shared by partner as part of integration|
| Callback Basic Auth| Basic authentication token to be shared by partner as part of integration|
