# Terminal Multiplexer Configuration

## Dependencies:

1. tmux
2. tmux plugin manager (_[github repo](https://github.com/tmux-plugins/tpm)_)
3. Font of your choice (_[Nerd fonts](https://www.nerdfonts.com/font-downloads)_)

## Installation:
1. Install tmux

    ```sh
    apt-get install tmux
    ```
2. Install tmux plugin manager

    ```sh
    git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
    ```
3. Copy the `.tmux.conf` file to your home directory

    ```sh
    cp .tmux.conf ~/.tmux.conf
    ```
4. Source the `.tmux.conf` file

    ```sh
    tmux source ~/.tmux.conf
    ```
5. Enter tmux and install the plugins

    a. Start a tmux session

    ```sh
    tmux new
    ```
    b. Install the plugins (use the following key combination)

    ```sh
    # Default prefix is Ctrl + b
    # This config uses Ctrl + Space as the prefix
    <prefix> + I
    ```
6. Copy the fonts to your home directory (if the fonts are not already installed)

    ```sh
    cp -r .fonts ~/
    ```
7. Update the font cache

    ```sh
    fc-cache -f -v
    ```
8. Set the bash font to the installed font (by the preferences menu)

## Key Bindings:

- Default prefix is `Ctrl + b`
- Custom prefix is `Ctrl + Space`

Read the default key bindings [here](https://tmuxcheatsheet.com/)

--------------------------------------------------------------------

#### **Based on**:
- _BashBunni tmux configuration ([bushbunni dotfiles](https://github.com/bashbunni/dotfiles))_
- _Hamvocke tmux configuration ([hamvocke dotfiles](https://github.com/hamvocke/dotfiles))_
