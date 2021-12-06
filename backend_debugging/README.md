# index.js File

### error 1
require("../db");
soluation:
require("./db");


# todoback/index.js
### error
dont require dotenv in index.js for mongoDB
soluation:
require("dotenv").config();

### error
app.use(express.json());
<< before Route

### error 
for index.js file (mongoDB)
process.env.DB_URI,
soluation:
process.env.DB_URL,


### error
.catch((err) => {
    console.log("DB connected");
soluation:
.catch((err) => {
    console.log(err);


### error
morgan is not defined
soluation:
const morgan = require("morgan");



# models/todo.js File
### error 1
const mongoose = require("mongose");
soluation:
const mongoose = require("mongoose");
and npm mongoose

### error 2
task: { type: Boolean, required: true },
soluation:
task: { type: String, required: true },

### error 3


# controllers/todos.js File
### error 1
const todoModel = require("./../../db/models/todos");
soluation:
const todoModel = require("./../../db/models/todo");

### error
module.export = {}
soluation:
module.exports = {}

### error 
const todo = req.body.todo;
soluation:
const { task } = req.body;

### error 
const newTodo = new todoModel({
    todo,
soluation:
const newTodo = new todoModel({
    task,

### error 
res.status(200).json(result);
soluation:
res.status(201).json(result);

### error
const getTodoById = (req, res) => {
  const { id } = req.query;
soluation:
const getTodoById = (req, res) => {
const { id } = req.body;


# routes/todos.js File
### error 
bath for controller File
= require("./../controllers/todos");
soluation:
= require("../controllers/todos");


Finally i need to change Port to 5000 (4000) dont work with me.