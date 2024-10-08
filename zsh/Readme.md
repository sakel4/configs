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
7. Install Powerlevel10k recomended fonts (after that you need to change the terminal font to the recomended font)

      ```sh
        cp -r fonts/* ~/.local/share/fonts
        ```
8. Install Powerlevel10k

    ```sh
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    ```
8. Source the `.zshrc` file

    ```sh
    source ~/.zshrc
    ```


## Resources
- https://scottspence.com/posts/my-zsh-config
