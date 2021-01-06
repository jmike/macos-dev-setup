# Sublime Text 3

### Installation

1. Visit [http://www.sublimetext.com/3](http://www.sublimetext.com/3);
2. Download the latest OSX build;
3. Open the downloaded dmg archive and move _Sublime Text 3_ to the _Applications_ folder.

### Make Sublime Text available in the terminal

Make Sublime Text 3 available in the terminal by creating a symbolic link to its CLI.

```bash
sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

You can now open a file from the terminal as follows:

```bash
subl <file>
```

### Enable external packages

_Package Control_ system is used to install external packages (i.e. add-ons) to Sublime. Unfortunately it's not part of the Sublime Text core distribution. So you need to install it manually.

1. Open _Sublime Text 3_;
2. Hit `` ctrl+`  `` to access the console;
3. Copy paste the appropriate Python code from [https://packagecontrol.io/installation](https://packagecontrol.io/installation) and hit _Enter_.

### Configure Sublime Text 3

##### Install Material Theme for Sublime Text 3

Material theme is on of the most polished themes for _Sublime Text_. The easiest way to install is by using the _Sublime Package Control_ system.

1. Open _Sublime Text 3_;
2. Go to `Tools > Command Palette` or just hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _Material Theme_ and hit _Enter_.

##### Install SideBarEnhancements

1. Open _Sublime Text 3_ and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _SideBarEnhancements_ and hit _Enter_.

##### Install TrailingSpaces

1. Open _Sublime Text 3_ and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _TrailingSpaces_ and hit _Enter_.

##### Update Sublime Text preferences

1. Go to `Sublime Text 3 > Preferences > Settings - User`;
2. Copy past the following settings:

```json
{
  "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
  "ensure_newline_at_eof_on_save": true,
  "fallback_encoding": "UTF-8",
  "font_size": 17,
  "ignored_packages": ["Markdown", "Vintage"],
  "indent_guide_options": ["draw_normal", "draw_active"],
  "jsdocs_align_tags": "no",
  "line_padding_bottom": 1,
  "line_padding_top": 1,
  "material_theme_contrast_mode": true,
  "material_theme_tabs_separator": true,
  "overlay_scroll_bars": "enabled",
  "rulers": [120],
  "tab_size": 2,
  "theme": "Material-Theme.sublime-theme",
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true,
  "folder_exclude_patterns": [
    ".svn",
    ".git",
    ".hg",
    "CVS",
    "node_modules",
    "bower_components"
  ]
}
```

### Install packages for JavaScript development

Make sure you have already installed the _Sublime Package Control_ system.

##### Install DocBlockr

The DocBlockr package provides creation and code completion of comment blocks.

1. Open _Sublime Text 3_ and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _DocBlockr_ and hit _Enter_.

##### Install SublimeLinter (if not already installed)

1. Open _Sublime Text 3_ and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _SublimeLinter_ and hit _Enter_.

##### Install ESLint

1. Make sure you have already installed Node.js and npm - if not, follow the [Install node.js and npm](install-node-npm.md) guide;
2. Install ESLint by typing the following in a terminal:

```bash
sudo npm install -g eslint
```

3. Install eslint-config-airbnb

```bash
sudo npm install -g eslint-config-airbnb eslint-plugin-react eslint-plugin-jsx-a11y eslint-plugin-import
```

##### Install SublimeLinter-eslint

1. Make sure you have installed SublimeLinter and eslint;
2. Open _Sublime Text 3_ and hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _SublimeLinter-contrib-eslint_ and hit _Enter_.
