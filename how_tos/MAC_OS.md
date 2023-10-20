# MAC OS Setup

* [Terminal set-up](https://github.com/hadri96/Github_setup/blob/main/how_tos/MAC_OS.md#terminal-set-up)
* [Using GitHub](https://github.com/hadri96/Github_setup/blob/main/how_tos/MAC_OS.md#github-setup)
	* [Repository creation](https://github.com/hadri96/Github_setup/blob/main/how_tos/MAC_OS.md#creating-a-repository)


## Terminal set-up

As MAC OS users, you already have most of what's needed to work with GitHub.

However, we do need to install a couple more things and to do that we need Homebrew.

**Homebrew🍺** is a popular package manager for macOS and Linux that allows users to easily install and manage software packages and libraries from the command line. It simplifies the process of downloading, updating, and maintaining various software tools and utilities on a computer. If you want to understand more about it, feel free to visit their [website](https://brew.sh/).

To install Homebrew, run the following command on your Terminal (copy-paste and press enter):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once the installation is done (it might take a couple of minutes), you will have to install a couple of packages to set up GitHub. The way Homebrew works is fairly similar to pip in Python, to install a package all you need to do is:

```bash
brew install [package_name]
```

So we are going to install three packages:
* git (version control system)
* gh (GitHub)
* openssh (a connectivity tool for remote logins)

Install them running the following command:

```bash
brew install git && brew upgrade git &&
brew install gh && brew upgrade gh &&
brew install openssh && brew upgrade openssh
```

Once you are done we are now ready to start setting up your GitHub access!🎉

## Oh My Zsh (optional)

Before we move on to set up GitHub, we are also going to install Oh My Zsh on your machine. Oh My Zsh is a popular open-source framework that makes your command line on a computer more user-friendly and customizable by adding cool features and designs. It's like giving your computer's "talking" part a makeover.

To install it, please enter the following command on your Terminal:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

This will allow for a significant boost in productivity when working on the Terminal (I'll show a couple of useful ones in class) and if you want to know more about Oh My Zsh features, feel free to visit their [website](https://ohmyz.sh/)

## Github setup

The first obvious step will be to create your own GitHub profile, you can register [there](https://github.com/signup?).

Once you are done with that, we are going to have to follow the steps on this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to create and link your machine with your Github account.

This part might be a bit more challenging which is why we will complete it in class.

Once this step is complete, you will need to then authenticate by entering the command:

```bash
gh auth login
```
During this process, it will ask you how you want to authenticate, **please make sure to select the SSH option**

## Using Github

### Creating a Repository

To create a repository on GitHub: we will use the following command:

```bash
gh repo create
```
This will prompt a series of questions:

1. You will need to choose how to create your repository

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/create_from_scratch.png?raw=true)

	The options are the following:

	* **Create a new repository on GitHub from scratch**

		You should select that option if you just started the project (for this how_to, we will use this as an example)
	* **Create a new repository on GitHub from a template repository**

		You should select that option if you want to use a template repo from GitHub (rarely used)
	* **Push an existing local repository to GitHub**

		You should select that option if you would like to upload an existing folder containing files.

2. In this step, you will have to enter several informations about your repository such as the name of the repo, the owner of the repository (can be you or one of the organizations you are a part of and finally a small description of what this project is about)

![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/repo_info.png?raw=true)

3. For this step, the visibility of your project

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/visibility.png?raw=true)

	GitHub offers three visibility options for repositories:

	**Public**: Public repositories are visible to anyone on the internet. Anyone can view, clone, and contribute to public repositories. This is ideal for open-source projects where you want to encourage collaboration and contributions from the community. **It is the default option for repositories on Github.**

	**Private**: Private repositories are only visible and accessible to users who have been granted permission by the repository owner. You can control who can read, write, or manage the repository. This is useful for projects that require confidentiality or are not ready for public access. **<font color='red'>These repositories are limited to 3 collaborators</font>** if you have Github free.

	**Internal**: Internal repositories are a feature of GitHub Enterprise, and they are visible and accessible only to members of your organization. This option is suitable for companies and organizations that want to keep their code within their own network but still benefit from GitHub's collaboration features.

4. In this step, you will decide whether to create a README file

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/readme.png?raw=true)

	A README.md file is a text document typically written in **Markdown** format. Markdown is a lightweight markup language that allows you to **format text using plain text conventions**, making it easy to read and write. To create a README.md file, you can use any text editor or code editor, such as Notepad, Visual Studio Code, or even a simple text editor like Notepad. You write the content of the README.md file using Markdown syntax to format text, create headings, lists, links, and more. Once you've written the README.md file, you can include it in your GitHub repository, and it will be automatically rendered with formatting when viewed on the GitHub website. This helps provide clear documentation and information about your project for users and contributors.

	Generally, it is good practice to have a README as it allows others to understand what your project is about so it is highly encouraged to have one.

5. In this step, you will have to decide whether to have a .gitignore file

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/gitignore.png?raw=true)

	A .gitignore file is **a configuration file used in Git repositories to specify which files and directories should be ignored by Git when tracking changes in your project**. It allows you to exclude certain files or patterns from being included in version control. This is especially useful for preventing sensitive or generated files, temporary files, build artifacts, and other non-essential files from cluttering your Git history and repository.

	When you create a .gitignore file in your Git repository, **you list the names of files, directories, or patterns that you want Git to ignore**. Git will then exclude these specified files from being staged, committed, or tracked as part of your project. This helps keep your repository clean, reduces its size, and ensures that only relevant and necessary files are managed by Git, making it easier to collaborate with others and share your code without including files that should remain private or unnecessary in the repository.

	GitHub has prefilled gitignore files for every programming language so you can use them. In case you say no, you will also be able to create it on your laptop directly.

6. In this step, you have the choice to add a license to your project

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/license.png?raw=true)

	When you create a GitHub repository, GitHub will ask whether you want to include a software license with your project. A software license defines the terms and conditions under which others can use, modify, and distribute your code. Here's what different options imply:

	* **No License**

		If you choose not to add a license, your project will still be publicly accessible on GitHub, but it will have no explicit licensing terms. This means others can view your code, but they won't have clear permissions to use, modify, or distribute it. It's not recommended for open-source projects because it can create ambiguity around how others can use your code.

	* **Add a License**

		If you choose to add a license, GitHub provides several popular open-source licenses to choose from, such as the MIT License, Apache License, GNU General Public License, and more. By selecting a license, you're specifying the terms under which others can use your code. It's important to choose a license that aligns with your project's goals, such as permissive licenses that allow broader use or copyleft licenses that enforce sharing improvements.

	Adding a license is a good practice, especially if you want to encourage collaboration, contributions, or distribution of your project. It helps clarify the legal and ethical expectations for users and contributors and contributes to the openness and sustainability of open-source software.

7. At this stage you are almost done, GitHub is just asking you for the final green light before creating the repository

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/confirmation.png?raw=true)

8. Before wrapping up, GitHub will just ask you whether you want to clone your repo on your local machine

	![screenshot](https://github.com/hadri96/Github_setup/blob/main/screenshots/clone.png?raw=true)


Congratulations, you just created your first GitHub repository 🎉😎
