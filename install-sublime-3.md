# Install Sublime Text 3

Download and install Sublime Text from [http://www.sublimetext.com/3](http://www.sublimetext.com/3).

#### Install Package Control

The next step is to install the Package Control system, as it isn't a part of the Sublime Text baseline. This involves cutting and pasting some Python code into the Sublime Text console. You can find further info at [https://packagecontrol.io/installation](https://packagecontrol.io/installation).

#### Install Spacegray theme

The easiest way to install is using Sublime Package Control, where Spacegray is listed as Theme - Spacegray.

1. Go to `Sublime Text 3 > Tools > Command Palette` or open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _Theme - Spacegray_ and hit _Enter_.

#### Install Spacegray theme

The easiest way to install is using Sublime Package Control, where Spacegray is listed as Theme - Spacegray.

1. Open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _Theme - Spacegray_ and hit _Enter_.

#### Install DocBlockr

The DocBlockr package provides creation and code completion of comment blocks.

1. Open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _DocBlockr_ and hit _Enter_.

#### Install SublimeLinter

1. Open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _SublimeLinter_ and hit _Enter_.

#### Install jshint

1. Make sure you have already installed node.js and npm - if not, read the [Install node.js and npm](install-node-npm.md) guide;
2. Install jshint by typing the following in a terminal:
  
  ```bash
  sudo npm install -g jshint
  ```

#### Install SublimeLinter-jshint

1. Make sure you have installed SublimeLinter and jshint;
2. Open Sublime Text 3 and hit `Command + Shift + P`;
3. Choose _Package Control: Install Package_;
4. Find _SublimeLinter-jshint_ and hit _Enter_.

#### Install TernJS

1. Open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _TernJS_ and hit _Enter_.

#### Install SideBarEnhancements

1. Open Sublime Text 3 and hit `Command + Shift + P`;
2. Choose _Package Control: Install Package_;
3. Find _SideBarEnhancements_ and hit _Enter_.

#### Configure Sublime Text

1. Go to `Sublime Text 3 > Preferences > Settings - User`;
2. Copy past the following settings:

	```json
	{
		"color_scheme": "Packages/User/base16-ocean.dark (SL).tmTheme",
		"ensure_newline_at_eof_on_save": true,
		"fallback_encoding": "UTF-8",
		"font_size": 14,
		"ignored_packages":
		[
			"Vintage"
		],
		"jsdocs_align_tags": "no",
		"line_padding_bottom": 1,
		"line_padding_top": 1,
		"rulers":
		[
			120
		],
		"tab_size": 2,
		"theme": "Spacegray.sublime-theme",
		"translate_tabs_to_spaces": true,
		"trim_trailing_white_space_on_save": true
	}
	```
