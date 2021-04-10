# Deployment: How-to

Download [Git Client](https://git-scm.com/downloads) for repository cloning purposes

Download [Docker Desktop](https://www.docker.com/products/docker-desktop) for simple deployment (optional)

Use all default settings for Git/Docker installation
___
## Set up the Project Folder Location
Create a new folder (preferably where you won't have to change permissions) which will house all of the contents that this application needs

Clone Required Repositories from command-line using git

Open a command-line in the folder you just created, for example:
- ``` C:\someuser\user\Desktop\Eve_Project_Folder> ```

Run the following "git clone" commands in this root directory one at a time:
- ```git clone https://github.com/ialmani/EVE-Front-End```
- ```git clone https://github.com/ialmani/EVE-Back-End```

Now you have a version of all of the code required to use the application
___
## Using Docker For Deployment 
#### **If you prefer maunal deployment, please skip this section**

**Make sure you have [Docker Desktop](https://www.docker.com/products/docker-desktop) downloaded and running**

Next you will execute the docker-compose.yml file housed in both the Front and Back End repositories, to do this:\

Navigate to the EVE-Front-End folder
- ```..\EVE_Project_Folder\EVE-Front-End>```

Run the command
- ```docker-compose up```

Once finished, the command line will open back up and you will repeat this for the Back End.

Once more, navigate to 
- ```..\EVE_Project_Folder\EVE-Back-End\eve-project>```

Run the command
```docker-compose up```

*NOTE*: The following *must* be done in addition to setting up Docker for the **Back End** to be fully functional
- Starting in the api folder ```..\EVE_Project_Folder\EVE-Back-End\api>``` 
- You must also manually create a super user by running the command 
```python manage.py createsuperuser``` 
in order to access the Django Admin page
- You must also manually enable your [Virtual Environment](https://github.com/ialmani/EVE/blob/master/Documentation/Deployment.md#setting-up-virtual-environment) for the Back-End to work.

Now you can open Docker and look at both of the containers you just made and from there, open them in your browser.
___
# Deployment: Back-End

#### **Current Versioning**
- Python= v3.8.3
- Django= v3.1.4
#### **Install Prerequisites**
- [Python](https://www.python.org/downloads/release/python-383/)
___
## Setting up Virtual Environment 

#### *Windows*

From the directory:
```..\EVE_Project_Folder\EVE-Back-End>```

Run the command
```python -m venv EVE-ve```
Navigate to the scripts folder in the newly created “EVE-ve" folder
```..\EVE-Project-Folder\EVE-Back-End\EVE-ve\Scripts>```

Run the command
```./activate.bat```
Your virtual environment is ready

#### *Mac*
From the directory:
```..\EVE_Project_Folder\EVE-Back-End>```

Run the command
```virtualenv env -p python3```

Run the command
```source env/bin/activate```

Your virtual environment is ready
___
### Installing Django
Make sure your virtual environment is **ON**

Next navigate to the api in the following folder:
```..\EVE-Project-Folder\EVE-Back-End\api>```

Run the command
```pip install -r requirements.txt```

***Caution:*** If pip isn't upgraded to max it will give you an error stopping requirements.txt installing onto your machine, this error will tell you what command you should use to update pip. Retry command once pip has been upgraded
___
### Starting the Django Server
Navigate to the following directory:

```..\EVE-Project-Folder\EVE-Back-End\api>```

Run the following commands
```python manage.py migrate```

```python manage.py createsuperuser```

```python manage.py runserver```

Once finished, Django will tell you the URL of the admin server that you can then access through your browser

### Stopping the Django Server
To quit the server, press CTRL+BREAK or CTRL+C on your keyboard
___
### Troubleshooting
**Command not found: django-admin**
- Django-admin should be on your system path if you installed Django via pip. If its not in your path ensure you have your virtual environment activated and you can try running the command python -m django

**macOS permissions**
- If your using mac, you may see the message “permission denied” when you try to run django-admin. A file must be “executable” before it can be run as a program. To do this open the terminal and go to the directory that the django-admin is installed then run the command sudo chmod +x django-admin.
 
### Where to find errors if logged
- To find errors look in the terminal tab as this is also where you go to run the server.
___
# Deployment: Front-End
#### Current Versioning
- node.js = v14.15.0 LTS
- npm = v6.14.8
#### Install Prerequisites
- [Node.js and npm](https://nodejs.org/en/) 

Be sure to install npm as well when completing the setup for Node.js
___
### Setting up node_modules package
From the top level project directory:
- ..\EVE-Project-Folder\EVE-Front-End>

Run the command
- npm install

From the “front_end” level project directory:
- ..\EVE-Project-Folder\EVE-Front-End>
___

### Starting the Front-End API
Run the command
```npm start```

### Stopping the Front-End API
CTRL+C will prompt you to terminate the batch job
It will ask you to press [y/n] to confirm.

___
### Troubleshooting
All troubleshooting will be done through the terminal.
### Where to find errors if logged
The only source of an error will be in the terminal.

### Most critical/vulnerable pieces that can fail
Import statements and dependencies are the most crucial part of the system currently.
___
