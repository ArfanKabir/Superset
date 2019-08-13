# Superset
Testing out Apache Superset, an app in the incubation stage on Apache which is similar to Tableau functionality wise (it is a data analytics tool), but is also open source; anything can be added into the code, and the programmer can add whatever functionality they need.

# Steps to get it working
Outside of Superset, I created a database using a csv that contained census data. So I converted that into a 
Firstly, had to install many dependencies, which include Cython, pymssql, superset itself, and virtual environment. Superset is a flask application, so it is entirely built in Python and uses said packages to run.

I ran superset in a virutal environment (that's what they recommend), and installed all the dependencies that I needed. Any database that's needed can be installed through their python package.

Superset itself can be loaded with a couple of examples (which is what I did to practice and get familiar with it), and then you can later load in a database and grab data from it. I used MSSQL (as mentioned before), and connected it using the sqlalchemy module in Superset itself, and configured the dashboard itself.

# Problems with Running Superset
Originally, I tried to run it using Docker and PostgreSQL (because the examples are loaded into PSQL), but that led to a big hassle that I struggled with for a couple of days. Creating the virutal environment and running it through there was a lot easier and I was able to both load the examples and load my own database onto there. It was also easier using MSSQL, but that was partially because I messed up installing PSQL on my own system.
