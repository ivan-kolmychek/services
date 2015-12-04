Collection of configuration for commonly-used services.

# WHY U NO LINK containers betwen one another?

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

# PostgresQL

## 9.4

`docker-compose up postgres-9-4` will bring up the container, which will
expose it's port on `127.0.2.253:5432`

# ElasticSearch

## 2.1

`docker-compose up elasticsearch-2-1` will bring up the container, which will
expose it's ports on `127.0.2.252:9200` and `127.0.2.252:9300`
