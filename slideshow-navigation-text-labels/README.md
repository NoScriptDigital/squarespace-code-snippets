# Squarespace Slideshow Navigation Text Labels

A reusable CSS snippet that adds visible “Previous” and “Next” text labels to Squarespace slideshow navigation buttons while preserving the built-in arrow icons.

Because some Squarespace slideshow and gallery components use similar control markup, the selectors may also work with compatible gallery navigation buttons.

## What it solves

Squarespace slideshow controls normally display arrow icons without visible text labels.

For some projects, the design or client requirements may call for clearer navigation controls that explicitly say:

* Previous
* Next

Squarespace does not provide a built-in setting for adding these visible text labels to slideshow navigation buttons.

This snippet uses CSS pseudo-elements to add the labels while keeping the existing Squarespace SVG arrow icons visible.

## Additional styling control

The snippet also allows the slideshow controls to use custom brand colors instead of the default Squarespace styling.

The following CSS variables control the appearance:

```css
:root {
  --slideshow-control-background: #3f948d;
  --slideshow-control-hover: #2f7670;
  --slideshow-control-text: #ffffff;
}
```

## How it works

The CSS targets slideshow buttons through their accessible `aria-label` attributes.

It supports selectors containing:

* `Previous`
* `previous`
* `Next`
* `next`

The `::after` pseudo-element adds the visible text label without replacing the existing accessible button label.

For the Next button, `flex-direction: row-reverse` places the text before the arrow so the visual order reads:

```text
Next →
```

The Previous button keeps the standard order:

```text
← Previous
```

## Key features

* Adds visible Previous and Next labels
* Preserves Squarespace SVG arrow icons
* Supports custom brand colors
* Includes hover and keyboard focus styles
* Includes responsive sizing for smaller screens
* Requires CSS only
* Does not replace the existing accessible button labels
* May also support compatible Squarespace gallery controls

## Best used for

* Squarespace slideshow blocks
* Image carousel navigation
* Compatible gallery navigation controls
* Illustration and photography websites
* Image-based portfolios
* Project slideshows
* Client-requested labeled navigation
* Designs that need clearer previous and next controls

## Files

* `styles.css`

## Squarespace implementation

Add the CSS through:

```text
Design → Custom CSS
```

The exact control markup can vary between Squarespace slideshow types, gallery types, templates, and platform updates.

Test the selectors on the specific slideshow or gallery where the snippet is being used.

## Customization

### Change the control colors

Update the CSS variables:

```css
:root {
  --slideshow-control-background: #3f948d;
  --slideshow-control-hover: #2f7670;
  --slideshow-control-text: #ffffff;
}
```

### Change the control width

```css
width: 128px !important;
min-width: 128px !important;
```

### Change the visible labels

```css
content: "Previous" !important;
content: "Next" !important;
```

### Change the typography

Update the font family, font size, font weight, letter spacing, and text transformation inside the shared text-label rule.

## Compatibility notes

This snippet was created for a Squarespace slideshow block.

Some Squarespace gallery controls may use similar `aria-label` attributes and related markup, so the same selectors can affect compatible gallery navigation buttons.

Always test the implementation on desktop, tablet, and mobile before publishing.

## Notes

This is a generalized reusable example.

Client-specific branding, site names, project copy, colors, and private implementation details have been removed or generalized.

