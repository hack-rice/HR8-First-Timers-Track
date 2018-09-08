# Facebook Messenger Bot

## Introduction

This document will provide a step-by-step gudie to developing your first Facebook Messenger bot. We'll be using Python since it's a very beginner-friendly language and offers perhaps the simplest implementation. Alternatively, you're welcome to use JavaScript + Node.js, in which case you can find an excellent guide with [Facebook's Quick Start Tutorial](https://developers.facebook.com/docs/messenger-platform/getting-started/quick-start/).

There are a few components that we have to set up in order to get a functional bot. First, we need to set up a server to listen for messages from Facebook. This is a stable point so that Facebook knows what to do when the user messages the bot. *Flask* is a web framework built on Python, so we'll use it to greatly simplify this process. Next, we'll need to enable the bot to respond to the user's messages. We'll code the logic in Python and use the *requests* library to sent the bot's chosen response back to Facebook. Finally, since we're developing this locally, we can use a cool tool called *ngrok* to expose the code on our local machine to the web, so that we don't have to host this anywhere and can run our bot from our local machine. We'll explain each of these steps in more detail as we go through them. 


## Software

Before we begin, we need to make sure all the necessary software is installed. Here are the things you'll need:
* Python 3.6 
* Pip


### Cygwin installation (Windows users only)

Visit [this website](https://cygwin.com/install.html) to install Cygwin.  For each screen on the installer where it provides a default option, the default is fine.  However, there is one screen that asks you to "Choose A Download Site".  Any site should work; however, some work better than others.  'https://mirror.steadfast.net' works well.

From this point on, whenever the tutorial says to use the terminal, you should use Cygwin instead.

### Pip installation
If you don't already have pip installed, we'll go ahead an install that now because it will be essential 
for the rest of the project. 

Visit [this website](https://pip.pypa.io/en/stable/installing/) to install pip. Follow the instructions, and once you 
think you're done, type `which pip` to check that pip has been installed. You should see the version number of the pip 
you installed print to your terminal.
