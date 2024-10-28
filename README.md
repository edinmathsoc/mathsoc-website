# University of Edinburgh MathSoc Website

Welcome to the official repository for the University of Edinburgh MathSoc website.

## Table of Contents

- [About](#about)
- [Installation](#installation)
- [Usage](#usage)
- [Uploading changes](#uploading-changes-members-of-the-mathsoc-exec-team-only)
<!-- - [Contributing](#contributing) -->
<!-- - [License](#license) -->

## About

This repository contains the source code for the University of Edinburgh MathSoc website. The website provides information about events, membership, and resources for students interested in mathematics.

## Installation

To set up the project locally, follow these steps: (Work in progress currently only works on MacOS and Linux)

1. Clone the repository:

    In a terminal window, run the following command:

    ```bash
    git clone --recursive git@github.com:samuelwebb2/mathsoc-website.git
    ```

    In order to complete this step you may need to setup the following if you haven't already:
    1. [Install an editor](https://code.visualstudio.com/Download)
    2. [Add ssh key to github](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

2. Navigate to the project directory and open it in your editor:

    ```bash
    cd mathsoc-website
    code .
    ```

3. Install the dependencies:

    If you don't have homebrew installed follow the instructions [here](https://brew.sh).

    ```bash
    brew install hugo node@20
    ```

    ```bash
    npm i -g blowfish-tools
    ```

## Usage

To start the development server, run:

```bash
blowfish-tools
```

Using your arrow keys sellect the option: 'Run a local server with Blowfish', and press enter.

Open your browser and navigate to [http://localhost:1313](http://localhost:1313) to view the website.

## Uploading changes (Members of the MathSoc exec team only)

If you are not a member of the MathSoc exec team, you will need to create a pull request to merge your changes into the main branch.

1. Pull the latest changes from the repository:

    ```bash
    git pull
    ```

2. Make your changes to the website.

    e.g. Add a new page to the website by using the following commands:

    ```bash
    blowfish-tools
    ```

    Using your arrow keys sellect the option: 'Generate a new article', and press enter.

    Follow the prompts to create a new page. Edit the page content in the `content` directory.

3. Add your changes to the staging area:

    ```bash
    git add .
    ```

4. Commit your changes:

    ```bash
    git commit -m "Your commit message here"
    ```

5. Push your changes to the repository:

    ```bash
    git push
    ```

6. Publish your changes to the live website:

    If you are a member of the MathSoc exec team, you can publish your changes to the live website by running the following command:

    ```bash
    hugo && rsync -avz --delete public/ mathsoc@tardisproject.uk:~/www
    ```

<!-- ## Contributing
We welcome contributions! Please read our [contributing guidelines](CONTRIBUTING.md) to get started. -->

<!-- ## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. -->