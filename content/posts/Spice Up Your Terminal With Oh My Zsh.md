+++
title = 'Spice Up Your Terminal With Oh My Zsh'
date = 2024-04-14T13:02:04+10:00
draft = false
+++

> Oh My Zsh is an open-source, community-driven framework for managing your [zsh](https://www.zsh.org/) configuration. - Oh My ZSH Github

In this blog post, I will guide you to install Oh My Zsh on your computer. Oh My Zsh allows you to customize your terminal prompt.

## Pre-requisites:

- MacOS or Linux because Oh My Zsh works best on Unix-based systems (WSL will work)
- `curl` or `wget`

## Install zsh:

#### Ubuntu/Debian:

```shell
sudo apt install zsh
```

#### Fedora:

```shell
sudo yum install zsh
```

## Set zsh as default shell:

```shell
chsh -s /bin/zsh
```

> Note: For some systems, you need to log out and log in again to take effect.

## Install Oh My Zsh:

#### curl:

```shell
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

#### wget

```shell
wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh
```

## Selecting A Theme:

Robbyrussell is the default theme that comes with Oh My Zsh. To change the theme, you need to edit the `~/.zshrc` in your home directory. Here is the theme list: [Github](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

## Update Oh My Zsh:

Run `omz update` to update Oh My Zsh.

## For more information:

For more information, take a look at their Github page: [Github](https://github.com/ohmyzsh/ohmyzsh)

#### Thank you for reading!!

> This blog post is writtin by Eason Li and edited by Google Bard.
