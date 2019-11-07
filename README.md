Node-RED Todo App
==================

**This project is part of the [Node-RED in Production Workshop](https://github.com/knolleary/node-red-in-production-workshop).**

### About

This is an example Node-RED project that provides a [Todo-Backend implementation](https://www.todobackend.com/).

The Todo-Backend project defines a simple web API for managing a todo list. It
was inspired by the [TodoMVC](http://todomvc.com/) project which showcases how
to implement a common Todo application across a wide range of technologies.

The Node-RED implementation requires an instance of CouchDB to be running locally
and for it to contain a database called `todos`. The easy way to create the database
on a fresh install of CouchDB is to run:

    curl -X PUT  http://localhost:5984/todos

This project includes a customised version of the TodoMVC web app in the `public` folder.

After cloning it into your Node-RED environment, you should make the following
changes to your Node-RED `settings.js` file:

 - set `httpAdminRoot` to `/admin` - this moves the editor away from the root
   path
 - set `httpStatic` to the absolute path to this project's `public` folder.

Once you have made those changes and restarted Node-RED, you should be able
to access the Todo web app on the url you would normally access the editor.



### Acknowledgements

The TodoMVC web app in the `public` folder is licensed under the MIT license. It
is based on the version available here: https://github.com/TodoBackend/todo-backend-client, with
minor modifications
