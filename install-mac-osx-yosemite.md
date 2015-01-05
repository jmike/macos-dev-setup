# Install Mac OSX Yosemite

#### A. Download Yosemite from the App Store

1. Open the App Store from an existing Mac OSX installation;
2. Download Mac OSX Yosemite;
3. Once downloaded, Mac OSX Yosemite installer will run automatically; dismiss the installer window and proceed.

#### B. Burn Yosemite on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine;
2. Find the volume name in terminal;

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume.

    ```bash
    sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
    ```

#### C. Install Yosemite
  
1. Plug the USB key to your machine;
2. Go to `System Settings > Startup Disk`;
3. Select the USB disk, i.e. something along the lines of _Install OS X Yosemite 10.10.1_, and hit _Restart_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

#### D. Install System Updates

Before doing anything with your new OS, make sure you install the latest system updates.

1. Open the App Store and to `Updates`;
2. Install all system updates.

#### E. Fix Security & Privacy

1. Encypt your HDD
    1. Go to `System Settings > Security & Privacy > FileVault`;
    2. Turn on FileVault; make sure you don't share your encryption key with Apple (beats the purpose of encrypting).

2. Disable Spotlight Suggestions
  1. Go to `System Preferences > Spotlight > Search Results`;
  2. Disable _Spotlight Suggestions_ and _Bing Web Searches_.
    
    You might want to disable more Spotlight Search categories, e.g. I only have _Applications_ and _System Settings_ enabled.

3. Disable Safari Spotlight Suggestions
  
    You would think you already disabled Spotlight Suggestions - you are wrong.
  
  1. Go to `Safari > Preferences > Search`;
  2. Uncheck the _Include Spotlight Suggestions_ option.

4. Enable Google DNS
  
  1. Go to `System Preferences > Network`;
  2. Select _Wi-Fi_ from the left-hand pane and click the _Advanced_ button;
  3. Open the _DNS_ tab;
  4. Click the + button under the DNS Servers and type `8.8.8.8`;
  5. Click and + button (again) and type `8.8.4.4`;
  6. Hit _OK_.
  
  You might want to repeat the process for the _Ethernet_ interface.
