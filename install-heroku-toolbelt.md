# Install Heroku CLI

Heroku Toolbelt is a must have if you are using [Heroku](http://www.heroku.com) to host your applications.

### Install Heroku ToolBelt

1. Visit [https://toolbelt.heroku.com/](https://toolbelt.heroku.com/);
2. Download the latest OS X installer;
3. Open the downloaded file and follow instructions;
4. Verify heroku toolbelt has been installed by running the following command.

  ```bash
  heroku --version
  ```
  
### Install heroku-config plugin

Heroku-config is a plugin that allows you to push your .env file to heroku by simply running `heroku config:push`. Similarity you can populate your local .env file by running `heroku config:pull`.

1. Make sure you are running Node.js v.6+;

  ```bash
  node --version
  ```
  
2. Install heroku-config by running the following command.

  ```bash
  heroku plugins:install heroku-config
  ```
