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

### 2019-10-30 - Dataobjects

**Upgrades**
- diory-server => 0.8.0

**Added**
- *DioryServer:* `/v1/dataobjects` endpoint

### 2019-01-20

- DiographStore Ruby gem (extracted from Genealogy Ruby app)
- Admin tool (Ruby)
- Receipt app (Ruby)

### 2018-12-31

Genealogy Ruby app (with built-in store for API requests)

### 2018-08-12

Diograph docker environment

### 2017-12-26 - Christmas Release

**Upgrades**
- diory-server => 0.7.0

**Added**
- *DioryServer:* Connection endpoint requires from-diory-id and to-diory-id parameters to work (`"?filter[from-diory-id]=1&filter[to-diory-id]=2"`)

### 2017-10-31 - Before Winter Release

**Upgrades**
- Diograph Admin app initial release
- diograph-store npm package => 0.0.10
- diory-server => 0.6.0
- upload-image initial version

**Added**
- *DiographStore:* update diory implemented, PUT requests
- *DiographStore & DioryServer:* support for geo property (latitude & longitude)
- *DiographAdmin:* search diories with diograph-search-create component
- *DiographAdmin:* show and update diory attributes and show background image
- *UploadImage:* extract image file EXIF tag contents to image diory and upload EXIF thumbnail .tiff to S3

### 2017-09-16 Search-create mid-release

**Upgrades**
- diograph-search-create npm package => 0.0.5

**Added**
- new DiographSearchCreate as a React component

### 2017-08-21 - August Release

**Upgrades**
- Diograph-store npm package => 0.0.8
- Diograph-authentication npm package => 0.0.9
- Initial search-create component => 0.0.1
- diory-server => 0.5.0

**Added**
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

