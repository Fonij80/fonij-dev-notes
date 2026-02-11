### Fonij Vocabulary

- VE: virtual environment
- proj: project
- env: environment
- var: variables
- dep: dependency

### Django Cheat Sheet

- Create django project steps:

  1- Create VE: # make sure that python is installed on your system
  - `python -m venv .venv`

  2- Activate VE:
  - `source .venv/bin/activate`

  3- Install django:
  - `python -m pip install django~=<version>`

  4- Create proj:
  - `django-admin startproject <project_name> .` # . means create project in the current folder

  5- Run proj:
  - `python manage.py runserver`

  6- Deactivate VE:
  - `deactivate`

- Database-related commands:
  - Make migrations:
    - `python manage.py makemigrations`

  - Apply available migrations:
    - `python manage.py migrate`

  - Postgres DB URL: $ DATABASE_URL: postgres://<username>:<password>@<host>:<port>/<database>

- App-related commands:
  - Create app:
    - `python manage.py startapp <app_name>`

- Test-related commands:
  - Run Tests:
    - `python manage.py test`

- Dep-related commands:
  - Update pip:
    - `python -m pip install –upgrade pip`

  - Output content of current VE:
    - `pip freeze > requirements.txt`

  - Env vars manager lib:
    - `pip install django-environ`

- VS-code-related commands:
  - Create .gitignore: CTRL + Shift + P

- ngrok-related commands:
  - Install:
    - `sudo snap install ngrok`

  - Connect:
    - `ngrok http 8000`

- API Schema Generation: $ python manage.py spectacular --file api.yaml

- For SSH Access: $ git@github.com:username/repo_name.git
- PAT: $ https://username:PERSONAL_ACCESS_TOKEN@github.com/username/repo.git

---

title: "Initial Set Up"
lang: en
handle: intial-set-up
layout: default

---

# Chapter 1: Initial Set Up

- Initial set up of every new technology you learn, is a headache but you have to do it once correctly to avoid further headaches.

- Learning Goals:
  - What is Shell?
  - Most used shell commands
  - Install Python
  - Set up virtual environment
  - Use git as version control

## What is Shell?

    - Command line:
        text-only interface,
        used for executing programs, installing software, using Git, connecting to servers in the cloud
        terms refer to the command line:
            Command Line Interface (CLI)
            Console: text-based app
            Terminal: program that opens up a new window to access CL
            Shell: program that runs commands on the underlying OS
            Prompt: where commands are typed and run, $ for Linux prompt, > for Windows and % for macOS.
            PowerShell: built-in terminal & shell on windows
            Terminal: built-in terminal on mac & linux

    - Shell Access:
        - Windows:
            search for “PowerShell” in taskbar search
        - Ubuntu & Mac:
            search for “terminal”,
            Ctrl + Alt + T in ubutnu

    - A Mac Tip:
        Since 2019, zsh is the default macOS shell (% prompt).
        Bash is the previous default macOS shell ($ prompt).

## Most used shell commands

    $ whoami: computer name/username
    $ # some command: not executed, # comment symbol
    $ echo “Hi!”: print sth
    $ pwd: print working dir
    $ cd {dir's_name}: change dir
    $ mkdir {dir's_name}: make new dir
    $ ls: list the dir/file
    $ clear: clear the terminal
    $ exit: close the terminal


    - Command autocomplete: > key in windows, tab in linux/mac
    - ↑ and ↓ keys cycle through previous commands

    * For more commands: https://ss64.com/

## Install Python

    - On Windows: Type “python” in the search bar and select the latest version of Python on the Microsoft Store and to download it.

To confirm that Python is installed correctly, open a new Terminal window with
PowerShell and type python --version. Then, type python to open the Python
interpreter from the command-line shell. You can exit the Python interpreter by typing either exit() or Ctrl-Z plus
Return.

    - On Mac: On Mac, the official installer on the Python website is the best approach. In a

new browser window, go to the Python downloads page and click on the button
underneath the text “Download the latest version for Mac OS X.” As of this
writing, that is Python 3.12. The package will be in your Downloads directory:
double-click on it to launch the Python Installer, and follow the prompts.
To confirm the download was successful, open a new Terminal window and type
python3 --version.
