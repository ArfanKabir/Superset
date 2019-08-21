# Building Superset

Step 0: Have Python installed on your system.
macOS comes with Python installed, but it is better to use the version that you can get with Homebrew,
as that version of Python comes installed with pip and is easier to work with than the system version.


Step 1. Run the command pip install virtualenv, activate the

Install the virtual environment module (if for some unknown reason, it doesn't come with your version of virutal environment),
and make sure to activate it. The project is in development, so it needs to be ran in a virutal environment so that it 
can be ran without being in production. Activate the virtual environment.

Step 2. Install your dependencies. 

In the virtual environment, you have to install everything you need. This will include the python module for whichever
database you need (I installed pymsssql, but you can install postgreSQL, mySQL, or whatever database backend that you decide)

Run the command pip install --upgrade setuptools pip, this will install all the other dependencies that Superset 
is going to need to work. 

Step 3. Install Superset and set it up
Run the following commands:
pip install superset, superset db upgrade, flask fab create-admin, and superset init
You can also run superset load_example just to get some working examples in superset as well if you just want to get a feel
for the app. 

Step 4. Run the server
run the command superset run -p 8080 --with-threads --reload --debugger

This will load up the server on the localhost, and superset


# Connecting your Own Database with Your Own Data

Use Pip Install to install the dependency for your desired database language (as mentioned before)

After that has been installed, run the server again using superset run -p 8080 --with-threads --reload --debugger

After that, go to the database tab under sources, and click on the plus sign. 

From there, you need to connect your database using SQLAlchemy syntax. It looks like the following: dialect+driver://username:password@host:port/database
For example, my database URL looked like mssql+pymssql://sa:XXXXXXXXXX@localhost:1433/electionKaggle

Test the connection, and you should get a message saying that it's okay.

Check off all the parameters, and then you should be able to add the tables from the database now.

Back at the homepage, you add the tables and get started with analyzing.
