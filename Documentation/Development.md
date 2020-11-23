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
Open http://localhost:3000 to view it in the browser.
The page will reload if you make edits and save them.
You will also see any lint errors in the console.

- npm test

Launches the test runner in the interactive watch mode.
See the section about running tests for more information.

- npm run build

Builds the app for production to the build folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

#### Backend

Making sure the virtual environment is set-up from [Deployment](https://github.com/ialmani/EVE/tree/master/Documentation/Deployment.md) 

Run the command 

- python manage.py runserver

This will start the server and is ready for use.

*NOTE*
-   Before you can see any articles (functionality) reflected in the frontend, you must go to the Django server that appears in the terminal and then appen

To stop the server: 

- CRTL+BREAK 

### Folder Structure

##### Frontend

All the front end components are in the src code directory

Each component has folders consisting of Javascript and styling files

##### Backend

Each application has its own directory, with its own models views and URLs