# Azure Web App: Conda
Conda is my prefered python package and environment manager
- I prefer miniconda
  - It is a leightweight version of Anaconda
  - In the future, this document may go over installing and setting up miniconda on a Windows device

The setup we are doing here is for local development of the web app
- Azure will create the necessary python environment from the Requirements.txt file
- This is important to keep in mind as you can always remove your local environment and start over if needed
- I like to keep a log of everything I do to the environment for future reference, things I include
  - The commands I entered into the Conda prompt
  - Listing of all libraries installed, including version, and any oddoties like conda channels

## Environment Setup
Before proceeding, setup the GitHub repository first and clone that to your local machine (see GitHub documentation). I'll use "repository" to refer to this root folder.

Open a conda prompt

Browse (change directory) into the "repository" folder
- This will depend on your setup

`cd repository`

Create the environment

`conda create --prefix ./env python`
- --prefix tells conda to create the environment at a specific path
- ./env indicates the path should be in the current directory and we will name the folder (and environment) "env"
- python - go ahead and install python, we will need it!
  - You can include other packages like flask, I prefer to install those separately after creating the environment

Activate the environment

`conda activate ./env`
- This is the starting point for all other commands
- All subsequent commands below will assume you have activated the environment

## Installing libraries
Conda is a great package manager, however, it relies on the user community to keep packages up to date.
- I always check the corresponding pypi.org site to see what the latest version is of a package

## Requirements.txt
The Requirements.txt file is used by Azure and GitHub Actions to install the appropriate python libraries
- This file will need to be re-created anytime changes are made to the conda evironment
- Be sure to activate the environment first

```
pip list --format=freeze > requirements.txt
```
