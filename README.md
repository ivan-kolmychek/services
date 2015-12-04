Collection of configuration for commonly-used services.

# Table of contents
 * [F.A.Q](#faq)

 * [PostgresQL](#postgresql)

 * [ElasticSearch](#elasticsearch)

 * [Redis](#redis)

 * [MySQL](#mysql)

# F.A.Q

## WHY U NO LINK containers betwen one another?

 * Because not all of project that I have to deal with are dockerized. 
And I want to be able to mess around with them without having to 
dockerize them first.

 * Because somethimes I just want to bring up that particular
version of service to mess around with tools available on my system,
without having them installed into the container.

 * Because it's a nice way to introduce new people to the wonderful world of 
Docker, by saying 

> Oh, you know what, you don't have to configure that dozen
of services you need for your app manually in your dev environment. Take this, it's a really easy way to manage services. 

And there is some chance that this particular developer will say "wow, so easy, much useful, nice syntax" and will want to learn more about Docker, even if they didn't have to.

But othewise yes, linking containers is very nice, easy and useful. And `docker-compose` helps to do that in sane way a lot.

## I want another service X here, what can I do?

You can ask someone to add it in the issues or you can add it yourself and submit a pull-request.

# PostgresQL

## 9.4

Usage: `docker-compose up postgres-9-4` 

Exposes: `127.0.2.253:5432`

# ElasticSearch

## 2.1

Usage: `docker-compose up elasticsearch-2-1`

Exposes: `127.0.2.252:9200` and `127.0.2.252:9300`

# Redis

## 3.0

`docker-compose up redis-3-0`

Exposes `127.0.2.251:6379`

## 2.8

`docker-compose up redis-2-8`

Exposes `127.0.2.250:6379`

# MySQL

## 5.6

`docker-compose up mysql-5-6`

Exposes `127.0.2.249:3306`
