# Create a Repo & Push To Github

In the last lesson, we learned how to generate a SSH key to authenticate with Github. In this lesson, we will create a new Git repository for our project and push our code to Github.

## Create a New Git Repository

To create a new Git repository, open your terminal and navigate to the root directory of your project. Run the following command to initialize a new Git repository:

```bash
git init
```

This command will create a new Git repository in the current directory. You will see a message that Git has initialized an empty repository in the specified directory.

## Add Files to the Repository

Now that we have initialized a new Git repository, we need to add our project files to the repository. VS Code does have GUI tools to do this, but you should know the commands anyway, so we will use the terminal.

Run the following command to add all files in the current directory to the repository:

```bash
git add .
```

This command will add all files in the current directory to the staging area. You can also add individual files by specifying the file name instead of `.`.

## Commit Changes

Once we have added our project files to the staging area, we need to commit the changes to the repository. Run the following command to commit the changes:

```bash
git commit -m "Initial commit"
```

This command will commit the changes to the repository with the message "Initial commit". You should replace this message with a descriptive message that explains the changes you are committing.

## Create a New Repository on Github

Now that we have committed our changes to the local repository, we need to create a new repository on Github to push our code to. Go to the [Github website](https://www.github.com) and sign in to your account. Click on the `+` icon in the top right corner and select `New repository`.

Fill in the repository name, description, and other settings, and click `Create repository`. You will see a message that the repository has been created.

## Push Code to Github

Now that we have created a new repository on Github, we need to push our code to the remote repository. Run the following command to add the remote repository URL to your local repository:

```bash
git remote add origin [repository-url]
```

Replace `[repository-url]` with the URL of your GitHub repository.

Finally, push the files to GitHub:

```bash
git push -u origin main
```

This command will push your code to the remote repository on Github. You will be prompted to enter your Github username and password. Once the code is pushed, you will see a message that the code has been pushed to the remote repository.

Now if you look at the repo page, you should see your code.
