Express + Angular application setup
===================================

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
- In new tab cd to frontend
    - cd frontend
- Add prody config in frontend folder
    - See frontend/proxy-config.json
- Modify apps=>outDir in frontend/angular-cli.json
    - Line should looke like: "outDir": "../public",
- Start frontend app
    - ng serve --proxy proxy-config.json


