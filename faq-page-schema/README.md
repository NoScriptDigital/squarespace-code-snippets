# Squarespace FAQPage Schema

A reusable JSON-LD structured data snippet for describing visible frequently asked questions and their answers on a Squarespace page.

## What it solves

Squarespace can display FAQ content through accordion blocks, text blocks, or custom layouts, but the page may not automatically identify that content as a structured FAQ collection.

This snippet uses `FAQPage`, `Question`, and `Answer` markup to describe the visible questions and answers.

## Important implementation rule

Every question and answer included in the schema must also be visible to visitors on the page.

Do not add hidden questions, keyword variations, or answers that are not part of the published page content.

## How to customize

Each FAQ entry follows this structure:

```json
{
  "@type": "Question",
  "name": "The visible question",
  "acceptedAnswer": {
    "@type": "Answer",
    "text": "The complete visible answer."
  }
}
```

Add or remove question objects as needed.

## Squarespace implementation

Add the markup through page-level Code Injection on the page containing the matching FAQ content.

Avoid applying the same FAQ markup across unrelated pages.

## Validation

After publishing:

* Confirm every marked-up question is visible on the page
* Confirm every answer matches the visible copy
* Test the page with Schema.org Validator
* Test the page with Google Rich Results Test
* Inspect the URL through Google Search Console

## Search visibility note

FAQ structured data can help search engines and other systems understand the content.

However, valid FAQ markup does not guarantee an expanded FAQ result in Google Search. Eligibility and appearance depend on Google’s current search policies, the website, and the page content.

## Files

* `faq-schema.html`

## Notes

Use `FAQPage` when the website provides one official answer to each question.

Do not use `QAPage` unless users can submit alternative answers.

Client questions, answers, names, and private project details have been removed from this reusable example.
