# Setup PGP

#### Install GPG Suite

1. Visit [https://gpgtools.org/](https://gpgtools.org/);
2. Download the latest .dmg archive;
3. Install GPG Suite on your machine.

###### Verify installation

* Open a browser.
* Write some text in a textbox.
* Select and right click on the text.
* You should be able to see several _OpenPGP_ options under the _Services_ menu.

#### Set PGP Keyboard shortcuts

1. Go to _System Preferences_ > _Keyboard_ > _Shortcuts_;
2. Select _Services_ from the left pane;
3. Scroll down to the _Text_ section. Locate entries starting with "OpenPGP:". Go through each entry, unchecking and deleting its keyboard shortcut.
4. Set four new shortcuts, i.e.

| Entry | Shortcut |
| :------------- |:-------------:|
| OpenPGP: Decrypt Selection | ⌃⌥⌘- |
| OpenPGP: Encrypt Selection | ⌃⌥⌘- |
| OpenPGP: Sign Selection | ⌃⌥⌘[ |
| OpenPGP: Verify Signature of Selection | ⌃⌥⌘[ |

#### Create new PGP Key pair

* Open the _GPG Keychain_ app that should be already installed in your system;
* Click _New_ from the top menu;
* Type in your full name and email address.
* Check the _Upload public key_ option;
* Enter a secure passphrase twice (x2) under _Advanced options_;
* Hit _Generate Key_.

#### Export a PGP Key

* Open the _GPG Keychain_ app;
* Select the key you want to export - it should now be highlighted;
* Click _Export_ from the top menu;
* Make sure to check the _Include secret key in exported file_ option, assuming you want to export a public/private key pair;
* Select the directory to save the exported key;
* Hit _Save_.

#### Import a PGP Key

* Open the _GPG Keychain_ app;
* Click _Import_ from the top menu;
* Select the file you want to import from your filesystem - it should normally end in `.asc`;
* Hit _Open_.
