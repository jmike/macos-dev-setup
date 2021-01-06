# zsh

Z shell comes pre-bundled with macOS Catalina (10.15) and above. This guide will help you configure zsh with code-completion, useful aliases and theming.

### Manual installation

> Note: ignore if you are using macOS 10.15+

If you are using an earlier macOS version, you will need to install zsh manually.

1. Make sure you have installed Homebrew on your system - if not, read the [Homebrew](homebrew.md) guide;

   ```bash
   which brew
   ```

2. Open terminal and run the following command:

   ```bash
   brew install zsh
   ```

3. Restart your terminal.

### Oh-my-zsh

[Oh my zsh](https://ohmyz.sh/) is a plugin system for zsh that allows you to easily expand your terminal with additional features.

##### Installation

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Powerlevel10k theme

[Powerlevel10k](https://github.com/romkatv/powerlevel10k) is an excellent theme for zsh.

##### Installation

1. Download and install the _Meslo Nerd Font_ on your local machine.

   - [MesloLGS NF Regular.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf)
   - [MesloLGS NF Bold.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf)
   - [MesloLGS NF Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf)
   - [MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf)

   Double-click on each file and click "Install".

2. Configure _Apple Terminal_ to use the _Meslo Nerd Font_.

   Open _Terminal → Preferences → Profiles → Text_, click _Change_ under _Font_ and select `MesloLGS NF` family.

   I suggest to also change the font-size to `13px`.

3. Download _Powerlevel10k_

   ```bash
   git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
   ```

4. Enable _Powerlevel10k_ in `~/.zshrc`

   Edit `~/.zshrc` with your editor and set the following variable.

   ```bash
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```

5. Configure _Powerlevel10k_ theme (if it doesn't automatically trigger the configuration wizard)

   ```bash
   p10k configure
   ```

### Plugins

Plugins are mostly meant for code completion. If you are a JavaScript developer like me, you could start with the following.

```
git
npm
yarn
extract
```

### Aliases

Aliases adhere to each developer's personal preference. My only suggestion would be to use the following.

```bash
alias ll="ls -la"
```

1. Open `~/.zshrc` with your favourite editor.
2. Append the lines above either at the end of the file or at the relevant section.
