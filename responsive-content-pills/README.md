# Squarespace Responsive Content Pills

A reusable HTML and CSS layout for organizing short topics, services, features, methods, or categories into a responsive group of pill-shaped labels.

## What it solves

Squarespace Fluid Engine can be difficult to control when several small content blocks need to appear as compact, evenly spaced pills.

Building each pill as a separate block may create:

* Uneven spacing
* Inconsistent widths
* Difficult row alignment
* Excessive gaps
* Awkward wrapping
* Limited control over padding and border styling
* Poor mobile stacking

This snippet places all pills inside one flexible container so the browser can automatically organize them into balanced rows.

## How it works

The pill wrapper uses:

```css
display: flex;
flex-wrap: wrap;
```

This allows each pill to keep its natural content width while wrapping onto new rows when space becomes limited.

The gap property controls the spacing between rows and columns:

```css
gap: 12px 10px;
```

## Key features

* Flexible pill-style layout
* Automatic row wrapping
* Content-based pill widths
* Consistent padding and borders
* Responsive mobile behavior
* Customizable colors
* Subtle hover styling
* No JavaScript required
* Easier to maintain than separate Squarespace blocks

## Best used for

* Coaching methods
* Program features
* Service categories
* Areas of expertise
* Topics covered
* Skills and capabilities
* Product attributes
* Filter-style labels
* Squarespace Code Blocks

## Files

* `index.html`
* `styles.css`

## Squarespace implementation

Place the pill HTML inside a Squarespace Code Block.

Add the CSS through:

```text
Design → Custom CSS
```

The CSS may also be placed inside a `<style>` element when the layout is specific to one page.

## Customization

Update the pill labels inside the HTML:

```html
<span class="content-pill">example topic</span>
```

Add or remove as many pills as needed.

Change the visual styling through the CSS variables:

```css
:root {
  --pill-text: rgba(255, 255, 255, 0.92);
  --pill-border: rgba(255, 255, 255, 0.42);
  --pill-background: rgba(255, 255, 255, 0.02);
  --pill-hover-background: rgba(255, 255, 255, 0.08);
}
```

Adjust the pill shape by changing:

```css
border-radius: 999px;
```

Use a smaller value for rounded rectangles instead of full pills.

## Responsive behavior

On desktop, pills stay on one row when space allows and wrap naturally as needed.

On smaller screens, the padding and font size are reduced, and longer labels can wrap inside each pill.

## Notes

This is a generalized reusable example.

Client-specific names, copy, brand colors, project language, and private implementation details have been removed or replaced.

## Live Preview

View the demo here:

https://noscriptdigital.github.io/squarespace-code-snippets/responsive-content-pills/


