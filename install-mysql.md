# Install MySQL

#### Install MySQL Server

1. Visit [http://dev.mysql.com/downloads/mysql/](http://dev.mysql.com/downloads/mysql/);
2. Download the latest .dmg archive;
3. Open the downloaded file and follow on-screen instructions;
4. You will receive a prompt window with the MySQL server password - store it in a temporary location;
5. Append the following to your .bash_profile;

  ```
  export PATH=${PATH}:/usr/local/mysql/bin
  ```

#### Setup MySQL Preference Pane

The _MySQL preference pane_ enables you to start, stop, and control MySQL server within _System Preferences_. 

To install MySQL preference pane follow the instructions here: [http://dev.mysql.com/doc/refman/5.6/en/macosx-installation-prefpane.html](http://dev.mysql.com/doc/refman/5.6/en/macosx-installation-prefpane.html)

Please note: The latest versions of the MySQL installer install the preference pane automatically. Check if you already have the preference pane installed. Go to _System Preferences_ and look for a _MySQL_ icon.

#### Reset your password

1. Open the _MySQL preference pane_;
2. Start the MySQL server;
3. Run the following in a terminal;

  ```bash
  mysql --user root --password
  ```
  
  Enter the server password you were given during MySQL server installation.
  
4. Execute the following SQL command;

  ```sql
  SET PASSWORD = PASSWORD('<new password/>');
  ```

5. Enter `quit` to exit the MySQL cli session;
6. Store password in a secure location, e.g. [KeePassX](https://www.keepassx.org/).

#### Install MySQL Workbench

MySQL Workbench is the official MySQL client. It's free, as in beer, and quite powerful.

1. Visit [http://dev.mysql.com/downloads/tools/workbench/](http://dev.mysql.com/downloads/tools/workbench/);
2. Download the latest .dmg archive;
3. Open the downloaded file and follow instructions.

#### Setup connection to local MySQL server

1. Run _MySQL Workbench_ that should already be installed in your system;
2. Go to `Database > Manage Connections...` from the top menu;
3. Hit the _New_ button from the bottom left corner;
4. Provide a meaningful connection name, e.g `root@localhost`;
5. Press the _Store in Keychain..._ button next to the _Password_ label;
6. Enter the server password you provided during password reset;
7. Hit the _Test connection_ button;
8. Assuming you got a success message, hit OK and your are done.
