# Skin Lessions Classification using Convolutional Neural Networks
<b>Authors</b>:  Jack Burdick, Adrià Romero López, Janet Weinthal, Adam Lovett <br>
<b>Advisor</b>:  Dr Oge Marques 

##Setting up the programming environment:<br>

###Step 1. Installing Python 2.7 in our computer
*(Jump to  step 2 if your computer has already Python 2.7 installed)*

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

###Step 2. Create a separate Python virtual environment
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
###Step 3. Install Keras
*(For step 3 we must be  working on the virtual environment).*
First, we need to install a few dependencies:
```
$ pip install numpy scipy
$ pip install scikit-learn
$ pip install pillow
$ pip install h5py
```
We also need to install Theano:
```
$ pip install Theano
$ sudo pip install --upgrade theano
$ theano-cache clear
```
Now we can install **Keras**:
```
$ pip install keras
```

###Step 4. Setup GPU support (once we have access to the HPC)
(to be completed)

###Step 5. Test out the installation
To verify that Keras has been installed, access the keras virtual environment, open up a Python shell, and import it:
```
$ workon keras
$ python
>>> import keras
```

A message *"Using Theano backend."* should appear at the terminal.

###Common errors:
- (In OS X) Check you have  **Xcode** installed (Theano will need **g++ compiler** that its installed with Xcode).<br>

Author: @Adrian (Contact me if you find some errors/doubts: adriaromero@me.com).<br>
References:  [Installing Keras for deep learning] (http://www.pyimagesearch.com/2016/07/18/installing-keras-for-deep-learning/)

