# My first API project with DB


1- It lacks node_modules folder to use it you need to go to terminal and write "npm install"

2- You will also need psql configuration file of your own database that called "psqlconfig.js" 
 
3- Inside the psql file you can copy paste this and fill it with your own info :



const Pool = require('pg').Pool;

const pool = new Pool({
    user:   ,  // you need to create it or use default postgres
    password:  ,  // use the password that you use for connecting to user
    database: ,  // your decision
    host:  , //usually localhost
    port: , // usually 5432
});


module.exports = pool;

-----------------------------------------------------------------

after you fill this you need to open your database (either by psql or console commands) and print :

CREATE TABLE todo(
    todo_id SERIAL PRIMARY KEY,
    description VARCHAR(255)
);

-------
I used Postman for all commands
