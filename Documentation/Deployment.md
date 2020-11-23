# Deployment: How-to
Download Git Client [Here](https://git-scm.com/downloads) (For repository cloning purposes)

Use all default settings for Git upon installation

### Set up Project Folder Location
Create a new folder (preferably where you won't have to change permissions) which will house the contents of the application

Clone Required Repositories from command-line

Open a command-line in the folder you just created

- C:\someuser\user\Desktop\Eve_Project_Folder>

Run the following commands from this project folder:
- git clone https://github.com/ialmani/EVE-Front-End
- git clone https://github.com/ialmani/EVE-Back-End

Now you have a version of all of the code required to use the application

### Deployment: Back-End
#### Current Versioning
- Python= v3.8.3
- Djagno= v3.1.3

#### Install Prerequisites
- Python [Download](https://www.python.org/downloads/release/python-383/)
Setting up Virtual Environment

##### Windows:
From the directory:
..\EVE-Project-Folder\EVE-Back-End>

Run the command
- py -m venv EVE-Virtualenv

Navigate to the scripts folder in the newly created 
“EVE-Virtualenv” folder
- ..\EVE-Project-Folder\EVE-Back-End\EVE-Virtualenv\Scripts>

Run the command
- activate.bat
##### Mac:
From the directory:
..\EVE-Project-Folder\EVE-Back-End>

Run the command
- virtualenv env -p python3

Run the command
- source env/bin/activate

Your virtual environment is ready

### Installing Django
Making sure your virtual environment is on:

Next navigate to the following folder:
- \EVE-Project-Folder\EVE-Back-End>

Run the command
- py -m pip install django

Run the command
- pip install djangorestframework

Run the command
- pip install django-cors-headers

### Starting the Django Server
Navigate to the following directory:
- \EVE-Project-Folder\EVE-Back-End\eve_backend>

Run the following command
- python manage.py runserver

It will tell you the URL of the server that you can then put into a browser if you wanted

### Stopping the Django Server
To quit the server, press CTRL+BREAK or CTRL+C on your keyboard

### Troubleshooting
Command not found: django-admin
- Django-admin should be on your system path if you installed Django via pip. If its not in your path ensure you have your virtual environment activated and you can try running the command python -m django

macOS permissions
- If your using mac, you may see the message “permission denied” when you try to run django-admin. A file must be “executable” before it can be run as a program. To do this open the terminal and go to the directory that the django-admin is installed then run the command sudo chmod +x django-admin.
 
### Where to find errors if logged
- To find errors look in the terminal tab as this is also where you go to run the server.

## Deployment: Front-End
#### Current Versioning
- node.js = v14.15.0 LTS
- npm = v6.14.8
#### Install Prerequisites
- Node.js & npm [Download](https://nodejs.org/en/) 
#### Setting up node_modules package
##### Start
From the “front_end” level project directory:
- ..\EVE-Project-Folder\EVE-Front-End\front_end>

Run the command
- npm install

From the “front_end” level project directory:
- ..\EVE-Project-Folder\EVE-Front-End\front_end>

Run the command
- npm start

##### Stop
CTRL+C will prompt you to terminate the batch job
### Troubleshooting
- All troubleshooting will be done through the terminal.
### Where to find errors if logged
- The only source of an error will be in the terminal.

### Most critical/vulnerable pieces that can fail

Import statements and dependencies are the most crucial part of the system currently.
