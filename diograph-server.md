# Diograph Server

## JSON API 1.0

This API is build with [jsonapi-resources](https://github.com/cerebris/jsonapi-resources).

This API is [JSON API 1.0](http://jsonapi.org/) compliant.

This API requires request header: ```Accept: application/vnd.api+json```

## Authentication

This API is authorization token protected.

This API uses room-id as an authentication token.

This API requires authorization token in request header, e.g. ```Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a```

## Pagination

Default pagination is 30 items per page. Maximum items per page is 100.

```
GET /diories?page[number]=3 # Returns the third page of diories (from 61-90)

GET /diories?page[size]=10 # Return only 10 items per page

GET /diories?page[size]=10&page[number]=3 # Parameters can also be combined
```

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

#### Diories filters
```
GET /diories?filter[diory_type]=place # Returns only spefic type of diories
```

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

### Search parameters

#### Query

Returns only diories that contain given string in the name.

**Accepted values:** Query string

```
?q=first
```

#### Type

Returns only diories of given type.

**Accepted values:** Any diory type: place, check-in etc.

```
?type=place
```

#### Date

Returns only date diories that contain given string in the name.

**Accepted values:** Query string

```
?date=2015
```

#### Sort

Returns diories in given order.

**Accepted values:** "a-first", "z-first", "newest-first", "oldest-first"

```
?sort=a-first
```


