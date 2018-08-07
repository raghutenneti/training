# training
#create directory 
mkdir project2
#run 
node init
#insatll express generator 
node express -g express generator 
#create express project
node express project2
#create all dependencies
{
  "name": "project2",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "node ./bin/www"
  },
  "dependencies": {
    "cookie-parser": "~1.4.3",
    "debug": "~2.6.9",
    "express": "~4.16.0",
    "http-errors": "~1.6.2",
    "jade": "~1.11.0",
    "morgan": "~1.9.0"
  }
}
"dependencies": {
  "cookie-parser": "~1.4.3",
  "debug": "~2.6.9",
  "express": "~4.16.0",
  "http-errors": "~1.6.2",
  "jade": "~1.11.0",
  "mongodb": "^3.0.5",
  "monk": "^6.0.5",
  "morgan": "~1.9.0"
}
#install dependencies
npm install
#start the npm and check dependencies
npm start
#it shows like
project2@0.0.1 start D:\sites\node\nodetest1
> node ./bin/www
#create one directory
mkdir data
#open cmd type dppath
"C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath c:\node\project2\data
#open  console
"C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"
#create database
use project2
#create data on to the database 
{
        "_id" : ObjectId("5202b481d2184d390cbf6eca"),
        "username" : "raghu",
        "email" : "raghu@testdomain.com"
}
{
        "_id" : ObjectId("5202b49ad2184d390cbf6ecb"),
        "username" : "sarma",
        "email" : "testuser2@testdomain.com"
}
{
        "_id" : ObjectId("5202b49ad2184d390cbf6ecc"),
        "username" : "sai",
        "email" : "sai@testdomain.com"
}
#start npm 
node npm start
#create DB function
router.post('/adduser', function(req, res) {

   var db = req.db;
   
   var userName = req.body.username;
   var userEmail = req.body.useremail;

   var collection = db.get('usercollection');

   collection.insert({
        "username" : userName,
        "email" : userEmail
    }, function (err, doc) {
        if (err) {
            res.send("There was a problem adding the information to the database.");
        }
        else {
            res.redirect("userlist");
        }
    });
});
# start npm once 
npm start
