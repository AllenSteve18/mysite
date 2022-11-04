# Django Coursera Week 1
#### This is the code for the auto-grader assignment for week 1 of **Building Web Applications in Django**. This code is to be uploaded to your personal accounts on [PythonAnywhere](https://www.pythonanywhere.com). Please follow the instructions below to do the same and get the site live.

###### Step 1: Clone the repository by running the command below in the bash console of your pythonanywhere beginner account.
```
git clone https://github.com/saumyasarkar11/mysite.git
```

###### Step 2: Create virtual environment and make sure you put proper python version(We will be using 3.10 here).
```
mkvirtualenv --python=/usr/bin/python3.10 mysite-env
```

###### Step 3: Install all the requirements for our application.
```
cd mysite
pip install -r requirements.txt
```

###### Step 4: Migrate database for our application followed by generationg a single static file for CSS, JS, images, etc.
```
python manage.py migrate
python manage.py collectstatic
```

###### Step 5: Go to *Web* tab on the top right and click on it. You will see *Create a Web Application* button, click on it. Select python version 3.10, click *Next* click on *Manual Configuration*(make sure you do not click on the “Django” option).

###### Step 6: Change source code and virtualenv location to that of your respective project by changing the username only. Refer to the image below.
![Screenshot 2022-11-04 195107](https://user-images.githubusercontent.com/76894046/199999856-3ad8c6c3-6cfe-4e03-ab4b-5e1d4b004c72.png)

###### Step 7: Change the WSGI configuration file by clicking on the link. Clicking the will lead you to an editor. Just remove everything and paste the below given code. Make sure you change *<your_username>* to your respective username. Refer to the image to locate the required file.
![Screenshot 2022-11-04 200245](https://user-images.githubusercontent.com/76894046/200001260-04d166bd-2255-4906-a846-fb85446ec96f.png)
```
import os
import sys

path = '/home/<your_username>/mysite'
if path not in sys.path:
     sys.path.insert(0, path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'
```
