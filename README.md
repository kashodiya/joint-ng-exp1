Express + Angular application setup
===================================

Introduction
------------
This is a skaleton application using Express and Angular.

How does it work?
-----------------
 
Express is used as a API application and Angular is used as pure front end application.
In development mode you run both the applications - Express on 3000 and Ng on 2400.
Ng is configured to route all the API calls (URLs that start with /api) to port 3000.
When done, you build Ng app. This will create HTML and related frontend files in public folder.
To test frontend in production mode, just run Express on 3000.

Prerequisites
-------------
- Install express generator
- Install angular-cli
    - Go https://github.com/angular/angular-cli

Recipe (without cloning this repo)
-------
- Create project folder
    - mkdir joint-ng-exp1
- Get into new folder
    - cd joint-ng-exp1
- Create express skaleton app
    - express
- Install express dependencies
    - npm install
- Create front end app using angular-cli
    - ng create frontend
- Change app.js 
    - Remove view settings
    - Remove error handlers
    - Remove views folder
    - Remove index and user routes
    - Remove existing static path
    - Add new static path 
        - app.use("/", express.static(__dirname + '/public'));
    - Create api route (see the code)    
- Run express app
    - nodemon
- Open new tab cd to frontend
    - cd frontend
- Add prody config in frontend folder
    - See frontend/proxy-config.json
- Modify apps=>outDir in frontend/angular-cli.json
    - Line should looke like: "outDir": "../public",
- Start frontend app
    - ng serve --proxy proxy-config.json
- Open your app using
    - http://localhost:4200
    - Note that the calls to api is proxied to 
        - http://localhost:3000


How to build?
-------------
- In frontend folder 
    - ng build
- This will delete the public folder and create new     



