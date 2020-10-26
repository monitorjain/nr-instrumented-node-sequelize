# New Relic auto-Instrumented Rest APIs with Express, Sequelize & MySQL example

This Instrumented NODEJS App is babelized (executes with babel script) and NR Instrumented and based on the following project by BEZKODER:
> [Build Node.js Rest APIs with Express, Sequelize & MySQL](https://bezkoder.com/node-js-express-sequelize-mysql/)

## Project setup

* First, start a MYSQL server (and don't change the default password which is "")

* If you don't have a local MYSQL server and you're on Mac - simply run "brew install mysql"

* Once mysql is installed, start up with this command - "brew services mysql start"

* Next, enter mysql client on terminal by running this command - mysql -u root -p 
    Once prompted for password, hit enter if no password has been set or enter your MSQL server password
    Next enter the following command on the msql client -> CREATE DATABASE testdb;
    
* Once MYSQL database is up and running, we can move to the NodeJS Sequelize project setup and execution phase


## Project Specs
=============================
 
* Note that the cloned project is pre-installed with New Relic instrumented

* Go to one.newrelic.com by clicking this link - Sign up New Relic Free Account and then visit this [link](https://one.newrelic.com/launcher/account-settings-launcher.account-settings-launcher)

* Copy your license key from this screen and paste it in the newrelic.js file on the home directory of the cloned repo

![pic](https://user-images.githubusercontent.com/45892212/97128724-2dbd2780-1791-11eb-8052-57a9625eaedd.png)



![pic](https://user-images.githubusercontent.com/45892212/97128822-71b02c80-1791-11eb-98f1-63e478ad34f8.png)




### 1.0 Build 
=============================
Once the Git project is cloned, simply execute the following:
```
npm install
```

### 2.0 Run (two options)
=============================

## 2.1 Kickstart with Babel
```
npm start
```
    This invokes the babel start script - nodemon -r newrelic --exec babel-node server.js
    
Note: Babel script execution can change the order of execution, hence newrelic is specially passed as the first package as required for dynamic instrumentation

## 2.2 Run directly with the node command (OPTIONAL - cp the backup package.json and remove the default one)
```
node server.js
```


### 3.0 Exercise Transactions for Full Observability in New Relic (two options)
=============================
Post an article - use any REST API CLIENT 
![article](https://user-images.githubusercontent.com/45892212/97129317-a8d30d80-1792-11eb-91d0-9893370bf313.png)

Full list of transactions are prescribed on this [tutorial blog](https://bezkoder.com/node-js-express-sequelize-mysql/#Test_the_APIs)

### 4.0 Validate New Relic O11y Patterns
=============================

## 4.1 Transaction reporting in New Relic APM
![first](https://user-images.githubusercontent.com/45892212/97129443-08311d80-1793-11eb-913e-f06b109ceb18.png)

## 4.2 Distributed Tracing
![second](https://user-images.githubusercontent.com/45892212/97129457-1121ef00-1793-11eb-84a5-7b415ffe9054.png)

