# reverse-engineering


--User Story--
As a learning developer
I want to walkthrough the source code
So that I am able to apply the learned tools to my own project.




--EXPLANATION OF FILES--

CONFIG
This is a directory that holds the middleware folder, the config folder, and the passport js file.

MIDDLEWARE

isAuthenticated.js {This restricts routes that the user is not allowed to see if not logged in. if they are logged in, it continues with request };
config.json { This file contains the connection configuration to connect to server};

passport.js { This file holds javascript that tells passport we want that the login will require an email address and password, as well as error bouncebacks if the login credentials don't match the database. };

MODELS

index.js { This file connects to our database and imports the users log in data };

user.js { requires "bcrypt" for password hashing. this makes the database secure even if compromised. Javascript defines what is stored on our database including email and password.};

PUBLIC

JS:
login.js{This file provides the login needed on the client-side to be able to log in as well as the api call to post.};

members.js{This file uses the api created to get the user data};

signup.js{This file contains the javascript that allows users to signup on the client side.};

STYLESHEETS

login.html{ This is the layout for the login page of the application.};

members.html{ This is the layout for the members page of the application.};

signup.html{ This is the layout for the signup page of the application.};

ROUTES

api-routes.js { This file holds the routes for signing in, logging out and getting the user's specific data to be displayed client-side.};

html-routes.js { This file holds the routes that check whether the user is signed in, whether user already has account etc, and then sends them to the corresponding appropriate html page};

package.json { contains all package info, node modules used, version info, as well as the dependencies needed before running the application};

server.js { This file requires packages, sets up the PORT, uses sessions to keep track of the user's log in status, creates express and middleware, creates routes and syncs database / logs message in terminal on successful connection to server};

.gitignore{This file ignores the node modules used so when it is pushed to github, it doesn't include those files as well in the push.};