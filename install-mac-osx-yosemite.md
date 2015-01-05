# Install Mac OSX Yosemite

#### A. Download Yosemite from the App Store

1. Open the App Store from an existing Mac OSX installation
2. Download Mac OSX Yosemite
3. Once downloaded, Mac OSX Yosemite installer will run automatically; dismiss the installer window and proceed

#### B. Burn Yosemite on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine
2. Find the volume name in terminal

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume

    ```bash
    sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
    ```

#### C. Install Yosemite
  
1. Plug the USB key to your machine
2. Go to `System Settings > Startup Disk`
3. Select the USB disk, i.e. something along the lines of _Install OS X Yosemite 10.10.1_, and hit _Restart_
4. Follow the instructions on screen (be patient, this will take a couple of hours)

#### D. Fix Privacy Settings

Once Mac OSX Yosemite is installed, you 'd want to change the privacy settings to prevent your system from sending Apple all kind of data.

1. Encypt your HDD
    1. Go to `System Settings > Security & Privacy > FileVault`
    2. Turn on FileVault; make sure you don't share your encryption key with Apple (beats the purpose)

2. Disable spotlight suggestions
  1. Go to `System Preferences > Spotlight > Search Results`
  2. Disable _Spotlight Suggestions_ and _Bing Web Searches_; you can disable more categories if you like (I only have Applications and System Settings categories)

3. Disable safari spotlight suggestions
  
    You would think that you already disabled _Spotlight Suggestions_. You are wrong.
  
  1. Go to `Safari > Preferences > Search`
  2. Uncheck the _Include Spotlight Suggestions_ option
