# NBA Data Dash
Powered by [reflex.dev](https://reflex.dev/) 



## Data Source

- https://github.com/NocturneBear/NBA-Data-2010-2024



## Tech Stack

- Python 3.12
- Reflex 0.5.5+, currently 0.6.4
- Pandas

    BTW - I am on Ubuntu 24.04.



## Getting Started

1. Basic setup
    ```shell
    ## Update and Upgrade
    sudo apt update && sudo apt upgrade -y
    ## Install the virtualenv tool and unzip
    sudo apt install python3.12-venv unzip
    
    ## Install the `bun` package manager for later use with Reflex
    ## If you have Node.js v20+ installed, this is not neccessary!
    curl -fsSL https://bun.sh/install | bash
    ## activate the .bashrc to make sure `bun` is accessible
    source ~/.bashrc
    ```
2. Create venv and give a go
    ```shell
    ## Make project directory
    mkdir reflex-nba-dash
    cd reflex-nba-dash
    ## create a venv named as '.venv'
    python3 -m venv .venv
    ## activate it
    source .venv/bin/activate
    ## list the modules in the .venv (only 'pip' itself)
    pip list
    ## Optuioally upgrade pip
    pip install --upgrade pip
    
    ## Ensure the python3 and pip are from the .venv, 
    ## if output is like "/usr/bin/", then remake the .venv
    which python3
    which pip
    ```
    Note: <font color="red">The ops below are in the Virtual Environment.</font>
    
3. Install the monster - Reflex
    ```shell
    ## This takes quite a while as many modules pop in
    pip install reflex==0.6.4
    ## check them out
    pip list
    ```
4. Give a go
    ```shell
    reflex init --template nba_dash
    ```
    It will prompt you some templates to select with, choose the one represents 'NBA'. 

    And the process will generate quite a few files in the project folder.
5. Install some extra python modules: pandas, numpy, etc. (please do)
    ```shell
    ## edit requirements.txt file ensuring the version of reflex == 0.6.4 (>=0.5.5)
    ## because the latest version 0.6.5 is very buggy as of November 12, 2024.
    pip install -r requirements.txt
    ```
6. Start up the Reflex App
    ```shell
    reflex run
    ## In macOS, It may complain no permission to run/install ...bun_install.sh 
    ## (it's actually installed previously), you have to use
    ## sudo reflex run
    ```
    Eventually, you will be presented with:
    
    > App running at: http://localhost:3000 
    >
    > Backend running at: http://0.0.0.0:8000
7. Enjoy the show.



## Push the Project to GitHub

1. Create a empty repository on your GitHub space, named as, say `nba-data-dash`.

2. Edit the `.gitignore` file to exclude the `venv` folder.

3. Commit and Push to the repo:

   ```shell
   ## Add data files in
   git add .
   ## Commit
   git commit -m "nba-data"
   ## channel it to master - sorry not a fan of main
   git branch -M master
   ## conenct to remote repo
   git remote add origin https://github.com/marcuszou/nba-data-dash.git
   ## Push the project files
   git push -u origin master
   ```

   

## License
MIT
    

