# Squarespace Navigation Link CTA Button

A reusable CSS snippet that transforms a selected Squarespace navigation link into a prominent call-to-action button across desktop and mobile menus.

## What it solves

Squarespace navigation links normally share the same visual treatment.

For some projects, one navigation item needs stronger emphasis because it represents the website’s main action, such as:

* Browse all products
* Book a consultation
* Donate
* Request a quote
* View all projects
* Get started

Squarespace may allow a separate header button in some layouts, but that button placement does not always match the desired navigation order or mobile menu structure.

This snippet styles an existing navigation link as a CTA button instead.

## Project requirement

For this implementation, the client wanted the CTA to appear as the first navigation item instead of the last.

The link order was arranged through the Squarespace Navigation panel. The CSS then transformed that selected link into a button.

On mobile, the CTA remained grouped and aligned with the other navigation links instead of appearing separately at the bottom of the menu.

## How it works

The CSS targets a navigation link by matching part of its destination URL:

```css
a[href*="browse-all-cartoon-sets"]
```

It applies the button styling to both:

```text
.header-nav-item
.header-menu-nav-item
```

This covers the desktop header navigation and the mobile menu navigation.

## Key features

* Converts an existing navigation link into a CTA button
* Works across desktop and mobile navigation
* Allows the CTA to follow the normal Squarespace navigation order
* Keeps the CTA grouped with mobile menu links
* Includes custom background, hover, and text colors
* Includes keyboard focus styling
* Uses CSS variables for easier brand customization
* Does not require JavaScript

## How to customize

Replace the URL fragment:

```css
a[href*="browse-all-cartoon-sets"]
```

with part of the destination URL for the navigation item that should become the CTA.

Examples:

```css
a[href*="donate"]
a[href*="book-now"]
a[href*="request-a-quote"]
a[href*="get-started"]
```

Update the color variables:

```css
:root {
  --nav-cta-background: #3f8f8a;
  --nav-cta-hover: #1f5f5b;
  --nav-cta-text: #ffffff;
  --nav-cta-radius: 3px;
}
```

## Navigation order

This CSS does not reorder navigation items.

To place the CTA first, move the corresponding page or link into the first position inside the Squarespace Navigation panel.

The CSS will style the link wherever Squarespace places it.

## Best used for

* Primary navigation CTAs
* Product or collection links
* Donation links
* Booking links
* Quote request links
* Portfolio collection links
* Desktop and mobile Squarespace menus
* Projects where the CTA must stay within the normal menu order

## Files

* `styles.css`

## Squarespace implementation

Add the CSS through:

```text
Design → Custom CSS
```

Confirm that the URL fragment in the CSS matches the actual navigation link.

Test the result in:

* Desktop navigation
* Tablet widths
* Mobile menu
* Hover states
* Keyboard focus states

## Notes

Squarespace header markup can vary between templates, header layouts, and platform updates.

This is a generalized reusable example. Client names, website URLs, brand details, and private project information have been removed.

