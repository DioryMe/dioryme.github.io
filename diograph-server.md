# Diograph Server

## JSON API 1.0

This API is build with [jsonapi-resources](https://github.com/cerebris/jsonapi-resources).

This API is [JSON API 1.0](http://jsonapi.org/) compliant.

This API requires request header: ```Accept: application/vnd.api+json```

## Authentication

This API is authorization token protected.

This API uses room-id as an authentication token.

This API requires authorization token in request header, e.g. ```Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a```

## Endpoints

### Diories
```
GET /diories

GET /diories/1

POST /diories

PATCH /diories/1

DELETE /diories/1
```

[Example requests and responses](https://github.com/jvalanen/diory-docs/wiki/Reading-diories)


### Connections
```
GET /connections

GET /connections/1

POST /connections

PATCH /connections/1

DELETE /connections/1
```

[Example requests and responses](https://github.com/jvalanen/diory-docs/wiki/Reading-connections)


### Search

```
GET /search?q=home&type=place&sort=newest-first
```

Returns array of search result objects:
```
[
  {
    "id": 1,
    "value": "Diory name 1"
  },
  {
    "id": 2,
    "value": "Diory name 2"
  }
]
```

### Parameters

#### Query
```
?q=first (string)
```

#### Type
```
?type=place (place, date, check-in etc. => all the existing diory types)
```

#### Date
```
?date=2015 (string)
```

#### Sort
```
?sort=a-first (a-first, z-first, newest-first, oldest-first)
```


