# Installs for clean install
Step 1: sudo apt install git

git config --global user.email "you@example.com"

git config --global user.name "Your Name"

sudo apt install nodejs-legacy

Step 2: sudo apt-get install nodejs

step 3: sudo apt-get install npm

To test (to get the version of the install): 

node -v 

npm -v 

npm install sqlite --save

once package.json is made do: npm install

when you get errors that some modules arent not there in the modules:

npm cache clean

rm -rf node_modules

npm install

#Deploying things to heroku
* create account : www.heroku.com
* then login to your account (using terminal command): heroku login
* create application in heroku (using terminal command): heroku create AppName
* Note: everything needs to be in your master branch of your app.
* go to master branch, git pull and npm install before sending to heroku
* When in your master branch do the following terminal command: git push heroku master 
* then type in terminal command: heroku open
