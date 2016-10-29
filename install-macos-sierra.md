# Install macOS Sierra

#### Download macOS Sierra from the App Store

1. Open the App Store from an existing Mac installation;
2. Download macOS Sierra;
3. Once downloaded, macOS Sierra installer will run automatically; dismiss the installer window and proceed.

#### Burn macOS Sierra on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine;
2. Find the volume name in terminal;

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume.

    ```bash
    sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ macOS\ Sierra.app --nointeraction
    ```

#### Install macOS Sierra
  
1. Plug the USB key to your machine;
2. Go to `System Settings > Startup Disk`;
3. Select the USB disk, i.e. something along the lines of _Install macOS Sierra 10.12_, and hit _Restart_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

###### Alternatively, you also may do the following:

1. Turn on or restart your machine;
2. Immediatelly press and hold the _Option_ key;
3. Select the USB disk, i.e. something along the lines of _Install macOS Sierra_, and hit _Enter_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

#### Format your hard drive

Having boot into the _macOS Sierra installer_ you are given the option to format your hard drive before installation. Do yourself a favour and choose _Mac OS Extended (Case-Sensitive, Journaled, Encrypted)_.

- Why _Case-Sensitive_? Because _Unix_.
- Why _Encrypted_? Because if you leave your data unencrypted and your machine gets stolen... boom.
