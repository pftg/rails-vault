---
title: TelAPI SMS Subscription Starter Kit
repo: dougiebuckets/TelAPI-SMS-Subscription-Starter-Kit
homepage: https://github.com/dougiebuckets/TelAPI-SMS-Subscription-Starter-Kit
language: Ruby
license:
templates: ERB
description: A Ruby on Rails application that expedites the process of creating an SMS subscription service with TelAPI.
---

## TelAPI SMS Subscription Starter Kit

### What is it?

The TelAPI SMS Subscription Starter Kit is a Ruby on Rails application that expedites the process of creating an SMS subscription service. A developer simply needs to clone this repo and follow the directions below. You'll have a working SMS subscription service up and running in no time :)

### How It Works

1. Head over to TelAPI and signup for a TelAPI account: http://www.telapi.com
1. Purchase a TelAPI phone number through the TelAPI dashboard
1. Configure your TelAPI number's SMS Request URL to point to the following: http://yourserversdomain.com/sms/index
1. Clone this repo
    ```
      git clone git@github.com:dougiebuckets/TelAPI-SMS-Subscription-Starter-Kit.git
    ```
1. Open the SMS controller in app/controllers
1. Replace the 'telapi_number' variable with your recently purchased TelAPI number
    ```
      telapi_number = "+15555555555"
    ```
1. Push this code to your server
1. Perform a migration to create the user's table on your server. The user's table has a 'numbers' column where your subscriber's phone numbers will be stored. Additional migrations can be used to add new columns for other user attributes.
    ```
      rake db:migrate
    ```
1. Have a beer and celebrate
