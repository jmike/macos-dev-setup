# Install git

Git comes pre-installed on the latest Mac OSX distributions. However, Apple's bundled version of Git is not as well-maintained as the official Git repo.

#### Install via Homebrew

1. Make sure you have installed Homebrew on your system - if not, read the [Install Homebrew](install-homebrew.md) guide;

    ```bash
    which brew
    ```

2. Open terminal and run the following command:

    ```bash
    brew install git
    ```

3. Verify git has been installed.

    ```bash
    git --version
    ```

#### Configure Git

1. Set Git editor;

  ```bash
  git config --global core.editor "nano"
  ```
  
2. Set Git default push behaviour;

  ```bash
  git config --global push.default simple
  ```

#### Add Git completion in bash

1. Create configuration files;
    
    ```bash
    touch ~/.bash_profile
    touch ~/.git-completion.bash
    touch ~/.git-prompt.sh
    ```

2. Populate `.git-completion.bash` with [https://github.com/git/git/blob/master/contrib/completion/git-completion.bash](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash);
3. Populate `.git-prompt.sh` with [https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh);
4. Update permissions of `.git-completion.bash` and `.git-prompt.sh`;
    
    ```bash
    chmod 755 ~/.git-completion.bash
    chmod 755 ~/.git-prompt.sh
    ```

5. Populate `.bash_profile`, as follows:

    ```bash
    #!/bin/bash
    
    export PATH="/usr/local/bin:$PATH"
    
    source ~/.git-completion.bash
    source ~/.git-prompt.sh
    
    MAGENTA="\[\033[0;35m\]"
    YELLOW="\[\033[0;33m\]"
    BLUE="\[\033[34m\]"
    LIGHT_GRAY="\[\033[0;37m\]"
    CYAN="\[\033[0;36m\]"
    GREEN="\[\033[0;32m\]"
    GIT_PS1_SHOWDIRTYSTATE=true
    export LS_OPTIONS='--color=auto'
    export CLICOLOR='Yes'
    export LSCOLORS=gxfxbEaEBxxEhEhBaDaCaD
    
    export PS1=$LIGHT_GRAY"\u@\h"'$(
        if [[ $(__git_ps1) =~ \*\)$ ]]
        # a file has been modified but not added
        then echo "'$YELLOW'"$(__git_ps1 " (%s)")
        elif [[ $(__git_ps1) =~ \+\)$ ]]
        # a file has been added, but not commited
        then echo "'$MAGENTA'"$(__git_ps1 " (%s)")
        # the state is clean, changes are commited
        else echo "'$CYAN'"$(__git_ps1 " (%s)")
        fi)'$BLUE" \w"$GREEN": "
    
    alias ll='ls -lah'
    alias gg='git status -s'
    ```

Please note: You need to restart your terminal for the settings to take effect.
