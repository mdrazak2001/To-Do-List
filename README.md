//npm init
//npm i ejs express body-parser mongoose lodash

# Server Starting Code

const express = require("express");

const bodyParser = require("body-parser");

const _ = require("lodash");

const ejs = require("ejs");

const mongoose = require('mongoose');

const app = express();

app.set('view engine', 'ejs');

app.use(bodyParser.urlencoded({
  extended: true
}));
app.use(express.static("public"));

mongoose.connect('mongodb://localhost:27017/test', {useNewUrlParser: true, useUnifiedTopology: true});

//TODO

app.listen(3000, function() {
  console.log("Server started on port 3000");
});
