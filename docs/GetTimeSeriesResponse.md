# OpenapiClient::GetTimeSeriesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **interval** | **Array&lt;Integer&gt;** | array containing the start and end points for the interval in the units specified by the &#x60;bucket_duration&#x60; parameter | [optional] |
| **dimensions** | **Object** | A set of dimension/value pairs corresponding to the dimensions specified in the &#x60;dimensions&#x60; parameter | [optional] |
| **points** | **Array&lt;Object&gt;** | An array of objects containing metrics for the points in the time-series | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::GetTimeSeriesResponse.new(
  interval: null,
  dimensions: null,
  points: null
)
```

