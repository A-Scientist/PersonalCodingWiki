[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki/Ruby)<br>
Under Construction<br>

# Ruby Data Structures
A list of useful data structures to be used in the Ruby language. Everything from Booleans to Collection objects that automatically interface with SQL databases.

## Collections

### Array (Ordered Collection)
Used when a collection changes size dynamically<br>

#### Range (Interval)

### Set
Used to ensure element uniqueness<br>
>owners<br>
>&nbsp;&nbsp;| results |<br>
>&nbsp;&nbsp;results := Set new.<br>
>&nbsp;&nbsp;self accounts do: [:each | results add: each owner].<br>
>&nbsp;&nbsp;^results<br>

##### Equality Method

##### Hashing Method

### Hash (Dictionary)
Used to map one kind of object to another<br>
>colors<br>
>&nbsp;&nbsp;| result |<br>
>&nbsp;&nbsp;result := Dictionary new.<br>
>&nbsp;&nbsp;result<br>
>&nbsp;&nbsp;&nbsp;&nbsp;at: ‘red’<br>
>&nbsp;&nbsp;&nbsp;&nbsp;put: (Color red: 1).<br>
>&nbsp;&nbsp;result<br>
>&nbsp;&nbsp;&nbsp;&nbsp;at: ‘gray’<br>
>&nbsp;&nbsp;&nbsp;&nbsp;put: (Color brightness: 0.5).<br>
>&nbsp;&nbsp;^resuit<br>

### Temporary Sorted Collection
Used for ordering elements<br>

### Sorted Collection
used to keep element in sorted order<br>
Any collection can be sorted by sending it “asSortedCollection”<br>

## classes

## Protocols

## Idioms