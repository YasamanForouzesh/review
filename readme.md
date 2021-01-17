# How node works?
## node include modules and packages. so modules and packes have to be instal and import and export
# what is the modules?
## module is the chunck of  code. We can create our modules but we need export it and when ever we want to use we shoudl import. lest's see one example:
## inside myModule.js :  I need export each function and variable that I want to use inside other js file--> 
## let counter=0
## modules.export.count=()=>{
##    for(let i; i<10 ; i++>){
##          count=i
##      console.log(count)
## }
## }
## inseide index.js: If I want to use one of the myModule.js function I shoudl import to my file -->
## const moduleObj=require('./myModule.js')
## moduleOb.count()
# what is the packages?
## Packages include many modules.
# How we can use others modules or packages?
## We need to download and install it. we can install it by globally or locally.
# locally: 
## We can enter just npm i [package's name] so this package can be used just inside that node application
# globally: 
## npm -g [package's name] by this one we can install just once andd use in other node application.
# How to start our project?