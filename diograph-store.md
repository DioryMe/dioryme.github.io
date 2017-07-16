# Diograph Store

Javascript library to make it as easy as possible for you to build Diograph apps.
Makes it easy to read and write diories and connections on Diograph Server through Javascript API instead of REST requests.

## Install

```
npm install diograph-store --save-dev
```

## Example

```
import DiographStore from "diograph-store"

DiographStore.setAuthToken("my-own-token")

DiographStore.getAll().then(res => {
    console.log(res)
})
```

## Usage / API

### DS.get(id)

Retrieve diory from Diograph API.

Returns Promise\<Diory>.

### DS.getAll(type)

Retrieve all diories with given type from Diograph API.

Returns Promise\<Array\<Diory\>\>.

### DS.create(obj)

Create a new diory.

Object given as attribute could look like this:
```
{
  "name": "My first diory",
  "address": "http://dioryme.github.io",
  "diory-type": "webpage",
  "background": null,
  "date": "05/01/2017"
}
```

Returns Promise\<Diory>

### DS.update(id, obj)

Updates the attributes of the diory.

```
DS.update(123, {
  "name": "New name"
})
```

Returns Promise\<Diory>.

### DS.delete(id)

Deletes a diory.

Returns Promise\<void>.


**=== Everything under this line hasn't been implemented yet ===**

### DS.connect(fromDioryId, toDioryId)

Connects two diories.

Returns Promise\<Object>.

```
{
  "connection": <Connection>,
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DS.createAndConnect(obj, fromDioryId)

Creates a new diory and connects it to another diory.

Object given as attribute could look the same as in "DS.create()".

Returns Promise\<Object>.

```
{
  "connection": <Connection>,
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DS.demote(relatedDiory, dioryInFocus)

Deletes connection between two diories.

Returns Promise\<Connection> (???).
