
## In Order

1. Install `.ssh`
1. Install CLT
    This install Git
    ```
    $ xcode-select --install
    ```
1. Setup git
    ```
    $ git config --global user.name "wochap"
    $ git config --global user.email gean.marroquin@gmail.com
    ```
1. Install Xcode
1. Install [Homebrew](https://brew.sh)

1. Install [nix](https://nixos.org/download.html)
1. Install [nix-darwin](https://github.com/LnL7/nix-darwin)
    Default config location: `~/.nixpkgs/darwin-configuration.nix`
    ```
    # Clone nix-config
    $ darwin-rebuild switch -I darwin-config=/Users/gean/nix-config/devices/mbp-darwin.nix
    ```
1. Install
    ```
    $ cd macos-config
    $ ./.macos
    $ brew bundle
    ```

## Any Order

* Setup System Preferences > Internet Accounts
  - iCloud
  - Google
* Setup System Preferences > Mission Control
  - Automatically rearrange Spaces... (False)
  - Group windows by application... (True)
* Setup System Preferences >  Spotlight
* Setup Night Shift
* Setup Battery GPU switching
* Setup Backgrounds

## Setup

1. VSCode sync settings
1. Firefox sync settings
1. Chrome sync settings
