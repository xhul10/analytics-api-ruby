# OpenapiClient::GetAnalyticsReportResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account** | **String** | the Video Cloud account id |  |
| **item_count** | **Integer** | the total number of items matching the request |  |
| **items** | [**Array&lt;Items&gt;**](Items.md) | array of analytics objects for the videos returned |  |
| **summary** | [**Summary**](Summary.md) |  |  |
| **video_engagement_1** | **Float** | number of views at the 1% point of the video duration for all videos |  |
| **video_engagement_25** | **Float** | number of views at the 25% point of the video duration for all videos |  |
| **video_engagement_50** | **Float** | number of views at the 50% point of the video duration for all videos |  |
| **video_engagement_75** | **Float** | number of views at the 75% point of the video duration for all videos |  |
| **video_engagement_100** | **Float** | number of views at the 100% point of the video duration for all videos |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::GetAnalyticsReportResponse.new(
  account: null,
  item_count: null,
  items: null,
  summary: null,
  video_engagement_1: null,
  video_engagement_25: null,
  video_engagement_50: null,
  video_engagement_75: null,
  video_engagement_100: null
)
```

