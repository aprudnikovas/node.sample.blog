node.sample.blog
================

[![Build Status](https://travis-ci.org/aprudnikovas/node.sample.blog.png?branch=master)](https://travis-ci.org/aprudnikovas/node.sample.blog)

## Introduction

Node app (blog) boilerplate. Role protected routes, integrated bootstrap. File structure inspired by [grails](http://grails.org/).

## Dependencies

1. Install [node.js](http://nodejs.org/#download).
2. Install [bower](http://twitter.github.com/bower/).
<pre>
$ sudo npm install bower -g
</pre>

3. Install [MongoDB](http://www.mongodb.org/downloads).
4. Start the MongoDB server from a terminal window:
<pre>
$ mongod
</pre>
5. Make sure your current directory is nodejs.sample.blog .
6. Install dependencies using the node package manger (npm).
<pre>
$ sudo npm install
</pre>

## Running the Demo

1. Make sure your current directory is nodejs.sample.blog:
<pre>
$ npm start
</pre>
2. Visit [http://localhost:3000](http://localhost:3000) in a web browser.

## Pushing to heroku

1. Create an account in [heroku](http://www.heroku.com/)
2. Install [heroku toolbelt](https://toolbelt.heroku.com/)
3. Create an app from cli while in node.sample.blog directory
<pre>heroku apps:create myAwesomeNodeApp</pre>
Will add `heroku` remote to git.
4. Define environment for your app:
<pre>heroku config:add NODE_ENV=production</pre>
5. As app relies on mongodb you should add add on to your app in heroku
<pre>heroku addons:add mongolab:starter</pre> or `heroku addons:add mongohq:sandbox`
Note: as these add ons are free, but in my case I had to verify account with credit card details.
6. Now just push to heroku
<pre>git push heroku master</pre>
7. To open app in the browser `heroku open` (should be myAwesomeNodeApp.heroku.com),
to check running process `heroku ps`, to see logs `heroku logs`

## Credit

- [Addy Osmani](http://addyosmani.com/) - backbone-boilerplates
- [Jeremy Martin](http://devsmash.com/) - password hash
- [Jared Hanson](https://github.com/jaredhanson) - passportjs
- [James Carr](http://blog.james-carr.org/) - Streaming Files from MongoDB GridFS

## License

[MIT License](http://opensource.org/licenses/MIT)
