# Squarespace Code Block Scroll Reveal

A reusable JavaScript and CSS solution that extends scroll-reveal animation behavior to custom Squarespace Code Blocks.

## What it solves

Squarespace can animate built-in page elements as they enter the viewport. However, custom HTML added through Code Blocks may not participate in the same reveal behavior.

This can create an inconsistent page experience where built-in Squarespace blocks animate during scrolling, while custom card grids and other coded elements appear immediately.

This snippet adds reveal behavior to custom coded elements so they enter the page more consistently with surrounding Squarespace content.

## How it works

The JavaScript watches elements using the `.reveal-card` class.

When an element enters the viewport, the script adds the `.is-visible` class. The CSS then transitions the element from hidden and slightly offset to fully visible.

Each element is observed only until its first reveal.

## How to use

Add the class to any custom coded element that should animate:

```html
<article class="custom-card reveal-card">
  Card content
</article>
