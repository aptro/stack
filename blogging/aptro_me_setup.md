# How [aptro.me](https://aptro.me) is setup

[aptro.me](https://aptro.me) is the blogging setup I use(intend) to write longform ideas.

## Criteria

* less to manage
* Minimal
* Customization
* Basic analytics - traffic, load

## Stack

1. Namecheap
   1. Get domain name
2. Clouflare
   1. DNS mapping
   2. Basic site and load analytics
   3. Network security
   4. Caching
3. AWS
   1. Ubuntu t3.micro, 8 GB, EC2
   2. MySql via RDS
   3. Elastic IP
4. Ghost
   1. [ghost-cli](https://ghost.org/docs/api/v3/ghost-cli/)
   2. [local setup via cli](https://ghost.org/docs/install/local/)
   3. [production setup via cli](https://ghost.org/docs/install/ubuntu/)
   4. [Desktop app](https://ghost.org/downloads/)
