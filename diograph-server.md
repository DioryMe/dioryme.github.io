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

## Filters

Filters the endpoint responses.

By diory-type:
```
# Returns only spefic type of diories
GET /diories?filter[diory-type]=place
```


## API V1 endpoints

### Diories
```
GET /diories

GET /diories/1
GET /diories/1.dg
GET /diories/abc123de-4567-abcd-efge-123abc456def
GET /diories/abc123de-4567-abcd-efge-123abc456def.dg

POST /diories

PUT /diories/1

DELETE /diories/1
```

[Example requests and responses](diograph-server/diories-examples.html)


### Connections
```
GET /connections?filter[from-diory-id]=1&filter[to-diory-id]=651

GET /connections/1
GET /connections/0644cca6-8d54-451f-8560-9a1d4da60ff5

POST /connections

PUT /connections/1

DELETE /connections/1
```

[Example requests and responses](diograph-server/connections-examples.html)

### Dataobjects
```
GET /dataobjects?filter[md5]=ij309g43g3ijg380jg&filter[file-size]=643554

POST /dataobjects
```

[Example requests and responses](diograph-server/dataobjects-examples.html)


### Diograph
```
GET /diograph
```

[Example requests and responses](diograph-server/diograph-examples.html)


### Search

```
GET /search?q=home&type=place&sort=newest-first
```

[Example queries and responses](diograph-server/search-examples.html)
