# Simple Commerce

The gist: build out a web app that allows sellers to add products that can be purchased on a public website. When a product is purchased, it creates an order for the seller to fulfill.

An eCommerce platform is simple to grasp since we use them on the regular, but there's a lot of complexity under the surface. It is certainly possible to build a simplified version, especially for learning purposes.

If you're interested in learning a new web technology, this project covers a lot of what you'd need to learn. Whether it's a server-rendered web app or a static site that works with an API, there's a lot going on.

## Specs

- Seller authentication
- Add products in admin
- List products in storefront
- Add items to a cart
- Accept payment to pay for items, [Stripe](https://stripe.com) is great for this!
- Create an order for the purchased products that's visible in the admin

## Concepts

- Non-trivial data models
- Storing data in the database
- Payment processing
- Authorization (admin access vs public storefront)
- Admin management area
- Public rendering of data

## Stretch Goals

- Associate photos with a product
- Digital file uploading & delivery
- Inventory management system
- Emails for both seller and buyer
- Allow sellers to customize their web storefront

## References

- Open source
    - [Spree](https://github.com/spree/spree) (Ruby)
    - [Solidus](https://solidus.io)
- Closed source
    - Big Cartel
    - Shopify
