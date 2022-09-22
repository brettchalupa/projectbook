# Restaurant Ordering Platform

The scope of this could really vary in its breadth! But the gist is to create a web app that allows restuarants to create a website that lets their patrons order online for pick-up. It would allow them to add menu items with their price and optional description.

Patrons could then view the website for the restaurant, add menu items to their order, and then pay for it to play it.

When an order is placed, the restuarant would then see in their dashboard an order has been placed. They can mark it as ready for pick up when it's been completed.

This would then notify the patron their food is ready for pick up.

I'd call this GrubBud, or maybe that's too close to the real thing. How about iMenu and get all 2000s Steve Jobs on it??? Call it what ya' want!

## Wireframes

## Concepts

- Admin for restuarant to manage their menu
- Public website for ordering w/ a cart with line items
- Payment processing
- State managing for the order with effects at various state changes (sounds like a state machine to me!)

## Scope

This is basically a full stack web app. For learning purposes, you could have it just be for one restaurant with HTTP basic auth for the Admin area. Or build out an entire sign up flow! Whatever you want.

But there's a lot to this.

If I was an educator who was teaching a course or writing a book on building web apps, I would use this as a class project because it is non-trivial, has levels of access control, includes interacting with APIs for payment process and notifications, has state management, and very likely has a database. It's also not just another blogging engine or Twitter clone or todo app. Plus! A lot of people can relate to and understand the concepts behind this because they've placed orders for food online. And if they haven't, if they've eaten out, the concepts are close enough to map to the technological needs. 

## Stretch Goals

- Payment processing with Stripe or something similar
- Order receipt web page with current status, could even poll or use websockets

There are so many business needs that could exist to make this more complex:

- Hours of business
- Line item customizations/requests
- Uploading restaurant branding