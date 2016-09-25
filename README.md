# Skin Lessions Classification using Convolutional Neural Networks
<b>Authors</b>:  Adria Romero López, Jack Burdick, Janet Weinthal, Adam Lovett <br>
<b>Advisor</b>:  Professor Oge Marques 

##Setting up the programming environment:<br>

###1. Installing Python 2.7 in our computer
*(Jump to  point 2 if your computer has already Python 2.7 installed)*

In order to install Python in our machine, we will need first to install *Homebrew*:
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Insert the Homebrew directory at the top of your PATH environment variable:
```
export PATH=/usr/local/bin:/usr/local/sbin:$PATH
```
Now, we can install Python 2.7:
```
$ brew install python
```

###2. Create a separate Python virtual environment
We are going to create a virtual environment exclusively for Keras-based projects to avoid problems related to conflicting library versions. <br>

Install virtualenv via pip:
```
$ pip install virtualenv
```
- Create a virtual environment for a project
```
$ cd my_project_folder
$ virtualenv venv
```
**virtualenv venv** will create a folder in the current directory which will contain the Python executable files, and a copy of the pip library which you can use to install other packages.

Next package to install is *virtualenvwrapper*. It provides a set of commands which makes working with virtual environments much more pleasant.

```
$ pip install virtualenvwrapper
$ export WORKON_HOME=~/Envs
$ source /usr/local/bin/virtualenvwrapper.sh
```

- Create a virtual environment:
```
$ mkvirtualenv fau-keras
```
This will create a Python virtual environment named **fau-keras** . This creates the *fau-keras* folder inside ~/Envs.

- Work on a virtual environment:
If we want to access this virtual environment, just use the **workon**  command followed by the name of the virtual environment:
```
$ workon <virtual env name>
```
In this case, we can access the keras virtual environment by executing the following command:
```
$ workon fau-keras
```
- Deactivating the virtual environment:
```
$ deactivate
```
- To delete:
```
$ rmvirtualenv venv
```

####Other useful commands
- List all of the environments:
```
lsvirtualenv
```
- Shows contents of site-packages directory.
```
lssitepackages
```

