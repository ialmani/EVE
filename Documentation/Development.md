# Development: How-To
___
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
___
## Clone Required Repositories
Create a *New Folder* (preferably somewhere you won't have to change any permissions) 

Open a command-line in the folder you just created, for example:
``` C:\someuser\user\Desktop\Eve_Project_Folder> ```

Run the following clone commands from this project folder one at a time:

```git clone https://github.com/ialmani/EVE-Front-End```
```git clone https://github.com/ialmani/EVE-Back-End```
___
## Setting up the development environment
You must refer to our **[Deployment Documentation](https://github.com/ialmani/EVE/tree/master/Documentation/Deployment.md)** for instructions on setting up both the Front-End and Back-End in order to proceed.

After getting each application running from following the deployment documentation, you can open the **EVE-Front-End** and **EVE-Back-End** folders in your preferred IDE to make changes.

*NOTE*: If you used **Docker Desktop** to deploy the application, you will have to manually add the dependencies for both the Front and Back End.

Instructions for the Back-End can be found in our documentation [Here](https://github.com/ialmani/EVE/blob/master/Documentation/Deployment.md#deployment-back-end).

Instructions for the Front-End can be found in our documentation [Here](https://github.com/ialmani/EVE/blob/master/Documentation/Deployment.md#deployment-front-end).
___
#### **Frontend**
In the EVE-Front-End directory, you can run:

```npm start```

This will run the app in the development mode.

Open ```http://localhost:3000``` to view it in the browser 
*(Default port # is 3000 unless changed)*

The page will reload if you make edits and save them.
You will also see any lint errors in the console.

In the EVE-Front-End directory, you can also run:

```npx cypress open```

This runs the interactive testing environment we chose called [Cypress](https://www.cypress.io/).

Once the Cy window opens up, click on
```"Tests.js"```
From there, your browser will open and Cypress will run through each of the tests automatically.
___
#### **Backend**

Making sure the virtual environment is set-up from the **[Deployment Documentation](https://github.com/ialmani/EVE/blob/master/Documentation/Deployment.md#setting-up-virtual-environment)**

***NOTE*:** Work on the develop branch.

First, enter the migration command:

```python manage.py migrate```

Next, you can **Start** the server by entering the command: 

```python manage.py runserver```

To **Stop** the server, press:  

```CRTL+BREAK```
___
## Folder Structure

#### Front-End

All the front end components are in the **src** code directory.

Each component has folders consisting of Javascript and styling files.

#### Back-End

Each application has its own directory, with its own models, views, and URLs.
