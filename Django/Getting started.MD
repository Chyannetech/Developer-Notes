### What is Django?
Django is by far the most popular Python-based web framework and its popularity continues to grow thanks to the amazing growth of Python itself.

Django was publicly released in 2005 and got its name from one of its creator's, Adrian Holovaty, who named Django after his favorite guitarist Django Reinhardt.

It's designed for the rapid development of highly-secure web applications.

Compared to the minimalist web framework of Express, Django is a much higher-level framework that provids lots of functionality baked-in, including:

A powerful Object-Relational-Mapper (ORM) for working with relational databases using Python code instead of SQL.
A built-in admin app for browsing and manipulating data in the database.
Built-in user management and authentication.

##### Components of a Django Project
The quirky thing about Django is how it names its high-level components.

What we think of as a web application, Django calls a project.

Further, what we think of as part of an app's functionality, or modules, Django refers to as apps.

##### Django's Routing Methodology
Because routing is so fundamental to developing web apps, it's worthwhile knowing in advance an important difference between Express and Django's routing methodology.

Web frameworks such as Express and Ruby on Rails, use both the HTTP verb & URL to define routes used to map requests to controller actions.

Other frameworks, such as Django and ASP.NET Core, use just the URL when defining a route, ignoring the HTTP verb.

That's why the Python modules used to define routes in Django are named urls.py (see diagram above).

Installation & Set Up


Prerequisite Installs
Django should have been installed during installfest.

Let's verify the installation as follows:

$ python3 -m django --version
# -> 2.2.x
If it's not installed, do a one-time install of the Django framework using the following command:

$ pip3 install Django


By default, Django uses a lightweight database called SQLite. However, SQLLite is not appropriate for production use because it's considered not to be scalable (for example, only one user/request can access the database at a time).

Therefore, from the start, we'll be following the better practice of using a more capable database by configuring each of our Django projects to work with PostgreSQL.

To use PostgreSQL, we need to do a one-time install of the psycopg2 Python package:

$ pip3 install psycopg2-binary
psycopg2is a popular library that enables Python applications to interface with PostgreSQL.




Create a Database for the Project
MongoDB automatically creates a database when you use it for the first time.

However, we're not so lucky with SQL databases where we will need to manually create a database that we want to use for a Django project in advance.

Let's create one now in psql for the project we're about to code:

$ psql
# CREATE DATABASE polls;

Run the \lcommand to confirm that pollsis in the list of databases.

Also, depending upon how PostgreSQL was installed, you might need the database's username/password. Just in case, make note of the username to the right of the database name in the list.

With the database created, type \qto exit the psql shell.

Video Setting up environment: 
command= pipenv shell inside djang env

https://generalassembly.zoom.us/rec/play/hB4PIyhA-TQEY6ZADyrDhsjE5-3f6aAUzuKnGnq9-2tAUqfbuj3SRltOShh1uAsvOuTzgeiQMJPiPc5U.9TLa74yHlzyczRwE?continueMode=true&_x_zm_rtaid=Y2GvA0H-RF-lO_uMI_f0CA.1659731489748.4b86889ac7b75c67bd2274e7fba6b0e0&_x_zm_rhtaid=987


https://generalassembly.zoom.us/rec/play/gabBJ4F5EqK5tt3RWO6dKTLhNa5GY30glcKJufQEN2KUlCU84vFEoueXHysJfF_un6yVRB_vXBEtO-I.2KG_P5FZvxq-5opW?continueMode=true&_x_zm_rtaid=Y2GvA0H-RF-lO_uMI_f0CA.1659731489748.4b86889ac7b75c67bd2274e7fba6b0e0&_x_zm_rhtaid=987

https://seir-batch.netlify.app/unit-projects/unit-four-project-requirements/

https://seir-batch.netlify.app/second-language/week-2/day-4/lecture-materials/uploading-images-to-amazon-s3/