# Zsh setup

## Dependencies:
- oh my zsh (_[oh my zsh](https://ohmyz.sh/)_)
- zsh-syntax-highlighting (_[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)_)
- zsh-autosuggestions (_[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)_)
- spaceship prompt (_[spaceship](https://github.com/spaceship-prompt/spaceship-prompt)_)

## Installation:

1. Install zsh

    ```sh
    sudo apt install zsh
    ```
2. Install oh my zsh

    ```sh
    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
3. Delete the default `.zshrc` and copy the `.zshrc` file to your home directory

    ```sh
    rm ~/.zshrc
    cp .zshrc ~/.zshrc
    ```
4. Create zsh allias file

    ```sh
    cp .zsh_aliases ~/.zsh_aliases
    ```
5. Install zsh-syntax-highlighting

    ```sh
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```
6. Install zsh-autosuggestion

    ```sh
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```
7. Install spaceship prompt

    ```sh
    # clone the repo to the Zsh custom theme directory
    git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
    # symlink it
    ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
    ```
8. Source the `.zshrc` file

    ```sh
    source ~/.zshrc
    ```


## Resources
- https://scottspence.com/posts/my-zsh-config
