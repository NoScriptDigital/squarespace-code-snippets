# Squarespace VideoObject Schema

A reusable JSON-LD structured data snippet for videos embedded on Squarespace pages.

## What it solves

Squarespace can display embedded videos, but the page may not automatically include all of the structured data needed to clearly describe that video to search engines.

This snippet adds `VideoObject` schema markup with key information such as:

* Video title
* Description
* Thumbnail image
* Upload date
* Embedded video URL

Adding accurate video structured data can help search engines understand the video and may improve its eligibility for video-related search features.

## Required information

Update these properties for each video:

```json
{
  "name": "Example Video Title",
  "description": "A concise description of the video.",
  "thumbnailUrl": "https://example.com/video-thumbnail.jpg",
  "uploadDate": "2026-02-26T13:59:00-07:00",
  "embedUrl": "https://player.vimeo.com/video/123456789"
}
```

## Property guidance

### `name`

Use the actual title of the video.

### `description`

Write a clear summary of what the video contains. It should match the visible video and surrounding page content.

### `thumbnailUrl`

Use a publicly accessible image URL that represents the video.

### `uploadDate`

Use the original publication date in ISO 8601 format.

Example:

```text
2026-02-26T13:59:00-07:00
```

### `embedUrl`

Use the URL for the embedded player, such as a Vimeo or YouTube embed URL.

## Squarespace implementation

Add the JSON-LD script through one of these locations:

* Page Header Code Injection for a page-specific video
* Site-wide Code Injection only when the same video appears throughout the site
* A Code Block on the page, when appropriate for the project setup

For most projects, page-level implementation is safer because the schema should only appear on pages where the video is actually visible.

## Validation

After publishing the page, test the live URL using Google’s Rich Results Test.

Also confirm that:

* The video is visible on the page
* The schema details match the visible video
* The thumbnail URL loads publicly
* The embed URL works
* The upload date is accurate

## Best used for

* Book trailers
* Course previews
* Product demonstrations
* Interviews
* Author introductions
* Portfolio videos
* Embedded Vimeo videos
* Embedded YouTube videos
* Squarespace landing pages

## Files

* `video-schema.html`

## Notes

Structured data can help search engines understand page content, but it does not guarantee a rich result.

The markup should describe content that users can actually see on the page.

This is a generalized reusable example. Client names, video titles, descriptions, URLs, and private implementation details have been removed.

