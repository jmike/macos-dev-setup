# Secure macOS Big Sur

### Install System Updates

1. Open the _App Store_ and go to `Updates`;
2. Install latest system updates.

### Encypt your hard disk

It's imperative to encrypt your hard disk, assuming you haven't already done so during OS installation.

1. Go to `System Settings > Security & Privacy > FileVault`;
2. Turn on FileVault; make sure you don't share your encryption key with Apple (kinda beats the purpose of encryption).

### Disable Spotlight Suggestions

1. Go to `System Preferences > Spotlight > Search Results`;
2. Disable everything, except _Applications_ and _System Settings_.

### Enable Cloudflare DNS

1. Go to `System Preferences > Network`;
2. Select _Wi-Fi_ from the left-hand pane and click the _Advanced_ button;
3. Open the _DNS_ tab;
4. Add the following IP addresses (click the + button under the DNS Servers, repeat where applicable);
  - 1.1.1.1
  - 1.0.0.1
  - 2606:4700:4700::1111
  - 2606:4700:4700::1001
5. Hit _OK_.

You might want to repeat the process for your _Ethernet_ interface.

### Enable Find My Mac (optional)

Enabling _Find My Mac_ is optional and mostly makes sense for remote devices, such as laptops.

1. Go to `System Preferences > iCloud`;
2. Log in to iCloud;
3. Select the Find My Mac checkbox.

If the worst happens and your machine get's stolen, you will be able to track it, remotely lock it, and send messages to its screen via iCloud.com or the _Find My iPhone_ app for iPad/iPhone.
