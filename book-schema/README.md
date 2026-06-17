# Squarespace Book Schema

A reusable JSON-LD structured data snippet for describing a book featured on a Squarespace website.

## What it solves

A Squarespace page may visually present a book, its author, and its subject matter without clearly identifying those relationships to search engines.

This snippet uses the Schema.org `Book` type to describe:

* Book title
* Book description
* Author
* Publisher
* Language
* Genre
* Book landing page URL

## How to customize

Update each property so it matches the visible book information on the page:

```json
{
  "name": "Example Book Title",
  "url": "https://example.com/book",
  "description": "A concise description of the book.",
  "inLanguage": "en",
  "genre": [
    "Parenting",
    "Mental Health"
  ]
}
```

Update the author information:

```json
{
  "@type": "Person",
  "name": "Author Name",
  "url": "https://example.com/about"
}
```

## Additional properties

When accurate information is available, the schema can also include:

* `isbn`
* `image`
* `datePublished`
* `bookEdition`
* `bookFormat`
* `sameAs`

Do not add values that have not been verified.

## Squarespace implementation

Add the JSON-LD through page-level Code Injection on the book page.

Site-wide Code Injection should only be used when the same book is genuinely relevant across the entire website.

## Validation

Test the published page using:

* Schema.org Validator
* Google Rich Results Test
* Google Search Console URL Inspection

## Files

* `book-schema.html`

## Notes

The `Book` type is valid Schema.org vocabulary, but structured data does not guarantee a special Google search appearance.

The markup should accurately describe content visible on the page.

Client names, book titles, URLs, and private project information have been removed from this reusable example.

