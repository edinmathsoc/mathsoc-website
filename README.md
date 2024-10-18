# how to set up mathsoc website

## add repository to your local machine

Request access to the MathSoc website repository on GitHub. You will need a GitHub account to do this. Once you have access, you can clone the repository to your local machine, use SSH.

install an editor of your choice, I recommend Visual Studio Code. [link](https://code.visualstudio.com/Download)

## add ssh key to github

If you don't have an ssh key on your local machine, you can generate one by following the instructions on the GitHub website. [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

If you haven't already, you will need to add your SSH key to your GitHub account. You can do this by following the instructions on the GitHub website. 
[link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## add ssh key to mathsoc website server (tardis)

Open a terminal window (You can do this inside Visual Studio Code or your terminal of choice) and ssh into the server using the following command:

```ssh mathsoc@tardisproject.uk```

You will be prompted to add a fingerprint to your known hosts. Type yes and press enter.

You will then be prompted for a password. This is the password for the mathsoc account on the server. If you don't have this, ask someone who does. Note that the password will not show up as you type it as it is hidden for security reasons.

Once you have successfully logged in, you can add your SSH key to the server by running the following command:

```ssh-copy-id mathsoc@tardisproject.uk```



