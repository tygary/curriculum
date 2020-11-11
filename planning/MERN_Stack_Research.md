# MERN Stack Research

# Questions?

Do we advertise teaching redux?  We should remove it if so…

How deep should we go into the state-management redux/reducers rabbit-hole?

How much do we need students to actually build theses from scratch versus just modify and implement parts?




# To research:

redux connect()





# Overall project examples:

[MERN without redux boilerplate](https://github.com/abhijeetjuneja/mern-without-redux-boilerplate)

- has validators
- controllers include routes
- authentication middleware

[MERN starter](https://github.com/joshuaslate/mern-starter)

- react redux
- router.js
- auth
- clean simple controllers and models


[Inventory Application](https://github.com/moelashmawy/inventory-application)

- react redux
- full application with multiple user modes
- 



----------
# React


## State

hooks
setState
useReducer
useEffect 

prop drilling vs context API vs Redux
[Context api vs redux](https://daveceddia.com/context-api-vs-redux/) - Easier to read
[React, Redux, and Context Behavior](https://blog.isquaredsoftware.com/2020/01/blogged-answers-react-redux-and-context-behavior/) - harder to read…
[React official context API guide](https://reactjs.org/docs/context.html)
[you might not need redux](https://www.simplethread.com/cant-replace-redux-with-hooks/) - useful comparison of how to do redux behavior in hooks
 

[Three principles of redux](https://redux.js.org/understanding/thinking-in-redux/three-principles)
[redux tooklit](https://redux-toolkit.js.org/tutorials/basic-tutorial) 

redux fetch data actions - BEGIN, SUCCESS, FAILURE
[Fetching data with redux](https://daveceddia.com/where-fetch-data-redux/)
[explaining thunks](https://stackoverflow.com/questions/35411423/how-to-dispatch-a-redux-action-with-a-timeout/35415559#35415559)

functional vs classes

pure components

higher order components (redux connect or context API wrapper)

[React State Management in 2020](https://medium.com/better-programming/react-state-management-in-2020-719d10c816bf) - local state vs hooks


[React boilerplate](https://github.com/react-boilerplate/react-boilerplate)


----------
# Express

[express.js](https://expressjs.com/)


## index.js

this should initialize the server, probably doesn’t need to be modified


## config

these are your keys, probably don’t need to be modified


## models

one file per model object

Create a mongoose schema, then export the model.

optionally can define methods and such to do things like encrypting password


## controllers

functions which get called by specific routes.  work with the models to update the DB.

optionally, this can just include the routing code here.


## routes.js

Can put all the routes in a separate file and then have each route call a specific controller function


## validators

Functions which can validate input datas and generate error messages



## Authentication

using passport or something else to work with auth
salting passwords
using JWT



----------
# Node

package.json
dependencies
scripts


----------
# Mongo

[mongoose](https://mongoosejs.com/docs/guide.html) 



## Creating schemas/Models

Creating a schema
Referencing another schema  `type: Schema.Types.ObjectId, ref: "Product"`  ([subdocuments](https://mongoosejs.com/docs/subdocs.html))
exporting a model
 
 
virtual properties
alias



## Searching for an object

findById
findOne

[Queries](https://mongoosejs.com/docs/queries.html)

[.populate](https://mongoosejs.com/docs/populate.html) and .exec - (join) bring in all the connected data from other linked models


## Updating objects (documents)

findOneAndUpdate
.save()

Creating an object / deleting an object


error handling

how to handle async activity. (await vs promises)

[validating objects](https://mongoosejs.com/docs/validation.html) (documents)

[middleware](https://mongoosejs.com/docs/middleware.html)

# Other

[UX Copywork](https://www.smashingmagazine.com/2017/02/improving-ui-design-skills-copywork/)
[React Copywork](https://daveceddia.com/learn-react-with-copywork/)
[Complete guide to React rendering behavior](https://blog.isquaredsoftware.com/2020/05/blogged-answers-a-mostly-complete-guide-to-react-rendering-behavior/)
[The History and Implementation of React-Redux](https://blog.isquaredsoftware.com/2018/11/react-redux-history-implementation/)







# Project One
## React
- primarily use functional components with useState
- maybe show one controlled component with class-based state?
- Try to minimize prop drilling, but don’t venture into context 


## Server
- no authentication
- simple schemas (no references)
- at least one variable route with CRUD


## Possible projects:
- TODO app
    - Simple, would only be a single todo list and user so that we only have a list of tasks
    - Start with those on the backend, eventually transition that to updating a server and storing it in the database.




# Project Two
## React
- Talk about reducers, stores, and actions
- Use context, as a way of avoiding prop drilling
- don’t get into redux in the primary path, but maybe have an optional side module using it.
- 


## Server
- Give authentication OOTB and have them create the register and login pages
- Schema has references and must use populate
- multiple routes



## Possible projects:
- ecommerce app
    - products
    - cart
    - checkout process
    - login flow and multiple users
- task tracker trello clone
    - tasks
    - boards
    - states
    - login flow multiple users
    - creating a task and moving it through the states flow
- social network (facebook, twitter, or forum clone)
    - posts
    - comments
    - login flow multiple users
    - different boards
    - creating a post, letting others comment on it
    - upvoting/liking
- 


