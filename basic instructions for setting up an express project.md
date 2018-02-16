Set up the folder (either by creating a repo on git and cloning it OR by creating a new folder in a workspace).

Inside the newly set up folder, open Terminal

Run "npm init" to initialise Node Package Manager
"enter" to accept defaults

Install Express "npm install express --save"
(--save adds the package to the dependencies list)

Install Jest "npm install jest --save-dev"

Install BodyParser (so that we can receive JSON) "npm install body-parser --save"

Install Handlebars "npm install hbs --save"

Install Fetch "npm install node-fetch --save"


---
We will need to initialise all the components in the relevant js file
---

const express = require('express');
const bodyParser = require('body-parser');
const app = express();

const fetch = require('node-fetch'); // if using fetch


app.use(bodyParser.json()); // parse incoming JSON
app.set('view engine', 'hbs'); // use Handlebars as a view engine


// only if returning object
app.post('/pathOfURL', function (req, res){
  res.json(req.body); // body = body of the request
});


// only if using Handlebars to render template
app.post('/pathOfURL', function(req, res){
  res.render("nameOfTemplateFile", req.body) // body = objectSentToPostReq
})


// add listener so that we can access what we're working on
app.listen(8080, function(){
  console.log("listening on port 8080");
});
