# Deploying to ReadTheDocs

## File Overview

Deploying to ReadTheDocs requires several files to be present in the directory. By the end, your file directory should look something like this (Example below is intended for Visual Studio Code):

```text
docs/
.gitignore
.readthedocs.yml
LICENSE
lumache.py
mkdocs.yml
pyproject.toml
README.md
    ...
```

### docs/

This the the documentation folder. It is where you place your markdown files in, and the content of your documentation.

### .gitignore

The Phyton ```.gitignore``` template.

### .mkdocs.yml

This is the configuration file that RTD uses. Simply create a file at the root of the directory, and name it ```.mkdocs.yml```.There is an optimized builder for MKDocs, which is recommended to be installed:

    # Read the Docs configuration file for MkDocs projects
    # See https://docs.readthedocs.io/en/stable/config-file/v2.html for details

    # Required
    version: 2

    # Set the version of Python and other tools you might need
    build:
    os: ubuntu-22.04
    tools:
        python: "3.12"

    mkdocs:
        configuration: mkdocs.yml

    # Optionally declare the Python requirements required to build your docs
    python:
    install:
    - requirements: docs/requirements.txt

### LICENSE

Your License file that you chose upon the Project Creation.

### lumache.py

When I deleted this file, the ReadTheDocs build crashes, do please dont delete it. Source code is too long to paste here, [please click me](https://github.com/readthedocs-examples/example-mkdocs-basic/blob/main/lumache.py) to get access to the whole code.

### mkdocs.yml

The default MKDocs configuration file. All configs go here.

### pyproject.toml

Insert the following code:

    [build-system]
    requires = ["flit_core >=3.2,<4"]
    build-backend = "flit_core.buildapi"

    [project]
    name = "lumache"
    authors = [{name = "Graziella", email = "graziella@lumache"}]
    dynamic = ["version", "description"]

### README.md

Project description you may add a brief overview of your project here.

## Deploying

After ensuring you have all the necessary files installed, you can deploy to RTD. First, you need to commit your changes.

Open up your terminal in your text editor, and ensure the terminal is on zhs. Enter ```git add .```, followed by:

    git commit -m $'Insert appropiate commit message'

And finally, enter ```git push origin main``` to send the changes to the GitHub repository.

Navigate to the RTD Project Dashboard, and select the option to add a Project. Choose the appropiate GitHub repository, and enter your desired configurations. From there, your project should be building. Click the "View Docs" option, and you should be able to see your docs live.