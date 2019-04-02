# Introduction

If you are a developer working with python, you should be using VirtualEnv to manage requirements for your projects and Virtualenwrapper to make your life easier with useful shortcuts.

The goal of this post is to help you configure your python installation in a way that prevents future problems in OSX.
We are assuming that you are working with python3.

Note if you are running OSX Mojave, it still comes with python 2 by default so we will ensure your setup doesn't use these system libraries for development.

This post is based on 
https://swapps.com/blog/how-to-configure-virtualenvwrapper-with-python3-in-osx-mojave/

But have run across a few other good articles on setting up a Python development environment:

- https://packaging.python.org/guides/installing-using-pip-and-virtualenv/
- https://sourabhbajaj.com/mac-setup/Python/virtualenv.html


# Setup Steps
Let’s have everything up to date and check that system is OK before we start:
```
brew update && brew upgrade
brew doctor
```

The results should 
read something like:
```

brew doctor
Your system is ready to brew.

```
If you get warnings, we recommend that you fix them before continuing to next step as your life could be complicated in the future steps.

No lets check to see if python 3 has been installed:

```
$ python3 --version
```

If not, use this command to install python3:
```
brew install python
```

At this point you probably have installed both python 2.7 and python 3 installed, however if you type in python -V, you will still get python 2.7 as its still the default, and you will only get python3 if you explicitly run python3.

```
python -V
Python 2.7.10

python3 -V
Python 3.7.1
```

While we could run python3 for everything, it might complicate other system activities so instead we will set python3 as the default version of python to use on my user. 

To do so we are going to modify the PATH with the following instruction:
```
export PATH="/usr/local/opt/python/libexec/bin:/usr/local/sbin:$PATH"
```
With this instruction, you have set precedence to your python3 installation over the default python installation, and you can verify it by running:

```
python -V
Python 3.7.1

pip -V
pip 18.1 from /usr/local/lib/python3.7/site-packages/pip (python 3.7)
```

## Virtualenvwrapper installation and configuration
Now that we have updated the python and pip configuration we can now setup the virtualenvwrapper installation will be much easier.

and just as explained in the installation guide

```
  $ cd $HOME (or home directory)

Run following commands

  $ pip install virtualenv

  $ pip install virtualenvwrapper

Now add it to shell startup file (.zshrc):

 $ export WORKON_HOME=$HOME/.virtualenvs

 $ export PROJECT_HOME=$HOME/Devel

 $ source /usr/local/bin/virtualenvwrapper.sh
 ```
