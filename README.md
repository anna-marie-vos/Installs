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
* to check logs type: heroku logs

## Note: to install Heroku on you pc type the following in your terminal:
* Run this from your terminal.
* The following will add our apt repository and install the CLI:
* sudo add-apt-repository "deb https://cli-assets.heroku.com/branches/stable/apt ./"
* curl -L https://cli-assets.heroku.com/apt/release.key | sudo apt-key add -
* sudo apt-get update
* sudo apt-get install heroku

### Note: error heroku is not a branch of the repository:
* that is because the cloned repo is not linked to heroku on this pc, so run the following:
* heroku git:remote -a yourHerokuAppName

### Note: run heroku locally to check for issues using:
*  heroku local web
* Your app should now be running on http://localhost:5000/.

### Note: when using knex and trying to deploy
* to check heroku, in terminal type: heroku logs 
* this will give you the errors as it runs.
* check if pg is installed, if not install this: npm install pg --save
* go to the heroku page click on the resources file and search for postgress in the addons and use that.
* then copy the string in settings and copy that into the knexfile.js
* in knexfile.js change production setting to : process.env.DATA

### Note: when bundle.js is not working
* in package.json add "postinstall":"webpack -p" and add bundle.js in .gitignore
* this will create a bundle.js in the public folder
* cut and paste babel into dependancies and remove from dev-dependencies

### Note: run postgress database
* type in terminal : heroku run bash
* then check that migrations directory in productions in knexFile.js is correct
also see :https://medium.com/modus-create-front-end-development/optimizing-webpack-production-build-for-react-es6-apps-a637e5692aea#.sdghfx639
