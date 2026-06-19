# Squarespace Text and Logo Marquee

A reusable HTML and CSS marquee that combines short text phrases with small logos, icons, or image separators in a continuous horizontal loop.

## What it solves

Squarespace includes native scrolling text features, but the built-in options may not support the exact combination of:

* Repeated text phrases
* Brand logos
* Custom image separators
* Precise spacing
* Custom typography
* Continuous looping
* Pause-on-hover behavior

This snippet creates a fully controlled marquee that can combine branded text with small logo or image elements.

## How it works

The marquee contains two identical groups.

The second group duplicates the first group so the animation can loop continuously without leaving an empty gap.

The track moves horizontally using:

```css
animation: text-logo-marquee-scroll 24s linear infinite;
```

The animation moves the complete track by half of its width:

```css
transform: translateX(-50%);
```

## Key features

* Continuous horizontal marquee
* Supports text and image logos
* Supports text and character icons
* Seamless duplicated loop
* Responsive typography
* Responsive logo sizing
* Pause on hover
* Pause during keyboard interaction
* Reduced-motion support
* No JavaScript required

## Best used for

* Calls to action
* Brand messages
* Product launches
* Promotional phrases
* Gaming and entertainment websites
* Fashion and retail websites
* Event announcements
* Featured categories
* Brand logo separators
* Squarespace Code Blocks

## Files

* `index.html`
* `styles.css`

## Squarespace implementation

Place the HTML inside a Squarespace Code Block.

Add the CSS through:

```text
Design → Custom CSS
```

The CSS may also be included inside a `<style>` element when the marquee is used on only one page.

## Adding an image logo

Use:

```html
<img
  class="text-logo-marquee__logo"
  src="your-logo.png"
  width="48"
  height="48"
  alt=""
  aria-hidden="true"
>
```

Decorative separator logos should usually use an empty `alt` attribute.

## Using a character instead of a logo

Replace the image with:

```html
<span class="text-logo-marquee__icon" aria-hidden="true">
  ×
</span>
```

## Customization

Change the background, text, spacing, timing, and logo size through the CSS variables:

```css
:root {
  --marquee-background: #05070a;
  --marquee-border: rgba(245, 246, 248, 0.18);
  --marquee-text: #f5f6f8;
  --marquee-accent: #35ff5c;
  --marquee-gap: 2.25rem;
  --marquee-duration: 24s;
  --marquee-logo-size: 2.5rem;
}
```

A lower duration creates a faster marquee.

A higher duration creates a slower marquee.

## Important duplication rule

Whenever a phrase, logo, or icon is added to the first group, add the same item to the second group in the same order.

The two groups must remain identical for the loop to appear seamless.

## Accessibility notes

The duplicate group is marked with:

```html
aria-hidden="true"
```

This prevents screen readers from announcing the repeated content twice.

The animation is disabled for visitors who prefer reduced motion.

## Notes

This is a generalized reusable example.

Client names, phrases, brand logos, asset URLs, colors, and private project details have been removed or replaced.

## Live Preview

View the demo here:

https://noscriptdigital.github.io/squarespace-code-snippets/text-and-logo-marquee/
