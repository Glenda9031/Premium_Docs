# Generate SSH Key

In the last lesson, we talked about Git and Github. In order to easily push our code to Github, we need to generate a SSH key to authenticate with Github. In this lesson, we will learn how to generate a SSH key and add it to our Github account.

## What is SSH?

SSH (Secure Shell) is a cryptographic network protocol that allows you to securely connect to a remote server over an unsecured network. It is widely used in the software development industry to securely transfer files and execute commands on remote servers. It is a secure alternative to traditional methods of connecting to remote servers, such as telnet and FTP.

## Generate SSH Key

To generate a SSH key, open your terminal and run the following command:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

This command will generate a new SSH key. The -t is for the type of key, and in this case we are using the Ed2559 algorithm, which is more secure than the traditional RSA algorithm. The -C is to specify a comment and we are adding our email address.

When you run this command, you will be prompted to enter a file in which to save the key. Press `Enter` to save the key in the default location (`~/.ssh/id_ed25519`). You will also be prompted to enter a passphrase to secure the key. You can enter a passphrase or leave it blank if you don't want to use one.

Once the key is generated, you will see a message that the key has been saved to the specified file. You can now add the key to your SSH agent by running the following

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

This will add the key to your SSH agent, which will securely store the key and use it to authenticate with remote servers.

## Add SSH Key to Github

Now that you have generated a SSH key, you need to add it to your Github account. To do this, you need to copy the contents of the public key file (`~/.ssh/id_ed25519.pub`) and add it to your Github account.

There are a few ways to get the content of the public key file. You can use the `cat` command to display the contents of the file in your terminal:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the contents of the file and go to your Github account. Click on your profile icon in the top right corner and select `Settings`. In the left sidebar, click on `SSH and GPG keys`. Click on `New SSH key` and paste the contents of the public key file into the `Key` field. Give the key a descriptive title and click `Add SSH key`.

Your SSH key is now added to your Github account, and you can use it to authenticate with Github when pushing your code.

You never have to do this again unless you need to generate a new key for a new computer or user. You can now push your code to Github using the SSH key you just generated.
