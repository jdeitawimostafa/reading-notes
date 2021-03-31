# summarizing : 

Heroku Deployment
Heroku with Node.js
$ brew install heroku/brew/heroku

We have to install Heroku first. (run this command from Terminal (Mac OS))
$ heroku login

Command opens your web browser to the Heroku login page.
$ node --version
$ npm --version
$ git --version

Before you continue, check that you have the prerequisites installed properly.
Prepare the app
In this step, you will prepare a sample application that’s ready to be deployed to Heroku.

To clone a local version of the sample application that you can then deploy to Heroku, execute the following commands in your local command shell or terminal:


$ git clone https://github.com/heroku/node-js-getting-started.git
$ cd node-js-getting-started

You now have a functioning Git repository that contains a simple application as well as a package.json file, which is used by Node’s dependency manager.

$ heroku create

Command creates an app on Heroku, which prepares Heroku to receive source code.
$ git push heroku main

Command deploys your code
$ heroku ps:scale web=1

Command ensures that at least one instance of the app is running.
$ heroku open

Command allows to visit deployed app
View logs
Heroku treats logs as streams of time-ordered events aggregated from the output streams of all your app and Heroku components, providing a single channel for all of the events.


$ heroku logs --tail
2011-03-10T10:22:30-08:00 heroku[web.1]: State changed from created to starting
2011-03-10T10:22:32-08:00 heroku[web.1]: Running process with command: `npm start`
2011-03-10T10:22:33-08:00 heroku[web.1]: Listening on 18320
2011-03-10T10:22:34-08:00 heroku[web.1]: State changed from starting to up

Define a Procfile
Use a Procfile, a text file in the root directory of your application, to explicitly declare what command should be executed to start your app.

The Procfile in the example app you deployed looks like this:

web: npm start
Scale the app
Right now, your app is running on a single web dyno. Think of a dyno as a lightweight container that runs the command specified in the Procfile.

You can check how many dynos are running using the ps command:

$ heroku ps
Scaling an application on Heroku is equivalent to changing the number of dynos that are running. Scale the number of web dynos to zero:
$ heroku ps:scale web=0
Access the app again by hitting refresh on the web tab, or heroku open to open it in a web tab. You will get an error message because you no longer have any web dynos available to serve requests.
Scale it up again:

$ heroku ps:scale web=1
Declare app dependencies
Heroku recognizes an app as Node.js by the existence of a package.json file in the root directory. For your own apps, you can create one by running npm init --yes.

The demo app you deployed already has a package.json, and it looks something like this:


{
  "name": "node-js-getting-started",
  "version": "0.3.0",
  ...
  "engines": {
    "node": "14.x"
  },
  "dependencies": {
    "ejs": "^3.1.5",
    "express": "^4.17.1"
  },
  ...
}

Run this command in your local directory to install the dependencies, preparing your system for running the app locally:

$ npm install

Once dependencies are installed, you will be ready to run your app locally. You’ll notice that a package-lock.json file is generated when npm install is run.
Run the app locally
Now start your application locally using the heroku local command, which was installed as part of the Heroku CLI:

$ heroku local web
Push local changes
In this step you’ll learn how to propagate a local change to the application through to Heroku. As an example, you’ll modify the application to add an additional dependency and the code to use it.

Begin by adding a dependency for cool-ascii-faces in package.json. Run the following command to do this:

$ npm install cool-ascii-faces
Modify index.js so that it requires this module at the start. Also add a new route (/cool) that uses it. Your final code should look like this:


const cool = require('cool-ascii-faces');
const express = require('express');
const path = require('path');
const PORT = process.env.PORT || 5000;

express()
  .use(express.static(path.join(__dirname, 'public')))
  .set('views', path.join(__dirname, 'views'))
  .set('view engine', 'ejs')
  .get('/', (req, res) => res.render('pages/index'))
  .get('/cool', (req, res) => res.send(cool()))
  .listen(PORT, () => console.log(`Listening on ${ PORT }`));

Now test locally: ```
$ npm install $ heroku local

```

Now deploy. Almost every deploy to Heroku follows this same pattern. First, add the modified files to the local git repository:

$ git add .
Now commit the changes to the repository:

$ git commit -m "Add cool face API"
Now deploy, just as you did previously:

$ git push heroku main
Finally, check that everything is working:

$ heroku open cool
You should see another face.