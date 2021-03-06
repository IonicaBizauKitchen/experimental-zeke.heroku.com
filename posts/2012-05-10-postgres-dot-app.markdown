---
layout: post
title: "Postgres.app"
date: 2012-05-10 23:00
comments: true
categories:
---

Factor X in Adam Wiggins' [Twelve-Factor App](http://www.12factor.net/dev-prod-parity)
is **dev/prod parity**: the idea that your development, staging, and production environments
should be as similar as possible to minimize unexpected problems.

For the heroku user, one easy move toward such parity is using postgres in the development
environment. In the past I was reluctant to use postgres because it was difficult to install
and it was always easier to use MySQL or SQLite because the barrier was lower.

But I'm happy to say that the [@mattt](http://twitter.com/mattt)'s new project,
[Postgres.app](http://postgresapp.com/), soothes that pain: *"Open the app, and you have
a PostgreSQL server ready and awaiting new connections. Close the app, and the server shuts down."*
Here's an example database configuration that works with Postgres.app right out of the box:

    development:
      adapter: postgresql
      host: localhost
      database: dreamboat-development

    test:
      adapter: postgresql
      host: localhost
      database: dreamboat-test

That's not all folks. Postgress.app has a great logo too!

<a href="http://postgresapp.com/">
  <img src="/images/extra/netsuke.png" class="no-border">
</a>

**Update**: If you've already got another version of postgres installed, you may need to prepend Postgres.app's binary to your PATH:

    export PATH=/Applications/Postgres.app/Contents/MacOS/bin:$PATH

**Update 2**: There's a great [eight-minute Railscast on Migrating to PostgreSQL](http://railscasts.com/episodes/342-migrating-to-postgresql)
that has some tips regarding use of PostgreSQL with Rails.
