# Install Mac OSX Yosemite

### Download Yosemite from the App Store

1. Open the App Store from an existing Mac OSX installation;
2. Download Mac OSX Yosemite;
3. Once downloaded, Mac OSX Yosemite installer will run automatically; dismiss the installer window and proceed.

### Burn Yosemite on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine;
2. Find the volume name in terminal;

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume.

    ```bash
    sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
    ```

### Install Yosemite

1. Plug the USB key to your machine;
2. Go to `System Settings > Startup Disk`;
3. Select the USB disk, i.e. something along the lines of _Install OS X Yosemite 10.10.1_, and hit _Restart_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).
