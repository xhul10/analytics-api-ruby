# OpenapiClient::VideoDataApi

All URIs are relative to *https://analytics.api.brightcove.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_alltime_video_views**](VideoDataApi.md#get_alltime_video_views) | **GET** /v1/alltime/accounts/{account_id}/videos/{video_id} | Get Alltime Video Views |


## get_alltime_video_views

> <GetAlltimeVideoViewsResponse> get_alltime_video_views(account_id, video_id, content_type, authorization, accept_encoding)

Get Alltime Video Views

'Returns the total alltime video views for a video. This is a low-latency endpoint appropriate for use by client-side apps such as the Brightcove Player.'

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::VideoDataApi.new
account_id = 'account_id_example' # String | a Video Cloud account ID
video_id = 'video_id_example' # String | a Video Cloud video ID
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)

begin
  # Get Alltime Video Views
  result = api_instance.get_alltime_video_views(account_id, video_id, content_type, authorization, accept_encoding)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling VideoDataApi->get_alltime_video_views: #{e}"
end
```

#### Using the get_alltime_video_views_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAlltimeVideoViewsResponse>, Integer, Hash)> get_alltime_video_views_with_http_info(account_id, video_id, content_type, authorization, accept_encoding)

```ruby
begin
  # Get Alltime Video Views
  data, status_code, headers = api_instance.get_alltime_video_views_with_http_info(account_id, video_id, content_type, authorization, accept_encoding)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAlltimeVideoViewsResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling VideoDataApi->get_alltime_video_views_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | a Video Cloud account ID |  |
| **video_id** | **String** | a Video Cloud video ID |  |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |

### Return type

[**GetAlltimeVideoViewsResponse**](GetAlltimeVideoViewsResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

