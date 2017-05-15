# Install Node.js & npm

### Install Node.js & npm

1. Visit [https://nodejs.org/en/download/current](https://nodejs.org/en/download/current);
2. Download the latest Node.js dmg archive, which comes bundled with the npm client. If you don't know which file to download look for the "macOS Installer";
3. Execute the dowloaded file and follow instructions;
4. Verify node.js and npm have been installed.

    ```bash
    node --version
    ```

    ```bash
    npm --version
    ```

### Login to npm

If you are planning to publishing modules to the npm registry you should login with your npm account.

1. Visit [https://www.npmjs.com/signup](https://www.npmjs.com/signup) and create a npm account. Skip this step if you already have a npm account;
2. Login to npm from your machine;

    ```bash
    npm login
    ```

3. Verify you are logged in to npm.

    ```bash
    npm whoami
    ```

    You should be able to see your username displayed in the terminal.
    
### Working with private modules

1. Append the following to your .bash_profile;

  ```bash
  export NPM_TOKEN=$(cat ~/.npmrc | awk -F'authToken=' '{print $2}')
  ```

2. Create a new `/.npmrc` file in the root folder of your project, with the following contents;

  ```bash
  //registry.npmjs.org/:_authToken=${NPM_TOKEN}
  ```

