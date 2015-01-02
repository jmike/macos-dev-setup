# Install git

Git comes pre-installed on the latest Mac OSX distributions. However, Apple's bundled version of Git is not as well-maintained as the official Git repo.

#### A. Install Git from Homebrew

If you don't yet have Homebrew installed, read the [Install Homebrew](install-homebrew.md) guide. Also make sure you have already installed Apple XCode from the App Store.

```bash
brew install git
```

#### B. Configure Git on your Mac

1. Create the configuration files
    
    ```bash
    touch ~/.bash_profile
    touch ~/.git-completion.bash
    touch ~/.git-prompt.sh
    ```

2. Populate `.git-completion.bash` with contents located here: [https://github.com/git/git/blob/master/contrib/completion/git-completion.bash](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)
3. Populate `.git-prompt.sh` with contents located here: [https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh)
4. Update permissions of `.git-completion.bash` and `.git-prompt.sh`, respectively
    
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

#### C. Restart your terminal

1. Restart your terminal for the settings to take effect
2. Verify that you have the latest git installed
    
    ```bash
    git --version
    ```
