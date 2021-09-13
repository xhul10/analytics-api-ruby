# OpenapiClient::Summary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ad_mode_begin** | **Integer** | Total ad mode begin events received for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **ad_mode_complete** | **Integer** | Total ad mode complete events received for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **active_media** | **Integer** | Total active videos in account(s) - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **bytes_delivered** | **Integer** | Total bytes of data delivered for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **daily_unique_viewers** | **Integer** | Total daily unique viewers for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **drm_bytes_packaged** | **Float** | Total DRM bytes packaged for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **engagement_score** | **Float** | Average engagement score for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **licenses_served** | **Integer** | Total DRM licenses serverd for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **live_seconds_streamed** | **Float** | Total second of live video streamed for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **play_rate** | **Float** | Average play rate for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **play_request** | **Integer** | Total play requests for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **player_load** | **Integer** | Total player loads for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_engagement_1** | **Float** | Average views at 1% point for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_engagement_25** | **Float** | Average views at 25% point for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_engagement_50** | **Float** | Average views at 50% point for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_engagement_75** | **Float** | Average views at 75% point for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_engagement_100** | **Float** | Average views at 100% point for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_impression** | **Integer** | Total video impressions for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |
| **video_view** | **Integer** | Total video views for all items - note that properties included in the summary vary depending on the dimension(s) and fields requested | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Summary.new(
  ad_mode_begin: null,
  ad_mode_complete: null,
  active_media: null,
  bytes_delivered: null,
  daily_unique_viewers: null,
  drm_bytes_packaged: null,
  engagement_score: null,
  licenses_served: null,
  live_seconds_streamed: null,
  play_rate: null,
  play_request: null,
  player_load: null,
  video_engagement_1: null,
  video_engagement_25: null,
  video_engagement_50: null,
  video_engagement_75: null,
  video_engagement_100: null,
  video_impression: null,
  video_view: null
)
```

