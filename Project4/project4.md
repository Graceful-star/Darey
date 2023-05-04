## DOCUMENTATION OF PROJECT4

### STEP1 :- Install NodeJs
Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine. Node.js is used in this tutorial to set up the Express routes and AngularJS controllers.

Update ubuntu
`sudo apt update`

Upgrade ubuntu
`sudo apt upgrade`

Add certificates
`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates`

`curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -`

Install NodeJS
`sudo apt install -y nodejs`

![Project11](images/image13.PNG)
![Project11](images/image14.PNG)
![Project11](images/image15.PNG)

### Step 2: Install MongoDB
MongoDB stores data in flexible, JSON-like documents. Fields in a database can vary from document to document and data structure can be changed over time. For our example application, we are adding book records to MongoDB that contain book name, isbn number, author, and number of pages.

`sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6`

`echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list`

Install MongoDB

`sudo apt install -y mongodb`

Start The server

`sudo service mongodb start`

Verify that the service is up and running

`sudo systemctl status mongodb`

Install npm – Node package manager.

`sudo apt install -y npm`

![Project11](images/image16.PNG)
![Project11](images/image17.PNG)
![Project11](images/image18.PNG)


Install body-parser package

We need ‘body-parser’ package to help us process JSON files passed in requests to the server.

`sudo npm install body-parser`

Create a folder named ‘Books’

`mkdir Books && cd Books`

In the Books directory, Initialize npm project

`npm init`

Add a file to it named server.js

`vi server.js`
Copy and paste the web server code below into the server.js file.

![Project11](images/image18.PNG)
![Project11](images/image19.PNG)
![Project11](images/image20.PNG)


### Step 3: Install Express and set up routes to the server
Express is a minimal and flexible Node.js web application framework that provides features for web and mobile applications. We will use Express in to pass book information to and from our MongoDB database.

We also will use Mongoose package which provides a straight-forward, schema-based solution to model your application data. We will use Mongoose to establish a schema for the database to store data of our book register.

`sudo npm install express mongoose`

In ‘Books’ folder, create a folder named apps

`mkdir apps && cd apps`

Create a file named routes.js

`vi routes.js`

Copy and paste the code below into routes.js

In the ‘apps’ folder, create a folder named models

`mkdir models && cd models`

Create a file named book.js

`vi book.js`

Copy and paste the code below into ‘book.js’

### Step 4 – Access the routes with AngularJS
AngularJS provides a web framework for creating dynamic views in your web applications. In this tutorial, we use AngularJS to connect our web page with Express and perform actions on our book register.

Change the directory back to ‘Books’

`cd ../..`

Create a folder named public

`mkdir public && cd public`

Add a file named script.js

`vi script.js`

In public folder, create a file named index.html;

`vi index.html`

![Project11](images/image21.PNG)


Change the directory back up to Books

`cd ..`

Start the server by running this command:

`node server.js`

![Project11](images/image22.PNG)
![Project11](images/image23.PNG)

