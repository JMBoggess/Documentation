# GitHub
GitHub can be used for source code control and automatic deployment to an Azure Web App

## Setup the Repository
Create a repository in GitHub
- I set mine as private so I do not have to worry about inadvertantly posting any secrets, keys, etc.
- Add a Readme.md file
  - I find this useful to make notes to myself or keep configuration information handy

## Clone the repository
I prefer to use GitHub desktop, it is possible to integrate git into Visual Studio Code (VSCode):
- Pros
  - You can then push changes directly to GitHub (and therefore to your Azure Web app) automatically
  - Essentially, it is convenient
- Cons
  - Git for Windows comes with a lot of baggage
  - There is a learning curve to using git

In GitHub desktop, clone the newly created repository

## Create .gitignore
This file will tell GitHub what not to sync between your local client and GitHub.com
- This can be used to prevent files with secrets, etc. (like config files) from being exposed on public repositories
- I primarily use it to prevent syncing the python/conda environment from my local computer
  - The environment can be recreated (see Requirements.txt) in the event my local computer crashes
  - The environment isn't copied to the web site, it is essentially built from the Requirements.txt file in Azure

Example contents:

```
# Conda Environment
env/

# Debugging
__pycache__/

# Archived Code
archive/
```
