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

