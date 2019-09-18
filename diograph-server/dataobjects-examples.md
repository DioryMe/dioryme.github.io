
# Example /dataobjects requests & responses

```
GET /dataobjects?filter[md5]=ij309g43g3ijg380jg&filter[file-size]=643554

POST /dataobjects
```


## GET /dataobjects?filter[md5]=ij309g43g3ijg380jg&filter[file-size]=643554

**Request**
```
curl 'http://localhost:3000/v1/dataobjects?filter[md5]=ij309g43g3ijg380jg&filter[file-size]=643554' \
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a' \
  -H 'Accept: application/vnd.api+json'
```

**Response**
```
200 - OK

{
   "data" : {
      "id" : "1",
      "type" : "dataobjects",
      "links" : {
         "self" : "http://localhost:3000/v1/dataobjects/1"
      },
      "attributes": {
        "id": "123-abc-asdf",
        "MD5": "ij309g43g3ijg380jg",
        "file-size": 643554,
        "s3-upload-url": "https://presignedurldemo.s3.eu-west-2.amazonaws.com/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJJWZ7B6WCRGMKFGQ%2F20180210%2Feu-west-2%2Fs3%2Faws4_request&X-Amz-Date=20180210T171315Z&X-Amz-Expires=1800&X-Amz-Signature=12b74b0788aa036bc7c3d03b3f20c61f1f91cc9ad8873e3314255dc479a25351&X-Amz-SignedHeaders=host"
      },
      "relationships" : {
         "room" : {
            "links" : {
               "self" : "http://localhost:3000/v1/dataobjects/1/relationships/room",
               "related" : "http://localhost:3000/v1/dataobjects/1/room"
            }
         }
      }
   }
}
```

## POST /dataobjects

**Request**
```
curl 'http://localhost:3000/v1/dataobjects' \
  -H 'Content-Type: application/vnd.api+json' \
  -H 'Accept: application/vnd.api+json' \
  -H 'Authorization: 5e423f7c-8545-4ae9-ad7d-634a7f00e03a' \
  --data-binary '{
      "data": {
        "attributes": {
          "id": "123-abc-asdf",
          "MD5": "ij309g43g3ijg380jg",
          "file-size": 643554,
          "s3-upload-url": "https://presignedurldemo.s3.eu-west-2.amazonaws.com/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJJWZ7B6WCRGMKFGQ%2F20180210%2Feu-west-2%2Fs3%2Faws4_request&X-Amz-Date=20180210T171315Z&X-Amz-Expires=1800&X-Amz-Signature=12b74b0788aa036bc7c3d03b3f20c61f1f91cc9ad8873e3314255dc479a25351&X-Amz-SignedHeaders=host"
        },
        "type": "dataobjects"
      }
    }'
```

**Response**
```
201 - Created

{
   "data" : {
      "id" : "1",
      "type" : "dataobjects",
      "links" : {
         "self" : "http://localhost:3000/v1/dataobjects/1"
      },
      "attributes": {
        "id": "123-abc-asdf",
        "MD5": "ij309g43g3ijg380jg",
        "file-size": 643554,
        "s3-upload-url": "https://presignedurldemo.s3.eu-west-2.amazonaws.com/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJJWZ7B6WCRGMKFGQ%2F20180210%2Feu-west-2%2Fs3%2Faws4_request&X-Amz-Date=20180210T171315Z&X-Amz-Expires=1800&X-Amz-Signature=12b74b0788aa036bc7c3d03b3f20c61f1f91cc9ad8873e3314255dc479a25351&X-Amz-SignedHeaders=host"
      },
      "relationships" : {
         "room" : {
            "links" : {
               "self" : "http://localhost:3000/v1/dataobjects/1/relationships/room",
               "related" : "http://localhost:3000/v1/dataobjects/1/room"
            }
         }
      }
   }
}
```

