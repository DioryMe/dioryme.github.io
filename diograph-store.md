# Diograph Store

Easy-to-use API for Diograph API. Read, write and connect diories without manual REST requests. Build your Diograph app without a hassle.

## Install

```
npm install diograph-store
```

## Example

```
import { DiographStore } from "diograph-store"

DiographStore.setAuthToken("my-own-token")

DiographStore.getAllDiories().then(res => {
    console.log(res)
})
```

## Usage / API

### DiographStore.getDiory(id)

Retrieve diory from Diograph API.

Current diory interface:
```
  id: string;
  name: string;
  url: string;
  type: string;
  background: string;
  date: string;
  geo: {
    type: string,
    latitude: string,
    longitude: string,
    geoRadius: string
  };
  connectedDiories = Array<Diory>;
```

Returns Promise\<Diory>.

### DiographStore.getAllDiories(type\*)

Retrieve all diories with given type from Diograph API. Returns all diories with any type if type is not given.

Returns Promise\<Array\<Diory\>\>.

\* optional parameter

### DiographStore.createDiory(obj)

Create a new diory.

Object given as a parameter could look like this:
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

### DiographStore.createAndConnectDiory(obj, fromDioryId)

Creates a new diory and connects it to another diory.

Object given as a parameter is the same as in "DiographStore.createDiory()".

Returns Promise\<ConnectionObject>.

```
{
  "connection": <Connection>,
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DiographStore.createAndConnectDioryStrongly(obj, fromDioryId)

Creates a new diory and connects it to another diory from both sides.

Object given as a parameter is the same as in "DiographStore.createDiory()".

Returns Promise\<ConnectionObject>.

```
{
  "connection": <Connection>,
  ("reversedConnection": <Connection>,) <= not yet implemented
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DiographStore.connectDiories(fromDioryId, toDioryId)

Connects two diories.

Returns Promise\<ConnectionObject>.

```
{
  "connection": <Connection>,
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DiographStore.updateDiory(id, obj)

Updates the attributes of the diory.

Object given as a parameter is the same as in "DiographStore.createDiory()".

Returns Promise\<Diory>


### DiographStore.deleteDiory(id)

Deletes a diory.

Returns Promise\<void>.


**=== Nothing under this line have been implemented yet ===**


### DiographStore.connectDioriesStrongly(fromDioryId, toDioryId)

Connects two diories from both sides.

Returns Promise\<ConnectionObject>.

```
{
  "connection": <Connection>,
  "reversedConnection": <Connection>,
  "fromDiory": <Diory>,
  "toDiory": <Diory>
}
```

### DiographStore.demoteDiories(fromDioryId, toDioryId)

Deletes connection between two diories.

Returns Promise\<void>.


### DiographStore.demoteDioriesStrongly(fromDioryId, toDioryId)

Deletes connection of two diories from both sides.

Returns Promise\<void>.
