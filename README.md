# Dotfiles

My personal **config files for Linux**.

![Demo Image](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/images/demo.png)

The installation will not just **_symbolically link all config files to the right place_** but also **_install some packages with appropriate Package Manager_** of your distros.

Although I tried to calculate all possible failures can happen, but you may need to manually install packages or link config files again if something goes wrong.

## Requirements

**IMPORTANT**: If you come from a fresh distro, you'll need to **update** (_e.g:_ `sudo apt update`,...) and **upgrade** (_e.g:_ `sudo apt upgrade`,...) all the packages first, then install requirements and follow the instruction below.

-   git.
-   bash shell.
-   [tput](https://command-not-found.com/tput).
-   _(Optional)_: Install these requirements if you want to get the best experience:
    -   Themes:
        -   Breeze Theme.
        -   Symphonic Theme.
        -   Brogrammer Theme.
        -   XTerm.
        -   Obsidian Theme.

## Installation

1. Clone the repository into `~/.dotfiles/`:

    ```shell
    git clone --depth=1 https://github.com/vuong-cuong-phoenix/dotfiles.git $HOME/.dotfiles
    cd $HOME/.dotfiles
    ```

2. Run this command:

    ```shell
    ./install.sh
    ```

-   The installation will backup config file if it is exists and is not linked to the correct place. All backup files are under `./BACKUP/<CURRENT DATE_TIME>/`.
-   If you haven't install `oh-my-zsh` before, then after the first time installation of it, you'll need to **run the command above again** to get effect of configurations.
-   Install any [Nerd Font](https://github.com/ryanoasis/nerd-fonts) and set it as default font for your Terminal.

## List of Packages and Configurations

-   **git**
    -   _~~.gitconfig.static: [~/.gitconfig.static](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/git/.gitconfig.static)~~ (Deprecated)_
    -   .gitignore_global: [~/.gitignore_global](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/git/.gitignore_global)
-   **curl**
-   **unzip**
-   **bash**
    -   .bash_profile: [~/.bash_profile](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/shell/.bash_profile)
    -   .bashrc: [~/.bashrc](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/shell/.bashrc)
-   **vim**
    -   .vimrc: [~/.vimrc](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/editor/.vimrc)
-   **zsh**
    -   .zprofile: [~/.zprofile](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/shell/.zprofile)
    -   .zshrc: [~/.zshrc](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/shell/.zshrc)
    -   **oh-my-zsh**: `~/.oh-my-zsh`
        -   zsh-autosuggestions: `~/.oh-my-zsh/custom/plugins/zsh-autosuggestions`
        -   zsh-syntax-highlighting: `~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting`
        -   powerlevel10k: `~/.oh-my-zsh/custom/themes/powerlevel10k`
    -   DIR_COLORS: [~/.dir_colors](https://github.com/vuong-cuong-phoenix/dotfiles/blob/master/shell/.dir_colors)

## Known Issues

-   **(Solved)** Cannot find **Hack Nerd Font** in **Gnome-Terminal**.  
    **==>** By default, **Gnome-Terminal** only shows _monospace-fonts_.  
    To choose **Hack Nerd Font** as the default font for **Gnome-Terminal**, you need to install `dconf-editor`, then open it, find `/org/gnome/terminal/legacy/profiles:/<profiles-id>/font` and then change **_Custom value_** to `<font-name> <font-size>` (_e.g:_ `Hack Nerd Font 14`)
