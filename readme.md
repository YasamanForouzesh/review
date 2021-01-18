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

