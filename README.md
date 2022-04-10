# StartHub
A platform that makes raising investment for your startups easier than never before! Startup owners pitch their startups, Investors explore and connect with them.
# Contents
1)How to run the code?\
2)Basic structure and URL paths\
3)Database\
4)Forms\
5)Views\
6)Static and Templates
# 1)How to run the code?
1.1)Clone the GitHub repository.\
1.2)Make sure you have installed Python 3.10.0 and Django 4.0.1\
1.3)Make sure you have pillow installed, else run the ```pip install Pillow``` command
1.4)cd into the main repository in the terminal. When you run the ls command, if you see the file manege.py, you are at the correct location to run the next command.If you don't see, then use cd to reach the correct directory.Make Migrations using "python3 manage.py makemigrations" followed by "python3 manage.py migrate"\\
1.5)Now if python 3.10.0 is the only version of python you have, then run the command "python manage.py runserver". If you have multiple versions of python, then run "python3 manage.py runserver".\
1.6)You would see something like this in terminal "Starting development server at (a url)". Copy that URL and run it in the browser(Chrome and Safari are strongly recommended).\
1.7)You can now access the website. Either sign up to make a new account or use email:ketaki@gmail.com password:dogcat123 to login(this is also the admin account). While signing up, make sure to create a complex password.
# 2)Basic structure and URL paths
2.1)Basic structure

"starthub" is the main project file that contains the settings.py. "core" is the core app of the whole website. "static" contains all the static files(image and css files).  
2.2)URLs\
urls.py in starthub directly points to urls.py inside the core directory. If you use /admin, you can access the Django admin panel.\
All the URLs in core/urls.py has been listed below.\
2.2.1)Common URLs:\
\
Landing page: ''\
Login page: signin/\
Sign up page: signup/\
Logout:logout/
\
2.2.2)URLs restricted to logged-in users:\
\
2.2.2.1)URLs for investors:\
\
Explore page: explore/\
Info page: info/'a string'/

2.2.2.1)URLs for startup owners:\
\
Profile : profile/\
List a company:litt/\
Redirecting after listing:redirectt/\
Info of your startup page: info/'a string'/\
Delete: delete/'a string'/


# 3)Database
Five models are used in the project:\
3.1) The django inbuilt User model. It stores username(email) and password.\
3.2) "Profile" model, which is in a one to one relation with the User model. It stores username(email)(one to one key)-'user', name-'name',mobile number-'mob',Account Type-'typee'\
3.3) "Startup"model, it stores all the information about the startup. It has a ManyToMany field 'tags' that connects to Tag Model and a ForignKey field 'owner' that refers User.\
3.4) "Tag" model, contains all tags. It has 'name' field.\
3.5) "TeamMember" model, **This model is currently not uder use. Will be devoloped in future!** To store the members of a startup, their photos and bios.

# 4)Views
There are 11 views in total in the take/views.py\
In most cases, views have been given the same name as the corresponding URL that refers to it.\
The views are simple and easy to understand on glancing through the code. Since there are a lot of them, it is not going to be covered one by one in this readme.\
Note: decorator 'login_required' imported from django.contrib.auth.decorators has been used to restrict the pages that are meant for logged in users only.

# 5)Static and Templetes
Static files are stored in the directory 'static' present in the main directory. static/img contains images used throughout the website. static/styles contains the css files.\
HTML files are stored in core/templetes/core.\
Templates use Bootstrap 5, given below are the GitHub repo for the same:\
https://github.com/twbs/bootstrap \


# Developed by Hackuna Matata
Front End Developers:\
Brij Desai\
Yukta Rajapur\
Backend End Developers:\
Ketaki Tamhanakar\
Nitheezkant R

Devfolio Project Submition: \
Project Demo:

# The End

