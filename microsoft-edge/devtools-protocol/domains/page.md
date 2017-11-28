#  Page Domain
Sample page domain for edp proxy, enables doing samply things. 

| | |
|-|-|
| [Types](#types) | [FrameId](#frameid) |
| [Commands](#commands) |  |
| [Events](#events) | |


## Types

### Timestamp `number`
Number of seconds since epoch.

### Headers `object`
Request / response headers as keys /values of Json object.

### ConnectionType `string`
Loading priority of a resource request.

##### Allowed Values
none, cellular2g, cellular3g, cellular4g, bluetooth, ethernet, wifi, wimax, other

### Request `object`
HTTP request data.

| Properties | | |
|-|-|-|
| typeId <br/> *optional*, *experimental* | `string` | A big description again. |
| anotherThing | `string` <br/> *Allowed values: x y z* | A big description that maybe is not useful. |


### <a id="frameid"></a> FrameId `string`
Unique loader identifier.