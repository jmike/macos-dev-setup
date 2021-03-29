# Node.js

### Node version choice

Before proceeding with installation you need to consider the Node.js version you will be using. Essentially, there are two (2) options to choose from:

1. Long-time-support (LTS);
2. Latest Node.js version.

If you are new to Node.js, I would suggest to go with the LTS version to avoid incompatibilities with packages (such as strapi).

### Installation

1. Visit [https://nodejs.org/en/download/current](https://nodejs.org/en/download/current);
2. Download the dmg archive (`latest` or `LTS` - depending on your preference), which comes bundled with Node.js and the npm client. If you don't know which file to download look for the "macOS Installer";
3. Execute the downloaded file and follow instructions;
4. Verify node.js and npm have been installed.

   ```bash
   node --version
   ```

   ```bash
   npm --version
   ```

##### Alternative installation via Homebrew

###### Latest version

```bash
brew install node
```

###### LTS version

At the time of writing the LTS version is `14.x`.

```bash
brew install node@14
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

1. Append the following to your `~/.bash_profile` or `~/.zshrc`;

```bash
export NPM_TOKEN=$(cat ~/.npmrc | awk -F'authToken=' '{print $2;exit;}')
```

2. Create a new `/.npmrc` file in the root folder of your project, with the following contents;

```bash
//registry.npmjs.org/:_authToken=${NPM_TOKEN}
```
