# Installs for clean install
* Step 1: install latest version: sudo apt-get upgrade
* Step 2: sudo apt install git
* git config --global user.email "you@example.com"
* git config --global user.name "Your Name"
* Step 3: Follow the instructions for installing nvm: https://github.com/creationix/nvm
* nvm install v6.9.5
* Step 4: install node using nvm, follow the nvm instrucitons
* step 5: sudo apt-get install npm
* To test (to get the version of the install): 
* node -v 
* npm -v 
* npm install sqlite --save
* once package.json is made do: npm install
* when you get errors that some modules arent not there in the modules:
* npm cache clean
* rm -rf node_modules
* npm install 
* to create a new package.json type in terminal: npm init
* to check network cards, in the terminal type: ifconfig

#Deploying things to heroku
* create account : www.heroku.com
* then login to your account (using terminal command): heroku login
* create application in heroku (using terminal command): heroku create AppName
* Note: everything needs to be in your master branch of your app.
* go to master branch, git pull and npm install before sending to heroku
* When in your master branch do the following terminal command: git push heroku master 
* then type in terminal command: heroku open
* to check logs type: heroku logs
## Other programs thats nice on Linux
* shutter
* Gimp
* for svg images also checkout: https://askubuntu.com/questions/301540/export-image-as-svg-in-gimp
* inkscape
* kazam

## Host static page with github pages
* clone the repository to your pc. 
* checkout a new branch called: gh-pages
* that's it, you'll find the live site at https://anna-marie-vos.github.io/repoName

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
* to seed / migrate your data run in terminal to access the heroku virtual pc: heroku run bash 
* npm run knex migrate:latest
* npm run knex seed:run

### Note: when bundle.js is not working
* in package.json add "postinstall":"webpack -p" and add bundle.js in .gitignore
* this will create a bundle.js in the public folder
* cut and paste babel into dependancies and remove from dev-dependencies

### Note: run postgress database
* type in terminal : heroku run bash
* then check that migrations directory in productions in knexFile.js is correct
also see :https://medium.com/modus-create-front-end-development/optimizing-webpack-production-build-for-react-es6-apps-a637e5692aea#.sdghfx639

# Creating a React App from scratch
* git clone repo
* npm init
* add .gitignore > add node_modules to ignore
## node modules to be installed:
* npm install express --save

# Installing Python
* ubuntu already has a python installed. To check the version: python --version
* if you want to check which version of python3 is installed: python3 --version
* To install latest version: sudo apt-get upgrade python3

# Installing Unity on Linux
* go to the unity forum for linux: https://forum.unity3d.com/threads/unity-on-linux-release-notes-and-known-issues.350256/
* scroll to the bottom to find the latest revision and download that.
* to uninstall unity type: sudo apt-get remove unity-editor -y

# Setting up emails

