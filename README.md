# My MacOS configuration

## Setup

### In Order

1. Login App Store
1. Install `.ssh`
    Example:
    ```
    $ ssh -k ~/.ssh/id_rsa
    ```
1. Install CLT
    This installs Git
    ```
    $ xcode-select --install
    ```
1. Setup git
    ```
    $ git config --global user.name "wochap"
    $ git config --global user.email gean.marroquin@gmail.com
    ```
1. Setup MacOS global config
    ```
    $ git clone git@github.com:wochap/macos-config.git ~/macos-config
    $ sh ~/macos-config/.macos
    ```
1. Install Xcode
1. Install [Homebrew](https://brew.sh)
    ```
    $ cd ~/macos-config
    $ brew bundle
    ```
1. Install [nix](https://nixos.org/download.html)
1. Install [nix-darwin](https://github.com/LnL7/nix-darwin)
    Default `nix-darwin` config location: `~/.nixpkgs/darwin-configuration.nix`
    **IMPORTANT** run with `bash`.
    ```
    # Clone nix-config to ~/nix-config
    $ git clone git@github.com:wochap/nix-config.git ~/nix-config

    # Build
    $ darwin-rebuild switch -I darwin-config=/Users/gean/nix-config/devices/mbp-darwin.nix
    ```
    In case zsh gives logs
    ```
    $ compaudit | xargs chmod g-w,o-w
    ```

### Any Order

* Setup System Preferences > Internet Accounts
  - iCloud
  - Google
* Setup System Preferences > Mission Control
  - Automatically rearrange Spaces... (False)
  - Group windows by application... (True)
* Setup System Preferences >  Spotlight
* Setup Disable auto brightness
* Setup Night Shift
* Setup Battery GPU switching
* Setup Backgrounds

## Post setup

1. VSCode sync settings
1. Firefox sync settings
1. Chrome sync settings
