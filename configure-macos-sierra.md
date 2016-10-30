# Configure macOS Sierra

#### Allow Apps from Anywhere

MacOS Sierra prevents executing unsigned apps. This can be very annoying, especially if you are a developer and tend to experiment with new apps on a regular basis.

1. Disable the macOS assessment subsystem;

  ```bash
  sudo spctl --master-disable
  ```  
2. Go to `System Preferences > Security & Privacy`;
3. Select `Anywhere` under the `Allow apps downloaded from` section.
 
Beware! With great power comes great responsibility.
