# OpenapiClient::GetAvailableDateRangeResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reconciled_from** | **String** | the earliest date that you can use for from and get reconciled data |  |
| **reconciled_to** | **String** | &#39;the latest date that you can use for to and get reconciled data (realtime data may be available for later dates)&#39; |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::GetAvailableDateRangeResponse.new(
  reconciled_from: null,
  reconciled_to: null
)
```

