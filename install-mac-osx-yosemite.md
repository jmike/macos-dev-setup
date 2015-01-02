# Install Mac OSX Yosemite

#### A. Download Yosemite from the App Store

1. Open the App Store from an existing Mac installation;
2. Download Mac OSX Yosemite;
3. Once downloaded, the Mac OSX Yosemite installer will run automatically; dismiss the installer window and proceed

#### B. Burn Yosemite on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine
2. Detect the volume name in terminal

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
3. Select the USB disk, i.e. something along the lines of `Install OS X Yosemite 10.10.1`, and hit `Restart`
4. Follow the instructions on screen (be patient, this should take a couple of hours)
