# Installation

## Requirements

Ensure you have the following mentioned below to start installing MKDocs:

- The Phyton Manager, [Pip](https://www.python.org/downloads/)
- You can run GitHub commands from your command line
- You can get access to your reposiutories SSH Key
- You have a text editor, prefebly [Visual Studio Code](https://code.visualstudio.com).

!!! note

    Pip is automatically installed with Phyton, so I recommend just downloading Phyton onto your computer.

## GitHub repository

First, make a GitHub repository. Name it something appropiate. For the settings, you will want to set the .gitignore template to Phyton. Choose a license of your choice, and enable the project with a README.md, and create.

Next, click on the "Code" button on your GitHub repository, and select SSH. Copy the SSH key. Then, open up your command line (Termianl if you are using Apple Silicon), and type:

    git clone (Paste SSH key here)

# Command Line

After completing the follwing step, type the following code into the command line:

    phyton -m venv venv

This command creates a phyton virtual enviroment, which is what allows us to view documentation and any edits made live. Next enter this code:

    source venv/bin/activate

Finally, install MKDocs using:

    pip install mkdocs

And then type: 

    code .

To open up Visual Studio Code

!!! tip

    If you are using a different text editor than Visual Studio, find out which command opens up the app from the Command Line, as "code ." may not work for all text editors.

You have successfully installed MKDocs, and are now ready to start editing.