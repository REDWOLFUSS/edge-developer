#  Sample Domain
Sample domain for edp proxy, enables doing samply things. 

| | |
|-|-|
| [Types](#types) | [LoaderId](#loaderid), [Timestamp](#timestamp), [Headers](#headers), [ConnectionType](#connectiontype), [Request](#request) |
| [Commands](#commands) | [enable](#enable), [getResponseBody](#getresponsebody), [clearBrowserCache](#clearbrowsercache) |
| [Events](#events) | [requestWillBeSent](#requestwillbesent), [loadingFinished](#loadingfinished) |


## Types

### <a id="loaderid"></a> LoaderId `string`
Unique loader identifier.

### <a id="timestamp"></a> Timestamp `number`
Number of seconds since epoch.

### <a id="headers"></a> Headers `object`
Request / response headers as keys /values of Json object.

### <a id="connectiontype"></a> ConnectionType `string`
Loading priority of a resource request.

##### Allowed Values
none, cellular2g, cellular3g, cellular4g, bluetooth, ethernet, wifi, wimax, other

### <a id="request"></a> Request `object`
HTTP request data.

</p>
| Properties | | |
|-|-|-|
| typeId <br/> *optional* | `string` | A big description again. ***Experimental***|
| anotherThing | `string` <br/> *Allowed values: x y z* | A big description that maybe is not useful. |


## Commands

### enable
Enables network tracking, network events will now be delieved to the client.

</p>
| Parameters | | |
|-|-|-|
| maxTotalBufferSize <br/> *optional* | `number` | | Buffer size in bytes to use when prserving network payloads (XHRs, etc.). ***Experimental*** |
| maxResourceBufferSize <br/> *optional* | `string` | Per-resource buffer size in bytes to use when preserving network payloads (XHRs, etc.). ***Experimental***|

### getResponseBody
Returns content served for the given request.

</p>
| Parameters | | |
|-|-|-|
| requestId | [`RequestId`](#requestid) | Identifier of the network request to get content for. |

</p>
| Returns | | |
|-|-|-|
| body| `string` | Response body. ***Experimental***|
| base64Encoded | `boolean` | True, if content was sent as base64. |

### clearBrowserCache
Clears browser cache.


## Events

### requestWillBeSent
Fired when page is about to send HTTP request.

</p>
| Parameters | | |
|-|-|-|
| requestId | [`RequestId`](#requestid) | Request identifier. |
| frameId | [`Page.FrameId`](page.md#frameid) | Frame identifier. ***Experimental*** |
| redirect <br/> *optional* | [`Response`](#response) | Redirect response data. |

### loadingFinished
Fired when HTTP request has finished loading.

</p>
| Parameters | | |
|-|-|-|
| requestId | [`RequestId`](#requestid) | Request identifier. |
| timestamp | [`Timestamp`](#timestamp) | Timestamp. |
| encodedDataLength | `number` | Total number of bytes received for this request. |