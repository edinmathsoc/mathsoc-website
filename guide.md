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
`git clone --recursive git@github.com:samuelwebb2/mathsoc-website.git`

You may have to install git your computer should prompt you if necessary.

## add ssh key to mathsoc website server (tardis)

Open a terminal window (You can do this inside Visual Studio Code or your terminal of choice)

Add your SSH key to the server by running the following command:

`ssh-copy-id mathsoc@tardisproject.uk`

You will be prompted for a password. Ask someone who already has access to it to share it with you. When you paste (or type) in the password to the terminal **nothing will show up don't worry it has still been typed in.**

On mac you will [install homebrew](https://brew.sh)

This will ask for your computers password

After the homebrew command has run don't forget to run the commands that it tells you to run in the terminal!

then install hugo with the command `brew install hugo`

On windows tbc

[Install npm/node.js](https://nodejs.org/en/download/package-manager)

download and install Node.js

`brew install node@20`
verifies the right Node.js version is in the environment
`node -v`
verifies the right npm version is in the environment
`npm -v`
should print `v20.18.0` this might be a higher number by the time you do this.

Now we will install blowfish-tools our theme manager using the following commands:
`npx blowfish-tools`

After install use the arrow keys to select Exit and press enter.

now we are going to make some aliases for some long commands you will use often.

`alias mathsoc-up="hugo && rsync -avz --delete public/ mathsoc@tardisproject.uk:~/www"`
