# docker-rails-mysql

## create rails

```
$ docker-compose run web rails new . --force --no-deps --database=mysql
```

## docker build

```
$ docker-compose build
```

## rails setting

```database.yml
development:
  <<: *default
  database: myapp_development
  host: db
  username: root
  password: password

# Warning: The database defined as "test" will be erased and
# re-generated from your development database when you run "rake".
# Do not set this db to the same as development or production.
test:
  <<: *default
  database: myapp_test
  host: db
  username: root
  password: password
```

## mysql create

```
$ docker-compose run web rails db:create
```

## Hello world!

```
$ docker-compose up
```
