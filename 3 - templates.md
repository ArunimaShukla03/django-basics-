In order to create a separation in our project we use "render" in "views.py" with request and name of the template. And now all we need to do is to create the template with the same name.

Now we have the folder called template with a folder "hello" as the name of the template is "hello/index.html". We could have just had "index.html" as the template name but often we want to prefix our templates with the directory name (so that if we have multiple different html files in different apps then they don't conflict with each other - this is called "namespacing").

We may also use render in the greet function and add an optional third argument called context and it is all of the information that we provide to the template. For example: all the variables that I want the template to have access to.

This context is in the form of key value pairs.

Now in our HTML file, we use {{ }} to merge django with HTML as anything inside it for example here "name" can be plugged while rendering.

We'll take look at the website "isitchristmas.com", which simply says "NO" on any other day than christmas or "YES" if it is christmas.

We'll create a similar website that says if it is new year's or not. That is, it checks if the current date is January 1 or not.

For this, we create a new app called "new year". And add it to the installed apps section in "settings.py" in main directory.

Again go to the "urls.py" for the main directory and add path for the urls of the newly created "newyear" app.

Now go to the "urls.py" for the app created i.e. and add views and its function in urlpatterns with its names. 

Now we need to create logic that whether or not its January 1st. We may do so by using a date time module in python. 

If we write "python" in the command line, it gives us python interpreter that lets us write python code just to experiment and test and see what the result is after running a certain python code.

PYTHON ON TERMINAL:

>>> import datetime
>>> now = datetime.datetime.now()

(this means that inside the datetime module there is a function called datetime.now() that gets the current date and time)

>>> now.year
2022

>>> now.month
12

>>> now.day
28

(this gives me information about the day, year and month for the current time)

>>> now.month == 1 and now.day == 1
False

(this condition means that this information about the current month and day is false)

We may use the same condition in the django view.

Now in views, we have imported datetime module that lets us know about the current information of date and time. And inside the "index" function, we have created a variable "now" that stores the current date and time.

Now during rendering, if the day and month of the year is equal to 1, it is "newyear".

Now, we create a new file called "index.html" and we need to use logic inside it so for that we use {% if newyear %} then it would write "YES" otherwise {% else %} it would write "NO" and end it by writing {% endif %}

This page created by Django is dynamic as it changes its values depending on the day but django also has static files within it that don't change like CSS which is dealt a little bit differently in Django.

In order to add static files in django, we add in a new folder called "static" that will contain all the static folders of this web application.

After creating this file, we can now write all the CSS in the "styles.css" file.

After writing the CSS code then we go to index.html and add {% load static %} at the top of the HTML page which will go ahead and load static file. Also we link this css file by typing <link href="{% static 'newyear/styles.css' %}" rel="stylesheet">

So we are not writing the direct url which we could do but we are writing that there is a static page in the folder newyear/styles.css which Django will figure out on its own.

We can use "for loop" in HTML by using {% for task in tasks %} and then looping through the elements of "task" variable in view and printing it in the form of an unordered list.

We write {% extends "tasks/layout.html" %} on the top of the page to indicate that this is the extension of "layout.html" and further add {% block body %} and {% endblock %} at the start and end of the block respectively.

ALSO, it is a little annoying to go the URL again and again and change the address so we may add a link that does the same.