# Diograph Store gem (Ruby)

Easy-to-use API for Diograph API. Read, write and connect diories without manual REST requests. Build your Diograph app without a hassle.

## Install

```
gem install diograph-store
```

## Example

```
require 'diograph-store'

diory = DiographStore.get_diory('123-abc-456')

puts diory
```

## Usage / API

Examples assumes that the following things are defined:

```
# Install gems
bundle install
# Console
irb
# Require diograph_store
require 'bundler/setup'
require 'rubygems'
require 'diograph_store'
# Define ENV's
ENV['DIOGRAPH_STORE_HOST'] = 'http://host.docker.internal:3000'
ENV['DIOGRAPH_STORE_TOKEN'] = 'testtoken'
ENV['DIOGRAPH_USER_TOKEN'] = "1"
# Create store
@store = DiographStore::DiographStore.new
```


### DiographStore#get_diory(diory_id)

Retrieve diory from Diograph API.

```
@store.get_diory('f57061f8-29d0-4000-b9e0-7b43c03305c6')
```

Returns DiographStore::Diory if diory exists.

Returns nil if diory was not found.

Otherwise an ErrorObject if there was an error.

### DiographStore#create_diory(diory_attributes)

Creates a diory.

```
diory_attributes = {
  name: "jee"
}
@store.create_diory(diory_attributes)
```

Returns DiographStore::Diory if diory was succesfully created.

Otherwise an ErrorObject if there was an error.

### DiographStore#find_or_create_diory(diory_attributes)

Tries to find a diory with given diory-id.

Returns DiographStore::Diory if diory exists.

Creates and returns DiographStore::Diory if diory wasn't found

```
diory_attributes = {
  "diory-id" => "f57061f8-29d0-4000-b9e0-7b43c03305",
  "name" => "jee"
}
@store.find_or_create_diory(diory_attributes)
```

### DiographStore#get_connection(connection_id)

```
@store.get_connection('5a5d7f80-eb8a-4c2b-a2bd-a643457a2324')
```

Returns DiographStore::Connection if connection exists.

Returns nil if connection was not found.

Otherwise an ErrorObject if there was an error.

### DiographStore#create_connection(from_diory_id, to_diory_id, connection_type)

```
@store.create_connection(
  from_diory_id: 'f57061f8-29d0-4000-b9e0-7b43c03305c6',
  to_diory_id: 'b6c60f50-333d-47e6-b53e-e8543bd66eb1',
  connection_type: 'mentions'
)
```

Returns DiographStore::Connection if connection was succesfully created.

Otherwise an ErrorObject if there was an error.


### DiographStore#update_diory_attribute

Updates given one attribute for diory

```
@store.update_diory_attribute(
  diory: @store.get_diory('f57061f8-29d0-4000-b9e0-7b43c03305c6') ,
  attribute_name: 'name',
  value: 'New name!'
)
```



### DiographStore#update_connection_attribute

Updates given attribute for connection

```
@store.update_connection_attribute(
  connection: @store.get_connection('298172b1-ae61-41ee-a06a-38b0f8087880'),
  attribute_name: 'connection-type',
  value: 'mentions'
)
```

### DiographStore#get_room

Retrieve room from Diograph API.

```
@store.get_room('testtoken')
```

Returns DiographStore::Room if room exists.

Returns nil if room was not found.

Otherwise an ErrorObject if there was an error.


### DiographStore#create_room

```
@store.create_room('f57061f8-29d0-4000-b9e0-7b43c03305c6', 'Room name')
```

Returns DiographStore::Room if room was succesfully created.

Otherwise an ErrorObject if there was an error.

