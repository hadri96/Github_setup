# MAC OS Setup

## Terminal set-up

As MAC OS users, you already have most of what's needed to work with Github.

However, we do need to install a couple more things and to do that we need Homebrew.

**Homebrew🍺** is a popular package manager for macOS and Linux that allows users to easily install and manage software packages and libraries from the command line. It simplifies the process of downloading, updating, and maintaining various software tools and utilities on a computer. If you want to understand more about it, feel free to visit their [website](https://brew.sh/).

To install Homebrew, run the following command on your Terminal (copy-paste and press enter):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once the installation is done (it might take a couple of minutes), you will have to install a couple of packages to set up Github. The way Homebrew works is fairly similar to pip in Python, to install a package all you need to do is:

```bash
brew install [package_name]
```

So we are going to install three packages:
* git (version control system)
* gh (Github)
* openssh (a connectivity tool for remote logins)

Install them running the following command:

```bash
brew install git && brew upgrade git &&
brew install gh && brew upgrade gh &&
brew install openssh && brew upgrade openssh
```

### Oh My Zsh

Before we move on to set up Github, we are also going to install Oh My Zsh on your machine. Oh My Zsh is a popular open-source framework that makes your command line on a computer more user-friendly and customizable by adding cool features and designs. It's like giving your computer's "talking" part a makeover.

To install it, please enter the following command on your Terminal:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

This will allow for a significant boost in productivity when working on the Terminal (I'll show a couple of useful ones in class) and if you want to know more about Oh My Zsh features, feel free to visit their [website](https://ohmyz.sh/)

Once you are done we are now ready to start creating your Github profile!🎉

## Github setup

The first obvious step will be to create your own Github profile, you can register [there](https://github.com/signup?).

Once you are done with that, we are going to have to follow the steps on this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to create and link your machine with your Github account.

This part might be a bit more challenging which is why we will complete it in class.



