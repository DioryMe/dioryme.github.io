
# Example requests & responses - GET

GET /connections/123

[POST /connections & DELETE /connections/123](https://github.com/jvalanen/diory-docs/wiki)

## GET /connections/123 request
```
curl 'http://localhost:3000/v1/connections/' \
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a' \
  -H 'Accept: application/vnd.api+json'
```

## GET /connections/123 response

```
{
  "data": {
    "id": "10116",
    "type": "connections",
    "links": {
      "self": "http://diory-server.herokuapp.com/v1/connections/10116"
    },
    "attributes": {
      "position": {
        "width": "20%",
        "top": "60%",
        "height": "20%",
        "left": "220%"
      },
      "room-id": "(not available)",
      "created-at": "2017-08-19T20:16:51.871+03:00",
      "updated-at": "2017-08-19T20:16:51.871+03:00",
      "from-diory-id": 6507,
      "to-diory-id": 6478
    },
    "relationships": {
      "from-diory": {
        "links": {
          "self": "http://diory-server.herokuapp.com/v1/connections/10116/relationships/from-diory",
          "related": "http://diory-server.herokuapp.com/v1/connections/10116/from-diory"
        }
      },
      "to-diory": {
        "links": {
          "self": "http://diory-server.herokuapp.com/v1/connections/10116/relationships/to-diory",
          "related": "http://diory-server.herokuapp.com/v1/connections/10116/to-diory"
        }
      }
    }
  }
}
```

