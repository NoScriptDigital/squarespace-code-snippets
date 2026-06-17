# Squarespace Responsive Equipment Card Table

A responsive HTML and CSS layout that organizes compact equipment or service categories into a structured grid with the visual clarity of a table and the flexibility of individual cards.

## What it solves

Squarespace built-in blocks can be difficult to use when a section needs many small, consistently sized items arranged into precise columns and rows.

Using separate Squarespace blocks for each item may create:

* Uneven spacing
* Inconsistent card widths
* Misaligned rows
* Excessive vertical space
* Limited control over icon and label positioning
* Difficult mobile stacking

This custom layout places all category items inside one controlled grid so the cards maintain consistent spacing, sizing, alignment, and responsive behavior.

## Layout behavior

The layout displays:

* Four columns on desktop
* Two columns on tablet
* One column on smaller mobile screens

Each item appears as an individual bordered card while the complete section maintains the organized appearance of a table.

## Key features

* Compact card-table layout
* Consistent row and column spacing
* Equal-height grid rows
* Inline SVG icons
* Responsive desktop, tablet, and mobile layouts
* Hover feedback
* Customizable CSS variables
* Accessible list semantics
* No external icon library required

## Best used for

* Equipment categories
* Product categories
* Service lists
* Industries served
* Capabilities sections
* Resource directories
* Feature comparison sections
* Squarespace Code Blocks

## Files

* `index.html`
* `styles.css`

## Squarespace implementation

The category HTML can be placed inside a Squarespace Code Block.

The CSS can be added through Squarespace Custom CSS or included in the Code Block inside a `<style>` element when page-specific styling is preferred.

## Customization

Colors can be changed using the CSS variables at the top of `styles.css`:

```css
:root {
  --cs-text: #2e3235;
  --cs-muted: #6e737a;
  --cs-border: #d8dde3;
  --cs-background: #ffffff;
  --cs-link: #092445;
  --cs-hover: #f6f7f9;
}
```

Update the category names, SVG icons, link destination, and explanatory copy for each project.

## Notes

This is a generalized reusable example.

Client-specific company names, copy, URLs, brand styling, and private project details have been removed or replaced.

