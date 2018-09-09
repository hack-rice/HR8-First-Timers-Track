# Reddit Bot

## Introduction

This document will provide a step-by-step gudie to developing your first Reddit bot. We'll be using Python since it's a very beginner-friendly language and offers perhaps the simplest implementation. Alternatively, you're welcome to use JavaScript + Node.js, in which case you can find an excellent guide [here](https://blog.syntonic.io/2017/07/07/reddit-bot-nodejs-example/).

There are a few components that we have to set up in order to get a functional bot. First, we need to set up a server to listen for comments on Reddit. *Flask* is a web framework built on Python, so we'll use it to greatly simplify this process. Next, we'll need to enable the bot to respond to the user's messages. We'll code the logic in Python and use the *requests* library to sent the bot's chosen response back to Facebook. We'll explain each of these steps in more detail as we go through them. 


## Software

Before we begin, we need to make sure all the necessary software is installed. Here are the things you'll need:
* [Python 3.6.5](https://www.python.org/downloads/release/python-365/)
* Pip3


### Cygwin installation (Windows users only)

Visit [this website](https://cygwin.com/install.html) to install Cygwin.  For each screen on the installer where it provides a default option, the default is fine.  However, there is one screen that asks you to "Choose A Download Site".  Any site should work; however, some work better than others.  'https://mirror.steadfast.net' works well.

From this point on, whenever the tutorial says to use the terminal, you should use Cygwin instead.

### Dependencies
Most newer versions of Python come with pip, so it should be already installed. SPecifically, we want to have pip3 installed. To check if you have pip installed already, type `which pip3` into the terminal. You should see the version number printed to the terminal if you have it.

If you don't have pip, you can install it [here](https://pip.pypa.io/en/stable/installing/).

This app has only one dependency which is PRAW 4, a Python wrapper for the Reddit API. Now that we have pip, we can enter into the terminal to install it:
```pip3 install praw```

## Bot Registration

We need to register the bot with reddit to enable it to actually interact with the site. TO do this, you'll need to log in to Reddit or create a new account. Navigating to the *preferences* page, you should see a tab titled *Apps*, with a button at the bottom that says "are you a developer? create an app...". Click on this button, and you'll be prompted to enter information about your bot. The title and description aren't very important, and you can check the *script* radio button since this won't be a full web app (not yet). 




