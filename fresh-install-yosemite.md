# Fresh-install Mac OSX Yosemite

#### A. Download Yosemite from the App Store

1. Open the App Store from your existing Mac installation
2. Search and download Mac OSX Yosemite
3. Once Yosemite has been downloaded, the installer will run automatically - dismiss the installer window and proceed

#### B. Burn Yosemite on a USB disk

1. Insert a blank USB disk (>= 8GB) to your computer
2. Detect the volume name in terminal

    ```bash
    ls -la /Volumes/
    ```

3. Run the following command, replacing _/Volumes/Untitled_ with the name of your volume
    ```bash
    sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
    ```

#### C. Install Yosemite
  
1. Plug the USB key and restart
2. Follow the installer instructions
