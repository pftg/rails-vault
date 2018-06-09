---
title: Rails Stripe Checkout
repo: RailsApps/rails-stripe-checkout
homepage: https://github.com/RailsApps/rails-stripe-checkout
language: Ruby
license:
templates: ERB
description: Rails 5.0 starter app for selling a product using Stripe Checkout
---

Rails 5.0 example application demonstrates how to sell a product using
[Stripe Checkout](https://stripe.com/checkout). Use this example
application as a starter app for your own web applications.

See the tutorial for a complete explanation of the code:

  - [**Stripe Checkout
    Tutorial**](https://tutorials.railsapps.org/rails-stripe-checkout)

The application uses:

  - [Stripe](https://stripe.com/) for credit card payment processing
  - [Devise](https://github.com/plataformatec/devise) for user
    management and authentication
  - [Role-Based
    Authorization](http://railsapps.github.io/rails-devise-roles) for
    administrator access
  - [Bootstrap](http://getbootstrap.com/) front-end framework

Other tutorials may be helpful:

  - [Signup and
    Download](https://tutorials.railsapps.org/rails-signup-download)
  - [Role-Based
    Authorization](http://railsapps.github.io/rails-devise-roles)
  - [Devise Tutorial](http://railsapps.github.io/rails-devise/)
  - [RSpec Tutorial](http://railsapps.github.io/rspec.html)

You can build this application in only a few minutes using the [Rails
Composer](http://railsapps.github.io/rails-composer/)
tool.

#### From the RailsApps Project

The [RailsApps](http://railsapps.github.io/) open source project offers
starter applications and tutorials for Rails developers. Generate the
applications with the Rails Composer tool.

All the code is explained in the Capstone Rails Tutorials. You can
purchase the [Capstone Rails
Tutorials](https://tutorials.railsapps.org/) to support the project.

#### If You Are New to Rails

If you’re new to Rails, see [What is Ruby on
Rails?](http://railsapps.github.io/what-is-ruby-rails.html), the book
[Learn Ruby on Rails](http://learn-rails.com/learn-ruby-on-rails.html),
and recommendations for a [Rails
tutorial](https://tutorials.railsapps.org/rails-tutorial).

## What Is Implemented — and What Is Not

This application is based on the
[rails-devise-roles](https://github.com/RailsApps/rails-devise-roles)
and
[rails-signup-download](https://github.com/RailsApps/rails-signup-download)
example applications. The rails-devise-roles application shows how to
implement “sign up” and “sign in” features (authentication) combined
with authorization for roles such as an administrator. The
rails-signup-download example application shows how a visitor can
download a PDF file after registering for an account.

The rails-stripe-checkout application implements a payment feature using
Stripe Checkout so a visitor makes a payment to obtain an example PDF
file. Devise provides account registration, so that a visitor creates an
account when he or she makes a purchase. This means the visitor can
return to the site, and after signing in with an email address and
password, can download the PDF file again to get an update or replace a
deleted file. This functionality is similar to sites such as
[Gumroad](https://gumroad.com/) or [Leanpub](https://leanpub.com/) where
authors sell digital books.

[Stripe Checkout](https://stripe.com/checkout) provides compliance with
[Payment Card Industry Data Security
Standards](https://www.pcisecuritystandards.org/) (PCI-DSS). Stripe
Checkout is a JavaScript script that generates a “Pay with Card” button
and form. The script submits the visitor’s credit card data to Stripe
and obtains an authorization token. Your application uses the
authorization token to initiate a payment so the visitor’s credit card
data is never stored or exposed by your application.

Most examples of Stripe Checkout show how to make one-time purchases
with no account registration feature. In contrast, the
rails-stripe-checkout application shows how to integrate Stripe Checkout
with Devise for account registration. The application provides a
two-step “sign up and purchase” process that initiates a payment and
creates a user account.

For a one-step process, you can use the
[Stripe.js](https://stripe.com/docs/stripe.js) script instead of Stripe
Checkout, creating a custom form. Stripe Checkout is simpler. Stripe.js
provides more flexibility. This application does not show how to use
Stripe.js.

The rails-stripe-checkout example application does not show how to offer
multiple products for sale (though you can customize the application if
you wish). It also does not support subscription sales or recurring
billing (again, you can customize the application if you wish).

The rails-stripe-checkout application has all the functionality of the
rails-signup-download example application, including the ability to
subscribe a user to a MailChimp mailing list at the time an account is
created. The mailing list subscription feature runs as a background
process using [Active
Job](https://github.com/rails/rails/tree/master/activejob). You can
learn more about the subscription feature by reading the [Mailing List
with Active Job](https://tutorials.railsapps.org/rails-mailinglist-activejob) tutorial.
