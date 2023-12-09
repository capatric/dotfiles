# Patrick's Dotfiles

When working with various terminals and machines, we often find ourselves longing for the setup we had before. However, reconfiguring all the dotfiles to recreate the previous environment can be a tedious task, not to mention the time spent researching the optimal configurations to make the terminal look appealing.

[Chezmoi](https://www.chezmoi.io) offers a solution to this problem by helping us manage our personal configuration files across multiple machines securely. With Chezmoi, all we need to do is install it on our new machine. Then, with just a single command, all our configuration files are enabled, allowing the terminal to look and function as beautifully as our favorite one.

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

