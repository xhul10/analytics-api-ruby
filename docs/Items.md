# OpenapiClient::Items

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ad_mode_begin** | **Integer** | number of times a player entered ad mode | [optional] |
| **ad_mode_complete** | **Integer** | number of times a player completed ad mode | [optional] |
| **bytes_delivered** | **Float** | the total bytes of data delivered, including the videos, other assets such as images and captions, and (for player reports) the player code - some of the date is obtained from CDNs and may not be available for up to 3 days | [optional] |
| **engagement_score** | **Float** | the calculated engagement score for the video | [optional] |
| **play_rate** | **Float** | video views divided by video impressions | [optional] |
| **play_request** | **Integer** | number of play requests received for a video | [optional] |
| **video** | **String** | the video id | [optional] |
| **duration** | **String** | &#39;the duration of the video in seconds (note that the duration is available only if there is at least one &#x60;video_view&#x60;)&#39; | [optional] |
| **video_engagement_1** | **Float** | number of views at the 1% point of the video duration | [optional] |
| **video_engagement_25** | **Float** | number of views at the 25% point of the video duration | [optional] |
| **video_engagement_50** | **Float** | number of views at the 50% point of the video duration | [optional] |
| **video_engagement_75** | **Float** | number of views at the 75% point of the video duration | [optional] |
| **video_engagement_100** | **Float** | number of views at the 100% point of the video duration | [optional] |
| **video_impression** | **Integer** | number of times the video was loaded in a player | [optional] |
| **name** | **String** | name of the video | [optional] |
| **video_percent_viewed** | **Float** | average percentage of the video played when viewed | [optional] |
| **video_seconds_viewed** | **Float** | total seconds of the video viewed | [optional] |
| **video_view** | **Integer** | number of times some portion of the video was viewed | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Items.new(
  ad_mode_begin: null,
  ad_mode_complete: null,
  bytes_delivered: null,
  engagement_score: null,
  play_rate: null,
  play_request: null,
  video: null,
  duration: null,
  video_engagement_1: null,
  video_engagement_25: null,
  video_engagement_50: null,
  video_engagement_75: null,
  video_engagement_100: null,
  video_impression: null,
  name: null,
  video_percent_viewed: null,
  video_seconds_viewed: null,
  video_view: null
)
```

