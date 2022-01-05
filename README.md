# python-for-data-science-path
Python basics for Data Science, making it the most used tool among analytics

## Prerequisite
- [Python3](https://www.python.org/downloads/) was installed


## Create isolated Python environment
[virtualenv](https://virtualenv.pypa.io/en/latest/) is a tool to create isolated Python environments
```
python3 -m pip install --user virtualenv
python3 -m virtualenv --help
```
[virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/install.html) is a set of extensions to `virtualenv` tool, The extensions include wrappers for creating and deleting virtual environments and otherwise managing your development workflow.
```
python3 -m pip install virtualenvwrapper
```
`virtualenvwrapper` is a command line application, the default values for the command line options can be overridden via the configuration file or `Environment Variables`, 

### Shell Startup File
Add three lines to your shell startup file (.bashrc, .profile, etc.) to set the location where the virtual environments should live, the location of your development project directories, and the location of the script installed with this package, take my mac as an example, I'm using zsh, so I will append below environment variables to ~/.zshrc file:
```
export VIRTUALENVWRAPPER_PYTHON=/usr/local/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV=/usr/local/bin/virtualenv
export WORKON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/Devel
source /usr/local/bin/virtualenvwrapper.sh
```
NOTE: `VIRTUALENVWRAPPER_PYTHON` is a variable of the full path of the python3 interpreter. please use `which python3` to locate your python3.

### Quick start on a new project
- Run: workon
A list of environments, empty, is printed.
- Run: mkvirtualenv temp
A new environment, temp is created and activated.
- Run: workon
This time, the temp environment is included.
- Run: python3 --version
Display the python3 version for this virtual python3 environment
- Run: python3 -m pip list
Give you a empty python3 environment
- Run: python3 -m pip install pandas
Install pandas module in this virtual environment
- Run: deactivate
Quit virtual environment 
- Run: workon temp
Apply `temp` virtual environment