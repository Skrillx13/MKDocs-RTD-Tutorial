# Create A Project

## Commands to run

Open up the terminal in your text editor. From there, type:

    mkdocs new .

This generates the config files and docs folder for your project. Afterwrads type:

    mkdocs serve

This makes your MKDocs project serve on a Local Host project at http://127.0.0.1:8000. Open it up in your browser. Now everytime you edit a file in your project and save, your local host build will follow, meaning you can see your changes live. You now have a basic MKDocs project set-up.

## Configuration

First, you want to edit the mkdocs.yml folder ```mkdocs.yml```, and change the site name to whatever you wish. Next, we can install a theme onto MKDocs. This project currently has the [ReadTheDocs](https://sphinx-rtd-theme.readthedocs.io/en/stable/) theme in use, but another good one is [Material for MKDocs](https://squidfunk.github.io/mkdocs-material/).

From there, we can start adding more configuration.

### Linking a GitHub repository

Adding the following code to ```mkdocs.yml``` will allow us to link a GitHub repository to this Documentation. It will generate as a text saying "Edit on GitHub", and when clicked will bring users to the GitHub repository that you linked.

    repo_name: GitHub
    repo_url: https://github.com/Skrillx13/MKDocs-RTD-Tutorial

Be sure to replace the ```repo_url``` with the repository link of your choice.

!!! tip

    You can look at other MKDocs projects to get inspiration for configuration. Don't steal code though!

