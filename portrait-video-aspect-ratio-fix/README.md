# Squarespace Portrait Video Aspect Ratio Fix

A reusable CSS snippet that restores portrait videos to their original 9:16 aspect ratio inside the native Squarespace Video Block.

## What it solves

Videos recorded vertically on a phone are commonly created in a 9:16 portrait format.

When a portrait video is uploaded to a Squarespace Video Block, Squarespace may display it inside a standard landscape-style player. This can make the video appear smaller than intended and create empty or dark bands around the sides.

The native Video Block does not provide a setting for manually defining the video player’s aspect ratio.

This CSS forces the Squarespace player, video wrapper, and video element to use a 9:16 aspect ratio so the portrait video displays at its intended size and orientation.

## How it works

The CSS targets the Squarespace Video Block and its Plyr video player elements:

```text
.video-block .plyr
.video-block .plyr__video-wrapper
.video-block video
```

It then applies:

```css
aspect-ratio: 9 / 16;
width: 100%;
height: auto;
```

The video wrapper background is made transparent, and the video is fitted inside the portrait frame.

## Key features

* Restores portrait video dimensions
* Uses the original 9:16 mobile video ratio
* Removes the landscape-style presentation
* Reduces unnecessary side bands
* Works with the native Squarespace Video Block
* Requires CSS only
* Maintains responsive width
* Can preserve the full video without cropping

## Files

* `styles.css`

## Squarespace implementation

Add the CSS through:

```text
Design → Custom CSS
```

The rule will apply to Squarespace Video Blocks using the matching `.video-block` and Plyr player markup.

Test the video on desktop, tablet, and mobile after publishing.

## Object-fit options

To preserve the full video without cropping, use:

```css
object-fit: contain !important;
```

To completely fill the portrait frame, use:

```css
object-fit: cover !important;
```

The `cover` option may crop part of the video when the source dimensions do not perfectly match the player ratio.

## Customization

For a different portrait ratio, update:

```css
aspect-ratio: 9 / 16 !important;
```

For example, a 4:5 video would use:

```css
aspect-ratio: 4 / 5 !important;
```

## Best used for

* Phone-recorded portrait videos
* Coaching and wellness websites
* Personal-brand videos
* Vertical demonstrations
* Short-form video clips
* Author or speaker introductions
* Mobile-first video content
* Squarespace Video Blocks

## Compatibility notes

Squarespace may change its internal Video Block or Plyr markup over time.

Confirm that the selectors still match the published video player before relying on the snippet across multiple projects.

## Notes

This is a generalized reusable example.

Client names, project-specific class names, video files, URLs, branding, and private implementation details have been removed.

