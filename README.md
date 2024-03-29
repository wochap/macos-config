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
    $ sh ~/macos-config/.macos.zsh
    ```
1. Install Xcode
1. Install [Homebrew](https://brew.sh)
    ```
    $ cd ~/macos-config
    $ brew bundle
    ```
1. [Disable SIP](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection)
1. [Install yabai](https://github.com/koekeishiya/yabai/wiki/Installing-yabai-(latest-release))
1. [Install skhd](https://github.com/koekeishiya/skhd)
1. Install [nix](https://nixos.org/download.html)
1. Install [nix-darwin](https://github.com/LnL7/nix-darwin)
    Default `nix-darwin` config location: `~/.nixpkgs/darwin-configuration.nix`
    **IMPORTANT** run with `bash`?.
    ```sh
    # Clone nix-config to ~/nix-config
    $ git clone git@github.com:wochap/nix-config.git ~/nix-config

    # Build (only first time)
    $ darwin-rebuild switch -I darwin-config=/Users/gean/nix-config/devices/mbp-darwin.nix

    # Build with flakes (only first time)
    $ nix build .#darwinConfigurations.mbp-darwin.system
    $ ./result/sw/bin/darwin-rebuild switch --flake .#mbp-darwin

    # After updating config
    $ darwin-rebuild switch --flake .#mbp-darwin
    ```
    In case zsh gives logs
    ```
    $ compaudit | xargs chmod g-w,o-w
1. [Enable SIP](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection) after darwin-build
    ```
1. Setup neovim
    ```sh
    # Clone git@github.com:wochap/nvim.git
    $ git clone git@github.com:wochap/nvim.git ~/.config/nvim
    ```
1. Setup NodeJS links
    ```
    $ ln -s $(which node) /usr/local/bin/node
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
* Setup keyboard
  > Shortcuts
  > Keyboard > Modifier Keys

## Post setup

1. VSCode sync settings
1. Firefox sync settings
1. Chrome sync settings

## Troubleshooting

* warning: Nix search path entry '/nix/var/nix/profiles/per-user/root/channels' does not exist

```
$ nix-channel --update
```

* [opening lock file Permission denied](https://forum.holochain.org/t/nix-shell-tips-opening-lock-file-permission-denied/5173)

```
$ sudo chown -R <username>:staff /nix
```

## Guides

```sh
# Start mongodb
$ brew services start mongodb/brew/mongodb-community
```

## Resources

* https://daiderd.com/nix-darwin/manual/index.html#sec-options