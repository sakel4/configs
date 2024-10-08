# Zsh setup

## Dependencies:
- oh my zsh (_[oh my zsh](https://ohmyz.sh/)_)
- zsh-syntax-highlighting (_[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)_)
- zsh-autosuggestions (_[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)_)
- powerlevel10k (_[poerlevel10k](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#installation)_)

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
    # for powerlevel10k
    cp .zshrc_powerlevel10k ~/.zshrc
    # for starship
    cp .zshrc_starship ~/.zshrc
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
7. Install fonts (after that you need to change the terminal font to the recomended font)

      ```sh
        # for Powerlevel10k
        cp -r fonts_powerlevel10k/* ~/.local/share/fonts
        # for Starship
        cp -r fonts_starship/* ~/.local/share/fonts
        ```
8. Install Theme

    ```sh
    # Install Powerlevel10k
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    # Install Starship
    curl -sS https://starship.rs/install.sh | sh
    ```
9. Starship configuration (skip to step 10 if you chose powerlevel10k)

    ```sh
    mkdir -p ~/.config && cp .starship.toml ~/.config/starship.toml
    ```

10. Source the `.zshrc` file

    ```sh
    source ~/.zshrc
    ```


## Resources
- https://scottspence.com/posts/my-zsh-config
