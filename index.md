# Diograph Documentation

Diograph Platform opens up your own data to the apps.


## Diograph Server

Simple REST API that is JSON-API compliant.

This is where your apps can make requests to read and write your information.

[Explore the documentation](diograph-server.html)

## Diograph Store

Javascript library to make it as easy as possible for you to build Diograph apps.

Your Javascript API to read and write diories and connections on Diograph Server.

[Explore the documentation](diograph-store.html)

## Diograph Authentication

To keep your information safe, Diograph Server requires an authentication token attached to the every header of your every request.

This npm package has been made to make it as easy as possible for you to implement basic authentication to your Diograph apps.

[Explore the documentation](diograph-auth.html)

## Diograph Search Create

Combined input field for searching and creating diories.
It suggests diories as search results or diories to be created.

[Explore the documentation](diograph-search-create.html)


## CHANGELOG

### 2017-08-21 - August Release

**Upgrades:**
- Diograph-store npm package => 0.0.8
- Diograph-authentication npm package => 0.0.9
- Initial search-create component => 0.0.1

**Added:**
- *CheckInApp:* Diograph-authentication in use, multiple users enabled
- *CheckInApp:* Diograph-store in use
- *DiographServer:* Sign up & sign in & initial home screen
- *DiographServer:* Pagination to diories#index
- *DiographServer:* diory_type filter
- *DiographServer:* App grid to homescreen
- *DiographServer:* Search-endpoint autentication, multiple users enabled
- *TestApp:* Search-create component
- *TestApp:* Diory components
- Documentation: https://dioryme.github.io

