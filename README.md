# README

This repo collects scripts and notes I find useful for my linux systems.

Assuming that the scripts repo is located in $HOME/scripts, do the following.

## git
When git has not yet been configured at all, first set your name and e-mail
to work with your repo:
```bash
git config --global user. email "you@example.com"
git config --global user.name "Your Name"
```

The above creates a file `$HOME/.gitconfig` containing: 
```bash
[user]
    name = Your Name
    email = you@example.com
```

As you probably don't want to have your name and e-mail in plain text in the
repo, or you have different names/e-mails on different machines, make name and
e-mail local by moving `$HOME/.gitconfig` to `$HOME/.gitconfig.local`:
```bash
mv ~/.gitconfig ~/.gitconfig.local
```

Finally, soft link the gitconfig file:
```bash
ln -s ~/scripts/scripts/git/gitconfig ~/.gitconfig
```

## bash
The scripts repo collects additions to `$HOME/.bashrc` in a separate file.
Source it in `.bashrc` by:
```bash
echo -e "\n# Add my own additions\nsource $HOME/scripts/scripts/bash/bashrc_additions"
```

## vim
Settings for vim are stored in the repo as well and can be soft linked in the
same way:
```bash
ln -s ~/scripts/scripts/vim/vimrc ~/.vimrc
```
