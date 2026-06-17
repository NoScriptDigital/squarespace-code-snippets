# Squarespace Gallery Navigation Text Labels

A reusable CSS snippet that adds visible “Previous” and “Next” text labels to Squarespace slideshow and gallery navigation buttons while preserving the built-in arrow icons.

## What it solves

Squarespace gallery and slideshow controls normally display arrow icons without visible text labels.

In some projects, the design or client requirements may call for clearer navigation controls that explicitly say:

* Previous
* Next

Squarespace does not provide a built-in setting to add these labels to the slideshow controls.

This snippet uses CSS pseudo-elements to add the text while keeping the existing Squarespace SVG arrows visible.

## Additional styling control

The snippet also allows the gallery controls to use custom brand colors instead of the default Squarespace styling.

The following CSS variables control the appearance:

```css
:root {
  --gallery-control-background: #3f948d;
  --gallery-control-hover: #2f7670;
  --gallery-control-text: #ffffff;
}
```

## How it works

The CSS targets gallery buttons through their accessible `aria-label` attributes.

It supports selectors containing:

* `Previous`
* `previous`
* `Next`
* `next`

The `::after` pseudo-element adds the visible text label.

For the Next button, `flex-direction: row-reverse` places the text before the arrow so the visual order reads:

```text
Next →
```

The Previous control keeps the standard order:

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

## Best used for

* Squarespace slideshow sections
* Gallery navigation controls
* Image-based portfolios
* Illustration and photography websites
* Project galleries
* Client-requested labeled navigation
* Designs that need clearer gallery controls

## Files

* `styles.css`

## Squarespace implementation

Add the CSS through:

```text
Design → Custom CSS
```

The exact navigation markup can vary between Squarespace gallery types and templates. Test the selectors on the specific gallery or slideshow where the snippet is being used.

## Customization

Change the control width:

```css
width: 128px !important;
min-width: 128px !important;
```

Change the labels:

```css
content: "Previous" !important;
content: "Next" !important;
```

Change the font family, size, weight, and letter spacing inside the shared text-label rule.

## Notes

This is a generalized reusable example.

Client-specific branding, site names, project copy, and private implementation details have been removed.

