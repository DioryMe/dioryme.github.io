
# Example requests & responses - GET

GET /connections

GET /connections/123

[POST /connections & DELETE /connections/123](https://github.com/jvalanen/diory-docs/wiki)

## GET /connections?filter[from-diory-id]=1&filter[to-diory-id]=651 request
```
curl 'http://localhost:3000/v1/connections?filter[from-diory-id]=1&filter[to-diory-id]=651' \
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a' \
  -H 'Accept: application/vnd.api+json'
```

## GET /connections?filter[from-diory-id]=1&filter[to-diory-id]=651 response

{
    "data": [
        {
            "id": "876",
            "type": "connections",
            "links": {
                "self": "http://localhost:3000/v1/connections/876"
            },
            "attributes": {
                "position": {
                    "width": "20%",
                    "top": "60%",
                    "height": "20%",
                    "left": "220%"
                },
                "room-id": "(not available)",
                "created-at": "2017-12-26T16:41:05.131+02:00",
                "updated-at": "2017-12-26T16:41:05.131+02:00",
                "from-diory-id": 1,
                "to-diory-id": 651
            },
            "relationships": {
                "from-diory": {
                    "links": {
                        "self": "http://localhost:3000/v1/connections/876/relationships/from-diory",
                        "related": "http://localhost:3000/v1/connections/876/from-diory"
                    }
                },
                "to-diory": {
                    "links": {
                        "self": "http://localhost:3000/v1/connections/876/relationships/to-diory",
                        "related": "http://localhost:3000/v1/connections/876/to-diory"
                    }
                }
            }
        }
    ],
    "links": {
        "first": "http://localhost:3000/v1/connections?filter%5Bfrom-diory-id%5D=1&filter%5Bto-diory-id%5D=651&page%5Bnumber%5D=1&page%5Bsize%5D=30",
        "last": "http://localhost:3000/v1/connections?filter%5Bfrom-diory-id%5D=1&filter%5Bto-diory-id%5D=651&page%5Bnumber%5D=1&page%5Bsize%5D=30"
    }
}
```


## GET /connections/123 request
```
curl 'http://localhost:3000/v1/connections/10116' \
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

