# Squarespace Linked Logo Marquee

A reusable HTML and CSS snippet that creates a continuously scrolling strip of clickable publication, press, partner, or client logos.

## What it solves

Squarespace includes scrolling text effects, but it does not provide a built-in block for continuously scrolling linked images or publication logos.

This can be limiting when a website needs to display:

* Press mentions
* Publications
* Featured-in logos
* Media appearances
* Client logos
* Partner logos
* Awards
* Sponsor logos

Using separate image blocks can take too much space and does not create the continuous movement needed for a compact press strip.

This snippet creates a seamless horizontal logo marquee using HTML and CSS.

## How it works

The marquee contains two matching logo lists.

The first list contains the real interactive links.

The second list is a decorative duplicate used to create a continuous looping effect. It is hidden from assistive technology so screen-reader users do not hear every logo twice.

The CSS animation moves the track horizontally by half of its total width.

## Key features

* Continuously scrolling logo strip
* Clickable publication or partner logos
* Seamless looping effect
* Pause on hover
* Pause during keyboard interaction
* Keyboard focus styling
* Responsive logo sizing
* Edge-fade mask
* Reduced-motion support
* No JavaScript required

## Files

* `index.html`
* `styles.css`

## Squarespace implementation

Place the HTML inside a Squarespace Code Block.

Add the CSS through:

```text
Design → Custom CSS
```

The CSS can also be included inside a `<style>` element when the design should remain limited to one page.

## Adding logos

Add each interactive logo to the first list:

```html
<li>
  <a
    href="https://example.com/article"
    target="_blank"
    rel="noopener noreferrer"
    aria-label="Read the feature in Publication Name"
  >
    <img
      src="logo-file.png"
      width="220"
      height="48"
      alt="Publication Name"
    >
  </a>
</li>
```

Then add the same logo to the decorative duplicate list in the same order:

```html
<li>
  <img
    src="logo-file.png"
    width="220"
    height="48"
    alt=""
  >
</li>
```

## Customization

Update these CSS variables:

```css
:root {
  --marquee-background: #5f6275;
  --marquee-text: #ffffff;
  --marquee-gap: 64px;
  --marquee-logo-height: 48px;
  --marquee-duration: 28s;
}
```

A lower duration creates faster movement.

A higher duration creates slower movement.

## Accessibility notes

The duplicate logo list should not contain keyboard-focusable links.

The duplicate list is marked with:

```html
aria-hidden="true"
```

The primary logos use descriptive alternative text and descriptive link labels.

The animation is disabled for visitors who prefer reduced motion.

## Best used for

* Press and media sections
* Featured-in logo strips
* Partner logo sections
* Client logo marquees
* Sponsor strips
* Publication links
* Personal brands
* Authors and journalists
* Portfolio websites

## Notes

This is a generalized reusable example.

Client names, publication URLs, Squarespace asset URLs, private project details, and proprietary logo files have been removed or replaced.

## Live Preview

View the demo here:  
https://noscriptdigital.github.io/squarespace-code-snippets/linked-logo-marquee/
