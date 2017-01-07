# Rumbl

To start:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.create && mix ecto.migrate`
  * Install Node.js dependencies with `npm install`
  * Start Phoenix endpoint with `mix phoenix.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](http://www.phoenixframework.org/docs/deployment).

## Chapter 2 : Lay of the Land

* We installed Phoenix, which is built using Erlang and OTP for the service layer, Elixir for the language, and Node.js for packaging static assets.
* We used the Elixir build tool mix to create a new project and start our server.
* Web applications in Phoenix are pipelines of plugs.
* The basic flow of traditional applications is endpoint, router, pipeline, controller.
* Routers distribute requests.
* Controllers call services and set up intermediate data for views.

## Chapter 3 : Controllers, Views and Templates

* We created a simple repository. We did so to simplify your plunge into
the world of controllers and views.
* We created actions, which serve as the main point of control for each
request.
* We created views, which exist to render templates.
* We created templates, which generate HTML for our users.
* We employed helpers, which are simple Phoenix functions used in templates.
* We used layouts, which are HTML templates that embed an action’s HTML.

## Chapter 4 : Ecto and Changesets

* We began the chapter by introducing Ecto and announcing our intention
to replace the in-memory repository with a database-backed repository
using Ecto.
* We configured our new database and connected it to OTP, so that Elixir
could do the right thing in the event of a Phoenix or Ecto crash.
* We created a schema, complete with information about each necessary
field.
* We created a migration, to help us specify our database tables and automate
doing and undoing any database changes.
* We created a changeset so Ecto could efficiently track and manage each
change requested by our application.
* We integrated this change into our application.

## Chapter 5 : Authenticating Users

* We added the comeonin dependency to our project.
* We built our own authentication layer.
* We built the associated changesets to handle validation of passwords.
*  We implemented a module plug that loads the user from the session and
made it part of our browser pipeline.
*  We implemented a function plug and used it alongside some specific
actions in our controller pipeline.

## Chapter 6 : Generators and Relationships

* We converted a private plug into a public function and shared it with our controllers and routers.
* You learned how to migrate and roll back changes to the database.
* We defined relationships between User and Video schemas and used functions from Ecto to build and retrieve associated data.
* You learned that Ecto uses strictly explicit semantics to determine if a
relationship is loaded or not.
