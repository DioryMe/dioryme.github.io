
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
