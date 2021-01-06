# Install (clean) macOS Big Sur

### Download macOS Big Sur from the App Store

1. Open the App Store from an existing Mac installation;
2. Download macOS Big Sur;
3. Once downloaded, macOS Big Sur installer will run automatically; dismiss the installer window and proceed.

### Burn macOS Big Sur on a USB disk

1. Insert a blank USB disk (>= 13GB) to your machine;
2. Find the volume name in the terminal;

   ```bash
   ls -la /Volumes/
   ```

3. Run the following command, replacing `/Volumes/Untitled` with the actual name of your volume.

   ```bash
   sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled -- /Applications/Install\ macOS\ Big\ Sur.app --nointeraction
   ```

### Install macOS Big Sur

> Before you proceed with installing macOS please make sure you have backed up your previous settings, keys and data. If you need help to organize your thoughts, refer to our [backup guide](/backup.md).

1. Plug the USB disk to your machine;
2. Go to `System Settings > Startup Disk`;
3. Select the USB disk, i.e. something along the lines of _Install macOS Big Sur 11_, and hit _Restart_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

##### Alternatively, you also may do the following:

1. Turn on or restart your machine;
2. Immediatelly press and hold the _Option_ key;
3. Select the USB disk, i.e. something along the lines of _Install macOS Big Sur_, and hit _Enter_;
4. Follow the instructions on screen (be patient, this will take a couple of hours).

### Format your hard drive

Having booted into the _macOS Big Sur installer_ you are given the option to format your hard drive before installation. Do yourself a favour and choose _APFS (Case-Sensitive, Encrypted)_.

- Why _APFS_?

  _APFS_ is a newer file system, optimized for SSD and Flash Drives. If you are using a mechanical drive (highly unlikely) then revert to using the older _Mac OS Extended_ file system.

- Why _Case-Sensitive_?

  Because _Unix_. This guide is targeted towards devs.

- Why _Encrypted_?

  Because you live in an imperfect world. If your laptop gets stolen, at least your data will be protected.
