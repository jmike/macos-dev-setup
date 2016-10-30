# Install Sublime Text 3

### Install Sublime Text 3

1. Visit [http://www.sublimetext.com/3](http://www.sublimetext.com/3);
2. Download the latest OSX build;
3. Open the downloaded dmg archive and move _Sublime Text 3_ to the _Applications_ folder.

### Enable external packages

_Package Control_ system is used to install external packages (i.e. add-ons) to Sublime. Unfortunately it's not part of the Sublime Text core distribution. So you need to install it manually.

1. Open _Sublime Text 3_;
2. Hit ``ctrl+` `` to access the console;
3. Copy paste the appropriate Python code from [https://packagecontrol.io/installation](https://packagecontrol.io/installation) and hit _Enter_.

### Install suggested plugins for JavaScript development

##### Install Material Theme for Sublime Text 3

Material theme is on of the most polished themes for _Sublime Text_. The easiest way to install is by using the _Sublime Package Control_ system.

1. Open _Sublime Text 3_;
2. Go to `Tools > Command Palette` or just hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _Material Theme_ and hit _Enter_.

##### Install SideBarEnhancements

1. Open _Sublime Text 3_;
2. Hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _SideBarEnhancements_ and hit _Enter_.

##### Install TrailingSpaces

1. Open _Sublime Text 3_;
2. Hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _TrailingSpaces_ and hit _Enter_.

##### Configure Sublime Text

1. Go to `Sublime Text 3 > Preferences > Settings - User`;
2. Copy past the following settings:

  ```json
  {
    "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
    "ensure_newline_at_eof_on_save": true,
    "fallback_encoding": "UTF-8",
    "font_size": 17,
    "ignored_packages": [
      "Markdown",
      "Vintage"
    ],
    "indent_guide_options": [
      "draw_normal",
      "draw_active"
    ],
    "jsdocs_align_tags": "no",
    "line_padding_bottom": 1,
    "line_padding_top": 1,
    "material_theme_contrast_mode": true,
    "material_theme_tabs_separator": true,
    "overlay_scroll_bars": "enabled",
    "rulers": [
      120
    ],
    "tab_size": 2,
    "theme": "Material-Theme.sublime-theme",
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true,
    "folder_exclude_patterns": [
      ".svn", ".git", ".hg", "CVS",
      "node_modules",
      "bower_components"
    ]
  }
  ```

### Make Sublime Text available in terminal

Sublime Text 3 ships with a CLI called `subl`. Create a symbolic link to your CLI and you are done.

```bash
sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```
