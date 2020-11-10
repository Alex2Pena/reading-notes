1. Set up
- requires Git
- create a login
1. Prepare the app
- $ git clone https://github.com/heroku/node-js-getting-started.git
- $ cd node-js-getting-started
1. Deploy the app
- $ heroku create
- $ git push heroku master
- $ heroku ps:scale web=1
- $ heroku open
1. View logs
- $ heroku logs --tail
1. Define a Procfile
- Use a Procfile, a text file in the root directory of your application, to explicitly declare what command should be executed to start your app.
1. Scale the app
- Right now, your app is running on a single web dyno. Think of a dyno as a lightweight container that runs the command specified in the Procfile.
1. Declare app dependencies
- Heroku recognizes an app as Node.js by the existence of a package.json file in the root directory. For your own apps, you can create one by running npm init --yes.
1. Run the app locally
- Now start your application locally using the heroku local command, which was installed as part of the Heroku CLI:
1. Push local changes
- Begin by adding a dependency for cool-ascii-faces in package.json
- npm install cool-ascii-faces
1. Provision add-ons
- Add-ons are third-party cloud services that provide out-of-the-box additional services for your application, from persistence through logging to monitoring and more.
1. Start a console
- To get a real feel for how dynos work, you can create another one-off dyno and run the bash command, which opens up a shell on that dyno. You can then execute commands there. Each dyno has its own ephemeral filespace, populated with your app and its dependencies - once the command completes (in this case, bash), the dyno is removed.
1. Define config vars
- Heroku lets you externalize configuration - storing data such as encryption keys or external resource addresses in config vars.
1. Provision a database
- The add-on marketplace has a large number of data stores, from Redis and MongoDB providers, to Postgres and MySQL. In this step, you will add a free Heroku Postgres Starter Tier dev database to your app.
