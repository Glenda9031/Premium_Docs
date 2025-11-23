# What Is Git & Github

Now that we have a finished project, we need to learn how to manage and deploy it. We will talk about the different types of hosting services as well as domain names, but before we do that, I want to introduce you to Git and Github.

## What is Git?

Git is a version control system that allows you to manage and keep track of your code changes. It is a distributed version control system, which means that you can work on your code offline and then push your changes to a remote repository when you are ready. It is a powerful tool that allows you to collaborate with other developers, track changes, and revert to previous versions of your code. It is widely used in the software development industry and is an essential skill for any developer.

Git is used with some really complex projects, but you can still use it with a simple website build like this one. It is a great way to keep track of your code changes and collaborate with others. Also, there are web hosting services that allow you to deploy your website directly from a Git repository, which makes it easy to manage your code and deploy your website and make it live.

## What is Github?

Github is a web-based platform that allows you to host your Git repositories online. It is a social coding platform that allows you to collaborate with other developers, share your code, and contribute to other projects. It is widely used in the software development industry and is a great way to showcase your work and build your portfolio.

## Install Git

Before we can start using Git, we need to install it on our computer. You can download Git from the official website [here](https://git-scm.com/). If you are on a Mac, you can also install Git using Homebrew by running the following command in your terminal:

```bash
brew install git
```

If you are on Linux, you can use whatever package manager your distribution uses to install Git. For example, on Ubuntu, you can install Git by running the following command in your terminal:

```bash
sudo apt-get install git
```

To check if Git is installed, open your terminal and run the following command:

```bash
git --version
```

If Git is installed, you should see the version number displayed in your terminal.

## Configure Git

Once Git is installed, you need to configure it with your name and email address. This information will be used to identify you as the author of your code changes. You can configure Git with your name and email address by running the following commands in your terminal:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Replace your name and email address with your own information. This information will be stored in your Git configuration file, which is located in your home directory (`~/.gitconfig`).

## Create a Github Account

Now that you have Git installed and configured, you can create a Github account. Go to the [Github website](https://www.github.com) and sign up for a free account. Once you have created an account, you can start using Github to host your Git repositories online.

In the next lesson, we will create a new Git repository for our project and push our code to Github. We also need to generate a SSH key to authenticate with Github.
