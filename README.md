# Mongo Driver for Fluent

![Swift](http://img.shields.io/badge/swift-3.0-brightgreen.svg)
[![CircleCI](https://circleci.com/gh/vapor/mongo-driver.svg?style=shield)](https://circleci.com/gh/vapor/core)
[![Slack Status](http://vapor.team/badge.svg)](http://vapor.team)

## Install Mongo

### OS X

```shell
brew install mongodb
```

### Ubuntu

```shell
sudo apt-get update
sudo apt-get install mongodb
```

## Run

```shell
mongod
```

## Use in Vapor

When setting up your droplet, create a database using a MongoDriver instance and pass it into the Droplet intializer.

```
let mongo = try MongoDriver(
	database: "test",
	user: "user1",
	password: "pswd1",
	host: "localhost",
	port: 27017
)
let db = Database(mongo)
let drop = Droplet(database: db)
```

