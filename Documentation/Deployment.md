# Deployment: How-to
- Download Git Client [Here](https://git-scm.com/downloads) (For repository cloning purposes)
- Use all default settings for Git upon installation
### Set up Project Folder Location
- Create a new folder (preferably where you won't have to change permissions) which will house the contents of the application
- Clone Required Repositories from command-line

Open a command-line in the folder you just created

- C:\someuser\user\Desktop\Eve_Project_Folder>

Run the following commands from this project folder:
- git clone https://github.com/ialmani/EVE-Front-End
- git clone https://github.com/ialmani/EVE-Back-End

Now you have a version of all of the code required to use the application

## Deployment: Back-End
### Current Versioning
- Python= v3.8.3
- Django= v3.1.3
### Install Prerequisites
- [Python](https://www.python.org/downloads/release/python-383/)

### Setting up Virtual Environment
From the directory:
- ..\EVE-Project-Folder\EVE-Back-End>

Run the command
- py -m venv EVE-Virtualenv

Navigate to the scripts folder in the newly created “EVE-Virtualenv” folder
- ..\EVE-Project-Folder\EVE-Back-End\EVE-Virtualenv\Scripts>

Run the command
- activate.bat

Your virtual environment is ready

### Installing Django
Making sure your virtual environment is on by looking for the following on your command line

- (EVE-Virtualenv) C:\..\..\EVE-Back-End>

Next navigate to the following folder:

- (EVE-Virtualenv) ..\EVE-Project-Folder\EVE-Back-End>

Run the command
- py -m pip install Django

Once finished, Run the next command
- pip install djangorestframework

Django is now ready to be started

### Starting the Django Server
Making sure the virtual environment is set up, navigate to the following directory:
- (EVE-Virtualenv) ..\EVE-Project-Folder\EVE-Back-End\eve_backend>

Run the following command
- python manage.py runserver

It will tell you the URL of the server that you can then put into a browser if you wanted

The django server is now ready for development
## Deployment: Front-End
### Current Versioning
- node.js = v14.15.0 LTS
- npm = v6.14.8
### Install Prerequisites
- Node.js & npm [Download](https://nodejs.org/en/) 
### Setting up node_modules package
From the “front_end” level project directory:
- ..\EVE-Project-Folder\EVE-Front-End\front_end>

Run the command
- npm install

#### Start

From the “front_end” level project directory:
- ..\EVE-Project-Folder\EVE-Front-End\front_end>

Run the command
- npm start
