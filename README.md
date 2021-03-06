## About

These are misc scripts and configuration files I use on my machine. Not
guaranteed to be portable but go nuts if you find anything useful. Copyright is
not always well documented and I don't guarantee that any code without explicit
copyright is not somehow copyright or patent encumbered.

Feel free to contact me if you want clearer copyright information on any
particular bit.

Most ~/bin/ stuff *should* be path agnostic, but the bashrc assumes ~/bin
exists. Various mozilla-related scripts assume ~/moz/ and ~/moz/moz-git/

## Symlinks on my systems:
        # Scripts/bash
        ln -sv $repo/bin            ~/bin
        ln -sv $repo/bashrc         ~/.bashrc
        ln -sv $repo/bash_profile   ~/.bash_profile

        # Emacs (Make sure you submodule init && update)
        ln -sv $repo/emacs          ~/.emacs
        ln -sv $repo/emacs.d        ~/.emacs.d

        # Git
        ln -sv $repo/gitconfig      ~/.gitconfig
        ln -sv $repo/gitignore      ~/.gitignore

        # Mercurial
        ln -sv $repo/hgrc           ~/.hgrc
        ln -sv $repo/hgignore       ~/.hgignore

## Other
        # tmux-powerline
        cp -v $repo/DejaVuSansMono-Powerline.ttf ~/.fonts/
        fc-cache -vf

        # ssh (does not want this file symlinked/insecure)
        cp -v $repo/sshconfig ~/.ssh/config
        chown -v $USER ~/.ssh/config
        chmod -v 600 ~/.ssh/config

## Various mozilla things assume:

- ~/moz/mozilla-central and other mozilla-* things are mozilla mercurial repos
- ~/moz/moz-git and ~/moz/moz-git-map are mozilla-git and hg-git-mapfile repos
  (for ghg/ghup/gmq/etc hg<->git scripts)
  - See:
    - https://github.com/Nephyrin/mozilla-git
    - https://github.com/Nephyrin/mozilla-git-hg-mapfile
- ~/moz/cfg is symlinked to $repo/moz/cfg

## Contact
- john@pointysoftware.net
