<!--
SPDX-FileCopyrightText: 2024 Jason Pena <jasonpena@awkless.com>
SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Welcome to my Dotfile Collection

Hello, and welcome to my personal dotfile collection! Have a look around,
contribute, or take whatever you want. Just keep in mind that the configurations
stored in this organization are personalized. Thus, what might work for me may
not work for you.

# Simple Dotfile Manager in Rust

> Source code: <https://www.github.com/awkless-dotfiles/sdmr>

> Design documentation: <https://dotfiles.awkless.com/sdmr>

The sdmr project is a simple dotfile manager written in Rust. The application
uses Git as the primary version control system to manage and organize the user's
dotfiles. The idea is to treat the user’s $HOME directory as a Git repository
such that their $HOME is considered the working tree, and some external
directory (typically $HOME/.local/share/dotfiles) acts as a bare repository to
keep track of the history.

A special feature of this dotfile manager is its use of Git's [sparse checkout
feature][sparse-checkout] to deploy or undeploy collections of dotfiles at once.
Thus, the user does not need to rely on symlinks or copies of their dofiles into
their `$HOME` directory. Give it a try!

[sparse-checkout]: https://git-scm.com/docs/git-sparse-checkout
