# Technical Exercise - Currency Project

# The exercise

This is a DevOps exercise aimed at taking two apps and deploying them out to a cloud based solution.

Inside each app is a README.md file which tells you more about each app and how to package / configure it.

# About the apps

This application consists of two parts:

1. Front End Project - An Angular project that runs the front end of the project
2. Back End Spring Boot app that loads and saves currency history to an in-memory H2 Database

The app itself takes the currency output from the ECB and allows the user to perform conversions and also allows the user to view currency conversion rate history.

# useful notes

*** BackEnd ***

The backend app uses src/main/resources/app.properties to manage it's connection strings.
In there you'll find which URLs it uses to connect to the ECB (important for allowing outgoing connections)
 
*** Front End ***

See the `src\app\environments\` folder for the environments file to make it all work.

# the task?

Please clone this repository and make any changes required to deploy this out to a cloud kubernetes solution and provide the URL for this.

Typically, we'd expect that each item is containerised into docker, and that a docker file is made so that the application can be deployed out to a kubernetes instance (for example)

The app will run as an HTML app, with an NGINX container with some rules to connect to the local backend instance (from app.properties - this is set as `server.port=4201`)

You'll also need to spin up the backend java instance, see it's `README.md` file on how to do this.

Feel free to alter any configuration files to make this work, we're happy for you to create a feature branch!

Bonus Points - 
1. Create new production profiles configurations in each file and 
2. Create secrets files for any required credentials

# Further help and assistance or Questions?

Good luck, and if you've any questions, please contact Luke Campbell (l.campbell@capital-iom.com) for assistance.



