# Strapi backend for Miniblog

December 2020

For front end part see:  [https://github.com/Raigyo/sapper-strapi-blog-static](https://github.com/Raigyo/sapper-strapi-blog-static)

## Strapi with PostgreSQL

### PostgreSQL

````bash
$ sudo -u postgres createuser <owning_user>

$ sudo service postgresql start
```

````sql
postgres=# CREATE DATABASE <db_name>;
postgres=# CREATE ROLE <role_user> WITH LOGIN PASSWORD '<password>' CREATEDB;
postgres=# GRANT ALL PRIVILEGES ON DATABASE <db_name> TO <role_user>;
````

### Strapi

npx create-strapi-app <my-app>

=> PostgreSQL

=> Username: <db_name>

=> Password: <password>

### GraphQL

`npm run strapi install graphql`

````json
{
  "endpoint": "/graphql",
  "tracing": false,
  "shadowCRUD": true,
  "playgroundAlways": false,
  "depthLimit": 7,
  "amountLimit": 100,
  "federation": false
}
````

## Heroku

See [Heroku Deployment - Heroku Postgres](https://strapi.io/documentation/3.0.0-beta.x/deployment/heroku.html)

## Useful links

- [Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)
- [Heroku Deployment](https://strapi.io/documentation/3.0.0-beta.x/deployment/heroku.html)
- [Strapi GraphQL](https://strapi.io/documentation/3.0.0-beta.x/plugins/graphql.html#configurations)
