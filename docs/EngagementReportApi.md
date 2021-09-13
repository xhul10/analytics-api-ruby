# OpenapiClient::EngagementReportApi

All URIs are relative to *https://analytics.api.brightcove.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_account_engagement**](EngagementReportApi.md#get_account_engagement) | **GET** /v1/engagement/accounts/{account_id} | Get Account Engagement |
| [**get_player_engagement**](EngagementReportApi.md#get_player_engagement) | **GET** /v1/engagement/accounts/{account_id}/players/{player_id} | Get Player Engagement |
| [**get_video_engagement**](EngagementReportApi.md#get_video_engagement) | **GET** /v1/engagement/accounts/{account_id}/videos/{video_id} | Get Video Engagement |


## get_account_engagement

> <Timeline> get_account_engagement(account_id, content_type, authorization, accept_encoding)

Get Account Engagement

Get a summary report of engagement for the account. Note:  Engagement reports are only available for periods within the past 32 days. Requests outside that range will return an error The only parameters supported for Engagement reports are from and to Engagement reports are available for single accounts only - reports on multiple accounts will not work

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::EngagementReportApi.new
account_id = 'account_id_example' # String | a Video Cloud account ID
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)

begin
  # Get Account Engagement
  result = api_instance.get_account_engagement(account_id, content_type, authorization, accept_encoding)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_account_engagement: #{e}"
end
```

#### Using the get_account_engagement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Timeline>, Integer, Hash)> get_account_engagement_with_http_info(account_id, content_type, authorization, accept_encoding)

```ruby
begin
  # Get Account Engagement
  data, status_code, headers = api_instance.get_account_engagement_with_http_info(account_id, content_type, authorization, accept_encoding)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Timeline>
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_account_engagement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | a Video Cloud account ID |  |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |

### Return type

[**Timeline**](Timeline.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_player_engagement

> <Timeline> get_player_engagement(account_id, content_type, authorization, accept_encoding, player_id)

Get Player Engagement

Get a summary report of engagement for a player. Note:  Engagement reports are only available for periods within the past 32 days. Requests outside that range will return an error The only parameters supported for Engagement reports are from and to Engagement reports are available for single accounts only - reports on multiple accounts will not work

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::EngagementReportApi.new
account_id = 'account_id_example' # String | a Video Cloud account ID
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
player_id = 'player_id_example' # String | a Video Cloud player ID

begin
  # Get Player Engagement
  result = api_instance.get_player_engagement(account_id, content_type, authorization, accept_encoding, player_id)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_player_engagement: #{e}"
end
```

#### Using the get_player_engagement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Timeline>, Integer, Hash)> get_player_engagement_with_http_info(account_id, content_type, authorization, accept_encoding, player_id)

```ruby
begin
  # Get Player Engagement
  data, status_code, headers = api_instance.get_player_engagement_with_http_info(account_id, content_type, authorization, accept_encoding, player_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Timeline>
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_player_engagement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | a Video Cloud account ID |  |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **player_id** | **String** | a Video Cloud player ID |  |

### Return type

[**Timeline**](Timeline.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_video_engagement

> <GetVideoEngagementResponse> get_video_engagement(account_id, content_type, authorization, accept_encoding, video_id)

Get Video Engagement

Get a summary report of engagement for a video. Note:  Engagement reports are only available for periods within the past 32 days. Requests outside that range will return an error The only parameters supported for Engagement reports are from and to Engagement reports are available for single accounts only - reports on multiple accounts will not work

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::EngagementReportApi.new
account_id = 'account_id_example' # String | a Video Cloud account ID
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
video_id = 'video_id_example' # String | a Video Cloud video ID

begin
  # Get Video Engagement
  result = api_instance.get_video_engagement(account_id, content_type, authorization, accept_encoding, video_id)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_video_engagement: #{e}"
end
```

#### Using the get_video_engagement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetVideoEngagementResponse>, Integer, Hash)> get_video_engagement_with_http_info(account_id, content_type, authorization, accept_encoding, video_id)

```ruby
begin
  # Get Video Engagement
  data, status_code, headers = api_instance.get_video_engagement_with_http_info(account_id, content_type, authorization, accept_encoding, video_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetVideoEngagementResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling EngagementReportApi->get_video_engagement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | a Video Cloud account ID |  |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **video_id** | **String** | a Video Cloud video ID |  |

### Return type

[**GetVideoEngagementResponse**](GetVideoEngagementResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

