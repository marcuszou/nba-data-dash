# NBA Data 2015-2016 Dash



## Data Source

- https://github.com/NocturneBear/NBA-Data-2010-2024



## Tech Stack

- Python 3.12
- Reflex 0.5.3+, currently 0.6.4
- Pandas

    BTW - I am on Ubuntu 24.04.



## Getting Started

1. Basic setup
    ```shell
    ## Update and Upgrade
    sudo apt update && sudo apt upgrade -y
    ## Install the virtualenv tool and unzip
    sudo apt install python3.12-venv unzip
    ## Install the `bun` module for later use with Reflex
    curl -fsSL https://bun.sh/install | bash
    ```
2. Create venv and give a go
    ```shell
    ## Make project directory
    mkdir nba-data-dash
    cd nba-data-dash
    ## create a venv named as 'venv'
    python3 -m venv venv
    ## activate it
    source venv/bin/activate
    ## list the modules in the venv (only 'pip' itself)
    pip list
    ```
    Note: <font color="red">The ops below are in the Virtual Environment.</font>

3. Install the monster - Reflex
    ```shell
    ## This takes quite a while as many modules pop in
    pip install reflex
    ## check them out
    pip list
    ```
4. Give a go
    ```shell
    reflex init
    ```
    It will prompt you some templates to select with, choose the one represents 'NBA'. 

    And the process will generate quite a few files in the project folder.
5. Install some extra python modules: pandas, numpy, etc. (please do)
    ```shell
    pip install -r requirements.txt
    ```
6. Start up the Reflex App
    ```shell
    reflex run
    ```
    Please install `bun` package (`curl -fsSL https://bun.sh/install | bash`) if you confront a warning like:

    > Warning: There was an error running command: ['/home/zenusr/.local/share/reflex/bun/bin/bun', 'install'].
    >
    > Warning: There was an error running command: ['/home/zenusr/.local/share/reflex/bun/bin/bun', 'add',...

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
    

