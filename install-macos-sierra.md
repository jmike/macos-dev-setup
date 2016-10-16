# Install macOS Sierra

#### Download Sierra from the App Store

1. Open the App Store from an existing Mac installation;
2. Download macOS Sierra;
3. Once downloaded, macOS Sierra installer will run automatically; dismiss the installer window and proceed.

#### Burn Sierra on a USB disk

1. Insert a blank USB disk (>= 8GB) to your machine;
2. Find the volume name in terminal;

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume.

    ```bash
    sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ macOS\ Sierra.app --nointeraction
    ```

#### Install Sierra
  
1. Plug the USB key to your machine;
2. Go to `System Settings > Startup Disk`;
3. Select the USB disk, i.e. something along the lines of _Install macOS Sierra 10.10.1_, and hit _Restart_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

##### Alternatively, you may do the following:

1. Turn on or restart your machine.
2. Immediatelly press and hold the _Option_ key.
3. Select the USB disk, i.e. something along the lines of _Install macOS Sierra_, and hit _enter_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).
