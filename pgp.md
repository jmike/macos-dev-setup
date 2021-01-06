# PGP

PGP is a suite of encryption tools that allows you to send and receive messages securely. You may use it to communicate via email, IM or other communication tool.

### Installation

1. Visit [https://gpgtools.org/](https://gpgtools.org/);
2. Download the latest .dmg archive;
3. Install GPG Suite on your machine.

##### Alternative installation via Homebrew

```bash
brew install --cask gpg-suite
```

##### Verify installation

1. Open a browser.
2. Write some text in a textbox.
3. Select and right click on the text.
4. You should be able to see several _OpenPGP_ options under the _Services_ menu.

### Keyboard shortcuts

1. Go to _System Preferences_ > _Keyboard_ > _Shortcuts_;
2. Select _Services_ from the left pane;
3. Scroll down to the _Text_ section. Locate entries starting with "OpenPGP:". Go through each entry, unchecking and deleting its keyboard shortcut.
4. Set four new shortcuts, i.e.

| Entry                                  | Shortcut |
| :------------------------------------- | :------: |
| OpenPGP: Decrypt Selection             |   ⌃⌥⌘-   |
| OpenPGP: Encrypt Selection             |   ⌃⌥⌘-   |
| OpenPGP: Sign Selection                |   ⌃⌥⌘[   |
| OpenPGP: Verify Signature of Selection |   ⌃⌥⌘[   |

### Create new PGP Key pair

1. Open the _GPG Keychain_ app that should be already installed in your system;
2. Click _New_ from the top menu;
3. Type in your full name and email address.
4. Check the _Upload public key_ option;
5. Enter a secure passphrase twice (x2) under _Advanced options_;
6. Hit _Generate Key_.

### Export a PGP Key

1. Open the _GPG Keychain_ app;
2. Select the key you want to export - it should now be highlighted;
3. Click _Export_ from the top menu;
4. Make sure to check the _Include secret key in exported file_ option, assuming you want to export a public/private key pair;
5. Select the directory to save the exported key;
6. Hit _Save_.

### Import a PGP Key

1. Open the _GPG Keychain_ app;
2. Click _Import_ from the top menu;
3. Select the file you want to import from your filesystem - it should normally end in `.asc`;
4. Hit _Open_.
