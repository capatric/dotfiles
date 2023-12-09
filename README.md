# Patrick's Dotfiles

Managed with [chezmoi](https://www.chezmoi.io) ❤️

## Setup dotfiles on a new machine

  1. (Optional) Install [Bitwarden](https://bitwarden.com/) and login if you plan to install secrets.

     **Linux**
     ```
     sudo snap install bw
     bw login
     ```

  2. [Install chezmoi](https://www.chezmoi.io/docs/install/) to `~/bin` and
     install dotfiles to `~/dotfiles`.
     ```
     sh -c "$(curl -fsLS git.io/chezmoi)" -- -b "$HOME/bin" init --apply -S ~/dotfiles mkasberg
     ```

Done! To keep up to date in the future:

    chezmoi update

Want to check the diff before applying changes?

    chezmoi <update|apply> -nv

