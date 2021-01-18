# How node works?
### node include modules and packages. so modules and packes have to be instal and import and export
# what is the modules?
### module is the chunck of  code. We can create our modules but we need export it and when ever we want to use we shoudl import. lest's see one example:
### inside myModule.js :  I need export each function and variable that I want to use inside other js file--> 
### let counter=0
### modules.export.count=()=>{
###    for(let i; i<10 ; i++>){
###          count=i
###      console.log(count)
### }
### }
### inseide index.js: If I want to use one of the myModule.js function I shoudl import to my file -->
### const moduleObj=require('./myModule.js')
### moduleOb.count()
# what is the packages?
### Packages include many modules.
# How we can use others modules or packages?
### We need to download and install it. we can install it by globally or locally.
# locally: 
### We can enter just npm i [package's name] so this package can be used just inside that node application
# globally: 
### npm -g [package's name] by this one we can install just once andd use in other node application.
# Two modules that I use and installed globally:
### nodemon
### sequelize-cli
# How to start our project? 
### we should first run npm init -y to start our node project. By this command the package.json will be created. After that we shoudl create the main js file. So use touch index.js (the name is depends on the name of the main inside the pakcage.json).
# How to run the clone projects from gitHub ?
### If we clone the project from the github, we should install all dependencies that is inside the package.json so we should run (npm i ) to install all depenciess. 


# Some modules that I used:
## If you want to know how to use each module and learn more about other useful module you can search or go to npm website to read their documentations.
####    moment
####    express 
####    fs
####    axios
####    models
####    express-ejs-layouts
####    ejs
####    cheerio
####    sequelize
####    psq
# ejs:
## ejs is the view file that user can see on their browser. These files unclude html and java script. we can use jave script by <%%> if we want to use and print the vlue of the variable we should use = sign <%= input%>. if we want to just use the variable to do some functionality we can do like <% input%>. <%- body%>
# Express:
## const express=require('express')
## const app= express()
## app.get('/ ',(req,res){})=> this route is for home.
## app.get('/:id',(req,res){})=> : make the variable(params) and we can access by req.params.id  .
app.get('/:id',(req,res)=>{ 

    res.send(req.params.id)

})
# How to run the code on browser:
## app.listen(3000, ()=>{
##    console.log('Listening on port 30000')
## }) 
## it means it will run on port 3000
## The * means , if you don't find the path(route) that is math to the url is error and we don't have have this route so it will go to the * one .
 app.get('*',(req,res)=>{

    res.send('404 Page not found')

})


# axios
### we should use this module when we want to use API 

    axios.get(`http://www.omdbapi.com/?apikey=${API_KEY}&s=${req.query.searchYerm}`)
    .then(response=>{
        res.send(response.data)
    })
 ### whole of this code will go to inside of the app.get or app.post ,....
# If you need learn more about RESTFUL: 
 https://gawdiseattle.gitbook.io/wdi/05-node-express/00readme-1/00readme#restful-routing

# cheerio:
### this module will help us to do scraping.
https://gawdiseattle.gitbook.io/wdi/javascript/additional-topics/js-data-scraping


# fs
### fs help us to read and write files

# Controllers
# Views
# Partials
# Models
models have the table information in javascript 

# Midelware
Ultra-simple middleware:
app.use((req, res, next) => {
    console.log('🦩 Hello! 🦩')
    next()
})
Drop this in your index.js on a project and navigate around. Watch your terminal print a lotta flamingos!
Middleware can be anything you want, middleware that we NPM install and utilize is just a series of functions just like this one!
If you're wondering what "next" is in this middleware, try removing it! You'll notice that you never escape your middleware and your routes will not resolve. Remember in express we have to give an endpoint to each req - res cycle! That's what next() is saying: "Just do the next thing, my middleware function is done."

app.use(express.static(__dirname + '/public'));

# Layouts
const ejsLayouts = require('express-ejs-layouts');
fore example for MidleWare: app.use(ejsLayouts)