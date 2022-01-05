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
- Run: workon \
A list of environments, empty, is printed.
- Run: mkvirtualenv temp \
A new environment, temp is created and activated.
- Run: workon \
This time, the temp environment is included.
- Run: python --version \
Display the python version for this virtual python environment
- Run: python -m pip list \
Give you a empty python3 environment
- Run: python -m pip install requests \
Install pandas module in this virtual environment
- Run: deactivate \
Quit virtual environment 
- Run: workon temp \
Apply `temp` virtual environment
- Run: rmvirtualenv temp \
Delete `temp` virtual environment if you don't need it anymore

### Requirements files
Requirements files are files containing a list of items to be installed using pip install, Given you already installed `requests` module in the `temp` virtual environment, we can use `pip freeze` to dump installed module list to a file named `requirements.txt`
```
python -m pip freeze > requirements.txt
```
Imaging you are one of the team member who work together on a python project, if someone installed a new python module he will update `requirements.txt` and committed to github. 
You could run below command to install new modules:
```
python -m pip install -r requirements.txt
```

## Create Jupyter notebook
The notebook extends the console-based approach to interactive computing in a qualitatively new direction, providing a web-based application suitable for capturing the whole computation process: developing, documenting, and executing code, as well as communicating the results. The Jupyter notebook combines two components: A web application and Notebook documents.
You can install Jupyter by installing [Anaconda](https://docs.jupyter.org/en/latest/install/notebook-classic.html0) or just by pip.

Instead of use Jupyter notebook directly, we also can use it in [VSCode](https://code.visualstudio.com/docs/datascience/jupyter-notebooks), PyCharm(professional edition) etc IDE.

### Quick start with Jupyter notebook in PyCharm
- Create a new Python project, specify a virtual environment.
> Press ⌘ , to open the project Settings/Preferences and go to Project <project name> | Python Interpreter. Then click the The Configure project interpreter icon and select Add.

- Open or create an .ipynb file.

- Add and edit source cells.

### Quick start with VSCode
- Install [Jupyter Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- Creating a new .ipynb file in your workspace
- Execute any of the code cells to launch the Jupyter server.

## Data science skill learning path
- Python basic syntax
- Data structure
    - list
    - array
    - dict
    - tuples
 - Matrix
    - numpy
    - matplot
 - Data frame
    - pandas
 - Visualization
 - Data processing
 - Linear regression
 - Classification
 - Clustering
 - Association rule learning
 - Reinforcement learning
 - Artificial Neural Networks
 - Convolutional Neural Networks