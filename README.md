# how to set up mathsoc website

## Install an editor if you haven't already

Install an editor of your choice, I recommend Visual Studio Code. [link](https://code.visualstudio.com/Download)

Open the editor, click open folder, and navigate to the folder where you will store the mathsoc website files. For example Documents. Open a terminal in VS Code (CMD + J on mac).

## Add ssh key to github

1. If you don't have an ssh key on your local machine, you can generate one by following the instructions on the GitHub website. [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
   1. You can check by typing the comand `ls -al ~/.ssh` if you get a response saying no known files then you will have to make one with the link above.

2. If you haven't already, you will need to add your SSH key to your GitHub account. You can do this by following the instructions on the GitHub website. 
[link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## add repository to your local machine

Request access to the MathSoc website repository on GitHub from a member of exec (or old exec). You will need a GitHub account to do this. 
Once you have access, you can clone the repository to your local machine. Use the command: 
`git clone git@github.com:samuelwebb2/mathsoc-website.git`

You may have to install git your computer should prompt you if necessary.

## add ssh key to mathsoc website server (tardis)

Open a terminal window (You can do this inside Visual Studio Code or your terminal of choice) and ssh into the server using the following command:

```ssh mathsoc@tardisproject.uk```

You will be prompted to add a fingerprint to your known hosts. Type yes and press enter.

You will then be prompted for a password. This is the password for the mathsoc account on the server. If you don't have this, ask someone who does. Note that the password will not show up as you type it as it is hidden for security reasons.

Once you have successfully logged in, you can add your SSH key to the server by running the following command:

```ssh-copy-id mathsoc@tardisproject.uk```



