# My Docker-VSCode Template for R (with Python, Julia, and LaTeX)

## Prerequisites (and for the first time to use this template)

- Install [Docker Desktop](https://www.docker.com/products/docker-desktop/). I strongly recommend using it on WSL2 (Windows Subsystem for Linux 2) if you are using Windows.
- Install [VSCode](https://code.visualstudio.com/) and [Remote-Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- Create [Docker volumes](https://docs.docker.com/storage/volumes/) by running
    ```{bash}
    docker volume create renv
    docker volume create pip
    docker volume createe julia
    docker volume create TinyTeX
    docker volume create fonts
    ```

## Quick Start
1. Clone this repository
1. Open it in VSCode and add Remote-Containers Extension
From the command palette (Ctrl+Shift+P), choose "open folder in container"
1. Open `localhost:8787` in a browser
1. Create a project for this project directory (by default, choose `/home/rstudio/work`)
1. RUN `renv::init()` in the R console
1. RUN `pip install dvc dvc-gdrive` for DVC install (if you have never used this template)
1. Set up a [DVC](https://dvc.org/) environment
    1. Prepare a folder in Google Drive (and copy the folder code)
    1. Init DVC
        ```{bash}
        dvc init
        dvc remote add --default myremote gdrive://GDRIVE_FOLDER_CODE
        ```
1. Set up LaTeX compiling recipe. Do the one of the following:
    - Rename `.vscode/_settings.json` into `.vscode/settings.json` (which is git-ignored)
    - Add the lines in `.vscode/_settings.json` into your `.vscode/settings.json`
1. Set up Julia environment
    1. Create an empty file `Project.toml` in the project root directory
    1. In Julia console, Run `] activate .` and `] instantiate`