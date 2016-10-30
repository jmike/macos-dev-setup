# Configure Sublime Text 3 for JavaScript development

Make sure you have already installed the _Sublime Package Control_ system. If not, please refer to the [Install Sublime Text 3](install-sublime-3.md) guide.

### Install DocBlockr

The DocBlockr package provides creation and code completion of comment blocks.

1. Open _Sublime Text 3_;
2. Hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _DocBlockr_ and hit _Enter_.

### Install SublimeLinter (if not already installed)

1. Open _Sublime Text 3_;
2. Hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _SublimeLinter_ and hit _Enter_.

### Install ESLint

1. Make sure you have already installed Node.js and npm - if not, follow the [Install node.js and npm](install-node-npm.md) guide;
2. Install ESLint by typing the following in a terminal:

  ```bash
  sudo npm install -g eslint
  ```
3. Install eslint-config-airbnb

  ```bash
  sudo npm install -g eslint-config-airbnb eslint-plugin-react eslint-plugin-jsx-a11y eslint-plugin-import
  ```

### Install SublimeLinter-eslint

1. Make sure you have installed SublimeLinter and eslint;
2. Open _Sublime Text 3_;
3. Hit `Command + Shift + P`;
4. Choose _Package Control: Install Package_;
5. Find _SublimeLinter-contrib-eslint_ and hit _Enter_.
