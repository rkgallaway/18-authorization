![CF](http://i.imgur.com/7v5ASc8.png) LAB 18
=================================================

## La8 18: Authorization

### Author: Ryan Gallaway

### Links and Resources

[![Build Status](https://www.travis-ci.com/rkgallaway/18-authorization.svg?branch=master)](https://www.travis-ci.com/rkgallaway/18-authorization)

* [repo](https://github.com/rkgallaway/18-authorization)
* [travis](https://www.travis-ci.com/rkgallaway/18-authorization)
* [back-end](https://lab18-authorization-rg.herokuapp.com) 

#### Documentation
* [jsdoc](https://github.com/rkgallaway/18-authorization/blob/master/docs/index.html)

### Modules
#### `google.js`
#### `middleware.js`
#### `router.js`
#### `user-models.js`
#### `404.js`
#### `500.js`

##### Exported Values and Methods

## Assignment
Implement a Bearer Authentication system with optional token expiry, api keys, and single use tokens.  
As per Code Fellows LAB.md, with the modifocation that we are to complete one or two improvements.

### Requirements

* Install the core bearer authorization system
  * `middleware.js` - Handle the Bearer Header to pull and verify with the token
  * `users-model.js` - Add a bearer authorization method that verifies the token
  
* Improve the core bearer authorization system...
  * Alter the JWT to be time sensitive (valid for 15 minutes)
  * Alter the JWT to be single-use
    * With every authenticated access, re-send a new JWT token as a cookie or header
    * Disable those that you've already authenticated
  
* Create a Auth Key system
  * Create a new route: `router.post('/key' ... )` that will generate a JWT without an expiration date, and noted to be an auth key (so that it won't be deleted like a single use token)
  * Allow users to authenticate using the Auth Key as they would a normal token
  * Auth Keys should never expire
  * Auth Keys should be re-usable

### Setup
#### `.env` requirements
* `PORT` - Port Defined in ENV
* `MONGODB_URI` - mongodb://heroku_7bch7mzm:82m8eevnegr57f89enbipgi07n@ds259154.mlab.com:59154/heroku_7bch7mzm

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.
  
#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

### UML 
#### Drawn in Collaboration with:
* Hannah Ingham
* George Raymond
* Jon DiQuattro
* Ryan Gallaway
![group whiteboard](./assets/bearer-drawing.jpg)
