# OpenapiClient::AnalyticsReportApi

All URIs are relative to *https://analytics.api.brightcove.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_analytics_report**](AnalyticsReportApi.md#get_analytics_report) | **GET** /v1/data | Get Analytics Report |
| [**get_available_date_range**](AnalyticsReportApi.md#get_available_date_range) | **GET** /v1/data/status | Get Available Date Range |


## get_analytics_report

> <GetAnalyticsReportResponse> get_analytics_report(content_type, authorization, accept_encoding, accounts, dimensions, where, opts)

Get Analytics Report

Get an analytics report on one or more dimensions. Note that the fields returned in the response will vary according to the dimension(s) requested and the fields specified in the fields parameter. See [the API Overview](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) and the dimension guides for details.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::AnalyticsReportApi.new
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
accounts = 'accounts_example' # String | One or more account ids, separated by commas
dimensions = OpenapiClient::Dimensions::ACCOUNT # Dimensions | One or more dimensions to report on; see [Multiple Dimensions](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) or which combined dimensions are supported  Dimensions:   - account   - browser_type   - city   - country   - date   - date_hour   - destination_domain   - destination_path   - device_os   - device_manufacturer   - device_type   - live_stream   - player   - referrer_domain   - region   - search_terms   - social_platform   - source_type   - video
where = OpenapiClient::LiveWhere::COUNTRY # LiveWhere | one or more 'dimension==value' pairs to filter the results; for live, the only available filters are `country`, `device-type`, and `video`
opts = {
  limit: 10, # Integer | Number of items to return
  offset: 10, # Integer | Number of items to skip
  sort: 'video_view', # String | Field to sort results by (prefix with `-` for descending order)
  fields: 'video_view, video_impression, video.name', # String | Fields to return - available fields varies according to the dimensions - see the [Overview: Analytics API](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) for more details
  from: TODO, # OneOfstringinteger | 'Start time for the period covered by the report — epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)'
  to: TODO, # OneOfstringinteger | End time for the period covered by the report — `now` or epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)
  format: OpenapiClient::Format::CSV, # Format | format to return the results in
  reconciled: true # Boolean | if true, only reconciled data is returned; if false, only realtime data is returned; if not present, both reconciled and realtime data are returned
}

begin
  # Get Analytics Report
  result = api_instance.get_analytics_report(content_type, authorization, accept_encoding, accounts, dimensions, where, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling AnalyticsReportApi->get_analytics_report: #{e}"
end
```

#### Using the get_analytics_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAnalyticsReportResponse>, Integer, Hash)> get_analytics_report_with_http_info(content_type, authorization, accept_encoding, accounts, dimensions, where, opts)

```ruby
begin
  # Get Analytics Report
  data, status_code, headers = api_instance.get_analytics_report_with_http_info(content_type, authorization, accept_encoding, accounts, dimensions, where, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAnalyticsReportResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling AnalyticsReportApi->get_analytics_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **accounts** | **String** | One or more account ids, separated by commas |  |
| **dimensions** | [**Dimensions**](.md) | One or more dimensions to report on; see [Multiple Dimensions](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) or which combined dimensions are supported  Dimensions:   - account   - browser_type   - city   - country   - date   - date_hour   - destination_domain   - destination_path   - device_os   - device_manufacturer   - device_type   - live_stream   - player   - referrer_domain   - region   - search_terms   - social_platform   - source_type   - video |  |
| **where** | [**LiveWhere**](.md) | one or more &#39;dimension&#x3D;&#x3D;value&#39; pairs to filter the results; for live, the only available filters are &#x60;country&#x60;, &#x60;device-type&#x60;, and &#x60;video&#x60; |  |
| **limit** | **Integer** | Number of items to return | [optional][default to 10] |
| **offset** | **Integer** | Number of items to skip | [optional][default to 0] |
| **sort** | **String** | Field to sort results by (prefix with &#x60;-&#x60; for descending order) | [optional][default to &#39;video_view&#39;] |
| **fields** | **String** | Fields to return - available fields varies according to the dimensions - see the [Overview: Analytics API](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) for more details | [optional][default to &#39;&#x60;video_view&#x60; + others (varies by dimension)&#39;] |
| **from** | [**OneOfstringinteger**](.md) | &#39;Start time for the period covered by the report — epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;)&#39; | [optional] |
| **to** | [**OneOfstringinteger**](.md) | End time for the period covered by the report — &#x60;now&#x60; or epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;) | [optional] |
| **format** | [**Format**](.md) | format to return the results in | [optional] |
| **reconciled** | **Boolean** | if true, only reconciled data is returned; if false, only realtime data is returned; if not present, both reconciled and realtime data are returned | [optional][default to true] |

### Return type

[**GetAnalyticsReportResponse**](GetAnalyticsReportResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_available_date_range

> <GetAvailableDateRangeResponse> get_available_date_range(accounts, dimensions, content_type, authorization, accept_encoding, where, opts)

Get Available Date Range

Get the date range for which reconciled data is available for any Analytics API report. All parameters are allowed, but only account, dimensions, and where affect the result - all others are ignored. Note that date range for this request must fall within the available date range for the dimensions requested.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure OAuth2 access token for authorization: BC_OAuth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = OpenapiClient::AnalyticsReportApi.new
accounts = 'accounts_example' # String | One or more account ids, separated by commas
dimensions = OpenapiClient::Dimensions::ACCOUNT # Dimensions | One or more dimensions to report on; see [Multiple Dimensions](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) or which combined dimensions are supported  Dimensions:   - account   - browser_type   - city   - country   - date   - date_hour   - destination_domain   - destination_path   - device_os   - device_manufacturer   - device_type   - live_stream   - player   - referrer_domain   - region   - search_terms   - social_platform   - source_type   - video
content_type = 'content_type_example' # String | Content-Type: application/json
authorization = 'authorization_example' # String | Authorization: Bearer access_token (see Getting Access Tokens)
accept_encoding = 'accept_encoding_example' # String | Accept-Encoding: gzip (optional)
where = OpenapiClient::LiveWhere::COUNTRY # LiveWhere | one or more 'dimension==value' pairs to filter the results; for live, the only available filters are `country`, `device-type`, and `video`
opts = {
  limit: 10, # Integer | Number of items to return
  offset: 10, # Integer | Number of items to skip
  sort: 'video_view', # String | Field to sort results by (prefix with `-` for descending order)
  fields: 'video_view, video_impression, video.name', # String | Fields to return - available fields varies according to the dimensions - see the [Overview: Analytics API](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) for more details
  from: TODO, # OneOfstringinteger | 'Start time for the period covered by the report — epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)'
  to: TODO, # OneOfstringinteger | End time for the period covered by the report — `now` or epoch time in milliseconds (`1535654206775`) or a date in the format `yyyy-mm-dd` (such as `2013-09-26`)
  format: OpenapiClient::Format::CSV, # Format | format to return the results in
  reconciled: true # Boolean | if true, only reconciled data is returned; if false, only realtime data is returned; if not present, both reconciled and realtime data are returned
}

begin
  # Get Available Date Range
  result = api_instance.get_available_date_range(accounts, dimensions, content_type, authorization, accept_encoding, where, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling AnalyticsReportApi->get_available_date_range: #{e}"
end
```

#### Using the get_available_date_range_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAvailableDateRangeResponse>, Integer, Hash)> get_available_date_range_with_http_info(accounts, dimensions, content_type, authorization, accept_encoding, where, opts)

```ruby
begin
  # Get Available Date Range
  data, status_code, headers = api_instance.get_available_date_range_with_http_info(accounts, dimensions, content_type, authorization, accept_encoding, where, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAvailableDateRangeResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling AnalyticsReportApi->get_available_date_range_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **accounts** | **String** | One or more account ids, separated by commas |  |
| **dimensions** | [**Dimensions**](.md) | One or more dimensions to report on; see [Multiple Dimensions](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) or which combined dimensions are supported  Dimensions:   - account   - browser_type   - city   - country   - date   - date_hour   - destination_domain   - destination_path   - device_os   - device_manufacturer   - device_type   - live_stream   - player   - referrer_domain   - region   - search_terms   - social_platform   - source_type   - video |  |
| **content_type** | **String** | Content-Type: application/json |  |
| **authorization** | **String** | Authorization: Bearer access_token (see Getting Access Tokens) |  |
| **accept_encoding** | **String** | Accept-Encoding: gzip (optional) |  |
| **where** | [**LiveWhere**](.md) | one or more &#39;dimension&#x3D;&#x3D;value&#39; pairs to filter the results; for live, the only available filters are &#x60;country&#x60;, &#x60;device-type&#x60;, and &#x60;video&#x60; |  |
| **limit** | **Integer** | Number of items to return | [optional][default to 10] |
| **offset** | **Integer** | Number of items to skip | [optional][default to 0] |
| **sort** | **String** | Field to sort results by (prefix with &#x60;-&#x60; for descending order) | [optional][default to &#39;video_view&#39;] |
| **fields** | **String** | Fields to return - available fields varies according to the dimensions - see the [Overview: Analytics API](/analytics/getting-started/analytics-api-overview-dimensions-fields-and-parameters.html) for more details | [optional][default to &#39;&#x60;video_view&#x60; + others (varies by dimension)&#39;] |
| **from** | [**OneOfstringinteger**](.md) | &#39;Start time for the period covered by the report — epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;)&#39; | [optional] |
| **to** | [**OneOfstringinteger**](.md) | End time for the period covered by the report — &#x60;now&#x60; or epoch time in milliseconds (&#x60;1535654206775&#x60;) or a date in the format &#x60;yyyy-mm-dd&#x60; (such as &#x60;2013-09-26&#x60;) | [optional] |
| **format** | [**Format**](.md) | format to return the results in | [optional] |
| **reconciled** | **Boolean** | if true, only reconciled data is returned; if false, only realtime data is returned; if not present, both reconciled and realtime data are returned | [optional][default to true] |

### Return type

[**GetAvailableDateRangeResponse**](GetAvailableDateRangeResponse.md)

### Authorization

[BC_OAuth2](../README.md#BC_OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

