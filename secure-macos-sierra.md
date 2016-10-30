# Secure macOS Sierra

### Install System Updates

1. Open the _App Store_ and go to `Updates`;
2. Install latest system updates.

### Encypt your hard disk

It's imperative to encrypt your hard disk, assuming you haven't already done during setup.

1. Go to `System Settings > Security & Privacy > FileVault`;
2. Turn on FileVault; make sure you don't share your encryption key with Apple (beats the purpose of encryption).

### Disable Spotlight Suggestions

1. Go to `System Preferences > Spotlight > Search Results`;
2. Disable _Spotlight Suggestions_ and _Bing Web Searches_.

You might want to consider disabling more Spotlight Search categories. A good suggestion is to keep only _Applications_ and _System Settings_.

##### Disable Safari Spotlight Suggestions

You might think that by disabling Spotlight Suggestions you are done - you are wrong.

1. Go to `Safari > Preferences > Search`;
2. Uncheck the _Include Spotlight Suggestions_ option.

### Enable Google DNS

1. Go to `System Preferences > Network`;
2. Select _Wi-Fi_ from the left-hand pane and click the _Advanced_ button;
3. Open the _DNS_ tab;
4. Click the + button under the DNS Servers and type `8.8.8.8`;
5. Click and + button (again) and type `8.8.4.4`;
6. Hit _OK_.

You might want to repeat the process for your _Ethernet_ interface.

### Enable Find My Mac (optional)

Enabling _Find My Mac_ is optional and mostly makes sense for remote devices, such as laptops.

1. Go to `System Preferences > iCloud`;
2. Log in to iCloud;
3. Select the Find My Mac checkbox.

If the worst happens and your machine get's stolen, you will be able to track it, remotely lock it, and send messages to its screen via iCloud.com or the _Find My iPhone_ app for iPad/iPhone.
