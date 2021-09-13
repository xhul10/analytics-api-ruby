# OpenapiClient::LiveAnalyticsApi

All URIs are relative to *https://analytics.api.brightcove.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_live_events**](LiveAnalyticsApi.md#get_live_events) | **GET** /v1/events/accounts/{account-id} | Get Live Analytics event |
| [**get_live_time_series**](LiveAnalyticsApi.md#get_live_time_series) | **GET** /v1/timeseries/accounts/{account_id} | Get Live Analytics time-series |


## get_live_events

> <GetEventsResponse> get_live_events(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, filters_for_live_analytics)

Get Live Analytics event

Provides a summary of analytics data collected for a live stream.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::LiveAnalyticsApi.new
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
account_id = 'account_id_example' # String | a Video Cloud account ID
dimensions_for_live_analytics = OpenapiClient::LiveDimensions::VIDEO # LiveDimensions | One or more dimensions to report on for Live Analytics requests Dimensions:   - video   - video, country   - video, device_type
metrics = 'video_impression' # String | Data metrics to return for live analytics requests:    - `video_impression` - the number of video impressions   - `video_view` - the number of video views   - `video_seconds_viewed` - seconds of video viewed   - `alive_ss_ad_start` - SSAI ad starts   - `fingerprint_count` - \"fingerprint\" (user) count   - `ccu` - concurrent viewers
filters_for_live_analytics = OpenapiClient::LiveWhere::COUNTRY # LiveWhere | One or more filters to limit responses for Live Analytics requests Available filters:   - video   - country   - device_type

begin
  # Get Live Analytics event
  result = api_instance.get_live_events(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, filters_for_live_analytics)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling LiveAnalyticsApi->get_live_events: #{e}"
end
```

#### Using the get_live_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetEventsResponse>, Integer, Hash)> get_live_events_with_http_info(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, filters_for_live_analytics)

```ruby
begin
  # Get Live Analytics event
  data, status_code, headers = api_instance.get_live_events_with_http_info(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, filters_for_live_analytics)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetEventsResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling LiveAnalyticsApi->get_live_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **account_id** | **String** | a Video Cloud account ID |  |
| **dimensions_for_live_analytics** | [**LiveDimensions**](.md) | One or more dimensions to report on for Live Analytics requests Dimensions:   - video   - video, country   - video, device_type |  |
| **metrics** | **String** | Data metrics to return for live analytics requests:    - &#x60;video_impression&#x60; - the number of video impressions   - &#x60;video_view&#x60; - the number of video views   - &#x60;video_seconds_viewed&#x60; - seconds of video viewed   - &#x60;alive_ss_ad_start&#x60; - SSAI ad starts   - &#x60;fingerprint_count&#x60; - \&quot;fingerprint\&quot; (user) count   - &#x60;ccu&#x60; - concurrent viewers |  |
| **filters_for_live_analytics** | [**LiveWhere**](.md) | One or more filters to limit responses for Live Analytics requests Available filters:   - video   - country   - device_type |  |

### Return type

[**GetEventsResponse**](GetEventsResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_live_time_series

> <GetTimeSeriesResponse> get_live_time_series(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, where, opts)

Get Live Analytics time-series

A time-series is defined as a an list of timestamp-value pairs representing samples of a variable (metric). The time-series API intends to allow the user to return a time-series for the set of metrics requested in the query.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::LiveAnalyticsApi.new
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
account_id = 'account_id_example' # String | a Video Cloud account ID
dimensions_for_live_analytics = OpenapiClient::LiveDimensions::VIDEO # LiveDimensions | One or more dimensions to report on for Live Analytics requests Dimensions:   - video   - video, country   - video, device_type
metrics = 'video_impression' # String | Data metrics to return for live analytics requests:    - `video_impression` - the number of video impressions   - `video_view` - the number of video views   - `video_seconds_viewed` - seconds of video viewed   - `alive_ss_ad_start` - SSAI ad starts   - `fingerprint_count` - \"fingerprint\" (user) count   - `ccu` - concurrent viewers
where = OpenapiClient::LiveWhere::COUNTRY # LiveWhere | one or more 'dimension==value' pairs to filter the results; for live, the only available filters are `country`, `device-type`, and `video`
opts = {
  bucket_limit: 10, # Integer | 'Max number of points to be returned for a time-series'
  bucket_duration: '5m', # String | 'Intervals duration in the form of an integer plus `m` (minutes), `h` (hours), or `d` (days)'
  from: TODO, # OneOfstringinteger | 'Start time for the period covered by the report — epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)'
  to: TODO # OneOfstringinteger | End time for the period covered by the report — `now` or epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)
}

begin
  # Get Live Analytics time-series
  result = api_instance.get_live_time_series(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, where, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling LiveAnalyticsApi->get_live_time_series: #{e}"
end
```

#### Using the get_live_time_series_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetTimeSeriesResponse>, Integer, Hash)> get_live_time_series_with_http_info(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, where, opts)

```ruby
begin
  # Get Live Analytics time-series
  data, status_code, headers = api_instance.get_live_time_series_with_http_info(content_type, authorization, accept_encoding, account_id, dimensions_for_live_analytics, metrics, where, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetTimeSeriesResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling LiveAnalyticsApi->get_live_time_series_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **account_id** | **String** | a Video Cloud account ID |  |
| **dimensions_for_live_analytics** | [**LiveDimensions**](.md) | One or more dimensions to report on for Live Analytics requests Dimensions:   - video   - video, country   - video, device_type |  |
| **metrics** | **String** | Data metrics to return for live analytics requests:    - &#x60;video_impression&#x60; - the number of video impressions   - &#x60;video_view&#x60; - the number of video views   - &#x60;video_seconds_viewed&#x60; - seconds of video viewed   - &#x60;alive_ss_ad_start&#x60; - SSAI ad starts   - &#x60;fingerprint_count&#x60; - \&quot;fingerprint\&quot; (user) count   - &#x60;ccu&#x60; - concurrent viewers |  |
| **where** | [**LiveWhere**](.md) | one or more &#39;dimension&#x3D;&#x3D;value&#39; pairs to filter the results; for live, the only available filters are &#x60;country&#x60;, &#x60;device-type&#x60;, and &#x60;video&#x60; |  |
| **bucket_limit** | **Integer** | &#39;Max number of points to be returned for a time-series&#39; | [optional] |
| **bucket_duration** | **String** | &#39;Intervals duration in the form of an integer plus &#x60;m&#x60; (minutes), &#x60;h&#x60; (hours), or &#x60;d&#x60; (days)&#39; | [optional] |
| **from** | [**OneOfstringinteger**](.md) | &#39;Start time for the period covered by the report — epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;)&#39; | [optional] |
| **to** | [**OneOfstringinteger**](.md) | End time for the period covered by the report — &#x60;now&#x60; or epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;) | [optional] |

### Return type

[**GetTimeSeriesResponse**](GetTimeSeriesResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

