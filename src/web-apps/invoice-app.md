# Invoice App

**The gist**: build an app that allows people to send invoices with line items and total to an email. Then allow the recipient to mark the invoice as paid.

Businesses who offer services need to get paid! This project could be useful to something, and that makes it appealing in a certain way that's different than "fun" projects. I could see there being space in the crowded world of invoicing software for an open source version with affordable pricing.

## Mock-Ups

## Specs

- Authentication
- Invoice creation
  - Recipient name and email
  - With line items
  - Note
- Viewing created invoices and their statuses
- Send invoice via email
- Recipient receives invoice w/ link to mark as paid
- Sender gets notified when paid and it is reflected in the app

Data model for **invoices**:

- id
- title
- note
- total
- line items (maybe just an array of title, quantity, and unit price to start)
- state - draft, sent, paid

## Extra Credit

- Wire up payments with Stripe or another payment gateway
- Store recipients to make it easy to send invoices again
