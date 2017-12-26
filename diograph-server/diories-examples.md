
# Example requests & responses

GET /diories request

GET /diories response

GET /diories/1 request

GET /diories/1 response

[POST /diories & PATCH /diories/123 & DELETE /diories/123](https://github.com/jvalanen/diory-docs/wiki)

## GET /diories request

```
curl 'http://localhost:3000/v1/diories/' \
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a' \
  -H 'Accept: application/vnd.api+json'
```

## GET /diories response

```
200 - OK

{
  "data": [
    {
      "id": "1",
      "type": "diories",
      "links": {
        "self": "http://localhost:3000/v1/diories/1"
      },
      "attributes": {
        "diory-id": "diomber-diory-diomber-diory-775",
        "room-id": "5e423f7c-8545-4ae9-ad7d-634a7f00e03a",
        "version": "0.1.9",
        "diory-type": "image",
        "name": "2015-05-31 13.44.36.jpg",
        "address": null,
        "background": "http://diomber.s3.amazonaws.com/U2nZocL5JjP8KfF7GvOqt9zEwxMah3k6.jpg",
        "geo": {
          "type": "GeoCircle",
          "latitude": null,
          "longitude": null,
          "geoRadius": "50"
        },
        latitude: null,
        longitude: null,
        "date": null,
        "created": "2015-05-31T13:45:06+03:00",
        "modified": "2015-05-31T13:45:06+03:00",
        "data": { }
      },
      "relationships": {
        "connections": {
          "links": {
            "self": "http://localhost:3000/v1/diories/1/relationships/connections",
            "related": "http://localhost:3000/v1/diories/1/connections"
          }
        },
        "connected-diories": {
          "links": {
            "self": "http://localhost:3000/v1/diories/1/relationships/connected-diories",
            "related": "http://localhost:3000/v1/diories/1/connected-diories"
          }
        },
        "room": {
          "links": {
            "self": "http://localhost:3000/v1/diories/1/relationships/room",
            "related": "http://localhost:3000/v1/diories/1/room"
          }
        }
      }
    },
    { ... },
    { ... }
  ],
  "links": {
    "first": "http://localhost:3000/v1/diories?filter%5Broom_id%5D=df548369-d0a2-4ca5-b28a-dd4fb14c1f08&page%5Bnumber%5D=1&page%5Bsize%5D=30",
    "last": "http://localhost:3000/v1/diories?filter%5Broom_id%5D=df548369-d0a2-4ca5-b28a-dd4fb14c1f08&page%5Bnumber%5D=1&page%5Bsize%5D=30"
  }
}
```

## /diories/1 request

```
curl 'http://localhost:3000/v1/diories/1'
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a'
  -H 'Accept: application/vnd.api+json'
```

## /diories/1 response

```
200 - OK

{
  "data": {
    "id": "1",
    "type": "diories",
    "links": {
      "self": "http://localhost:3000/v1/diories/1"
    },
    "attributes": {
      "diory-id": "diomber-diory-diomber-diory-775",
      "room-id": "5e423f7c-8545-4ae9-ad7d-634a7f00e03a",
      "version": "0.1.9",
      "diory-type": "image",
      "name": "2015-05-31 13.44.36.jpg",
      "address": null,
      "background": "http://diomber.s3.amazonaws.com/U2nZocL5JjP8KfF7GvOqt9zEwxMah3k6.jpg",
      "geo": {
        "type": "GeoCircle",
        "latitude": null,
        "longitude": null,
        "geoRadius": "50"
      },
      latitude: null,
      longitude: null,
      "date": null,
      "created": "2015-05-31T13:45:06+03:00",
      "modified": "2015-05-31T13:45:06+03:00",
      "data": { }
    },
    "relationships": {
      "connections": {
        "links": {
          "self": "http://localhost:3000/v1/diories/1/relationships/connections",
          "related": "http://localhost:3000/v1/diories/1/connections"
        },
        "data": [
          {
            "type": "connections",
            "id": "11343"
          },
          {
            "type": "connections",
            "id": "11344"
          }
        ]
      },
      "connected-diories": {
        "links": {
          "self": "http://localhost:3000/v1/diories/1/relationships/connected-diories",
          "related": "http://localhost:3000/v1/diories/1/connected-diories"
        },
        "data": [
          {
            "type": "diories",
            "id": "3649"
          },
          {
            "type": "diories",
            "id": "3650"
          }
        ]
      },
      "room": {
        "links": {
          "self": "http://localhost:3000/v1/diories/1/relationships/room",
          "related": "http://localhost:3000/v1/diories/1/room"
        }
      }
    }
  },
  "included": [
    {
      "id": "11343",
      "type": "connections",
      "links": {
        "self": "http://localhost:3000/v1/connections/11343"
      },
      "attributes": {
        "position": {
          "width": "20%",
          "top": "60%",
          "height": "20%",
          "left": "220%"
        },
        "room-id": "diomber-rooms-1",
        "created-at": "2016-11-22T12:08:31.190+02:00",
        "updated-at": "2016-11-22T12:08:31.190+02:00",
        "from-diory-id": 1,
        "to-diory-id": 3649
      },
      "relationships": {
        "from-diory": {
          "links": {
            "self": "http://localhost:3000/v1/connections/11343/relationships/from-diory",
            "related": "http://localhost:3000/v1/connections/11343/from-diory"
          }
        },
        "to-diory": {
          "links": {
            "self": "http://localhost:3000/v1/connections/11343/relationships/to-diory",
            "related": "http://localhost:3000/v1/connections/11343/to-diory"
          }
        }
      }
    },
    {
      "id": "11344",
      "type": "connections",
      "links": {
        "self": "http://localhost:3000/v1/connections/11344"
      },
      "attributes": {
        "position": {
          "width": "20%",
          "top": "60%",
          "height": "20%",
          "left": "220%"
        },
        "room-id": "diomber-rooms-1",
        "created-at": "2016-11-22T12:08:31.201+02:00",
        "updated-at": "2016-11-22T12:08:31.201+02:00",
        "from-diory-id": 1,
        "to-diory-id": 3650
      },
      "relationships": {
        "from-diory": {
          "links": {
            "self": "http://localhost:3000/v1/connections/11344/relationships/from-diory",
            "related": "http://localhost:3000/v1/connections/11344/from-diory"
          }
        },
        "to-diory": {
          "links": {
            "self": "http://localhost:3000/v1/connections/11344/relationships/to-diory",
            "related": "http://localhost:3000/v1/connections/11344/to-diory"
          }
        }
      }
    },
    {
      "id": "3649",
      "type": "diories",
      "links": {
        "self": "http://localhost:3000/v1/diories/3649"
      },
      "attributes": {
        "diory-id": "diomber-diory-diomber-diory-775",
        "room-id": "5e423f7c-8545-4ae9-ad7d-634a7f00e03a",
        "version": "0.1.9",
        "diory-type": "thing",
        "name": "Sunday - May 31",
        "address": null,
        "background": null,
        "geo": {
          "type": "GeoCircle",
          "latitude": null,
          "longitude": null,
          "geoRadius": "50"
        },
        latitude: null,
        longitude: null,
        "date": null,
        "created": "2015-05-31T13:45:06+03:00",
        "modified": "2015-05-31T13:45:06+03:00",
        "data": { }
      },
      "relationships": {
        "connections": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3649/relationships/connections",
            "related": "http://localhost:3000/v1/diories/3649/connections"
          }
        },
        "connected-diories": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3649/relationships/connected-diories",
            "related": "http://localhost:3000/v1/diories/3649/connected-diories"
          }
        },
        "room": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3649/relationships/room",
            "related": "http://localhost:3000/v1/diories/3649/room"
          }
        }
      }
    },
    {
      "id": "3650",
      "type": "diories",
      "links": {
        "self": "http://localhost:3000/v1/diories/3650"
      },
      "attributes": {
        "diory-id": "diomber-diory-diomber-diory-775",
        "room-id": "5e423f7c-8545-4ae9-ad7d-634a7f00e03a",
        "version": "0.1.9",
        "diory-type": "event",
        "name": "Kahvila Runo - Sunday - May 31",
        "address": null,
        "background": null,
        "geo": {
          "type": "GeoCircle",
          "latitude": null,
          "longitude": null,
          "geoRadius": "50"
        },
        latitude: null,
        longitude: null,
        "date": null,
        "created": "2015-05-31T13:45:06+03:00",
        "modified": "2015-05-31T13:45:06+03:00",
        "data": { }
      },
      "relationships": {
        "connections": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3650/relationships/connections",
            "related": "http://localhost:3000/v1/diories/3650/connections"
          }
        },
        "connected-diories": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3650/relationships/connected-diories",
            "related": "http://localhost:3000/v1/diories/3650/connected-diories"
          }
        },
        "room": {
          "links": {
            "self": "http://localhost:3000/v1/diories/3650/relationships/room",
            "related": "http://localhost:3000/v1/diories/3650/room"
          }
        }
      }
    }
  ]
}
```

