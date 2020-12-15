# Development: How-To

### FrontEnd
- Languages: HTML, CSS, Javascript
- Framework: [React](https://reactjs.org/)
### BackEnd
- Languages: Python
- Frameworks: [Django](https://www.djangoproject.com/)
### Databases
- [mySQL](https://www.mysql.com/)
### Recommended IDE’s
- [Visual Studio Code](https://code.visualstudio.com/download)
- [IntelliJ](https://www.jetbrains.com/idea/download/)
## Clone Required Repositories
- Create a new folder (preferably where you won't have to change permissions) which will house the contents of the application
- Clone the following repos using [Git](https://git-scm.com/downloads)
- [Frontend](https://github.com/ialmani/EVE-Front-End)
- [Backend](https://github.com/ialmani/EVE-Back-End)
## Setting up the development environment
- Refer to [Deployment](https://github.com/ialmani/EVE/tree/master/Documentation/Deployment.md) for instructions on setting up all of the required software for both Backend and Frontend.

- After getting the application running, you can open the EVE-Front-End and EVE-Back-End folders in your IDE to make changes

#### Frontend
In the project directory, you can run:

- npm start

Runs the app in the development mode.
Open http://localhost:3000 to view it in the browser (default port # is 3000 unless changed) .
The page will reload if you make edits and save them.
You will also see any lint errors in the console.

In the project directory, you can also run:

-npx cypress open

This runs the interactive testing environment we chose.
Once the Cy window opens up, click on "Tests.js"
From there, your browser will open and cypress will run through each of the tests automatically.

#### Backend

Making sure the virtual environment is set-up from [Deployment](https://github.com/ialmani/EVE/tree/master/Documentation/Deployment.md) 

Run the commands

- python manage.py migrate
- python manage.py runserver

This will start the server and is ready for use.

*NOTE*
-   Work on the develop branch.

To stop the server: 

- CRTL+BREAK 

### Folder Structure

##### Frontend

All the front end components are in the src code directory

Each component has folders consisting of Javascript and styling files

##### Backend

Each application has its own directory, with its own models views and URLs
