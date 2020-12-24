---
id: env-variables
title: Environment variables
---

Some Environment variables are necessary for each Osso deployment. If you Deploy Osso with the Heroku button, some of the these will be set for you, and you'll have the opportunity to set the others as you deploy your instance. Otherwise view your hosting provider's documentation on Environment or Configuration variables.

### BASE_URL
**required**

The base url for your Osso deployment, used to construct ACS URLs. Not required for Heroku deployments that use [Dyno Metadata](https://devcenter.heroku.com/articles/dyno-metadata). Must include protocol.

_Example Value:_ `https://osso.saasapp.com`

### DATABASE_URL
**required**

The URL to your Postgres database. Heroku will generate this for you when using the deploy to Heroku button, or otherwise when adding a Postgres addon.

_Example Value:_ `postgres://user:password@ec2-54-165-36-134.compute-1.amazonaws.com:5432/d5vj7h6o2psidfy0h`

### SESSION_SECRET
**required**

Key used for encrypting Osso sessions for both OAuth and Admin UI. Will be generated by Heroku when using the Heroku deploy button.

_Example Value:_ `9c670917322529f383c1df29e861e2ea21c03d09e30ead661846fa87ebc5b33a`

### CYPRESS_INSTALL_BINARY
Osso uses Cypress for e2e tests. This prevents yarn / npm from downloading the Cypress binary in your release environment. Not required but recommended.

_Example Value:_ `0`