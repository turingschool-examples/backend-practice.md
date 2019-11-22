# Backend Practice

## Introduction

This repo is intended for developers to get more comfortable with building databases using Express, Knex, and PostgreSQL. This dataset is a partial list of the data that comes from the [New York Philharmonic Subscribers Database](https://archives.nyphil.org/index.php/open-data).  You will be building a RESTful API and getting more practice with migrations, seeding data, and writing endpoints.

## Relationships

You will be building two tables (one for the seasons and another for the subscribers) using a one-to-many relationship.

### Required endpoints

* 4 GET endpoints
  * 2 GET endpoints for all of one resource (i.e. '/api/v1/seasons')
  * 2 GET endpoints for a specific resource (i.e. '/api/v1/seasons/:id')
* 2 POST endpoints
* 1 DELETE endpoint

**Bonus:** Experiment with building 2 PATCH endpoints as well.

### Status Codes & Error Handling

Reminder to practice incorporating correct status codes and good error handling.  All endpoints should respond with the minimum status code results:

* 200/201: Success
* 404: Not Found

If POST request fails to save an entity due to bad information being sent from the client, you should respond with

* 422: Unprocessable Entity

If you have a critical server error, you should respond with

* 500: Internal Server Error

You are welcome to use other appropriate status codes.

In addition to responding with the appropriate status code, you should send back clear, informative error messages when something goes wrong. For example, if a `POST` request fails because the request didn't include a required parameter, respond with something like `'Entity requires a <fieldName> but none was provided.'

### Deployment

Practice deploying your backend to Heroku!