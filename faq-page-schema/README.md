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
