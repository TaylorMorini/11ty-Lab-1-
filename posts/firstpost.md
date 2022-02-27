---
title: Getting Started with Webcomponents
description: This is a post on My Blog about web components
date: 2022-01-16
tags:
  - another tag
layout: layouts/post.njk
href: https://dev.to/taylormorini/getting-started-with-web-components-10k0

---
Would you like to learn how to create a simple "Hello World" screen using JavaScript and Web Components from scratch? Follow these steps to see how I did it!

## Before you Start

- Install [oh-my-zsh](https://ohmyz.sh/#install)
_It is not necessary to install this on your terminal, this is a preference.  It does, however, increase usability in my opinion._

![zsh](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xig52hcvhbknwjx6eq8h.png)

- Install [Visual Studio Code](https://code.visualstudio.com)
_This is my preferred IDE to complete this process._


![vs code](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2ifp4843ioigzw4tsfmj.png)


## What is Node.js/NPM?
>As an asynchronous event-driven JavaScript runtime, Node.js is designed to build scalable network applications.

Basically, Node.js is going to allow you to run code written in JavaScript.  NPM is the default package manager for Node.js.  This means that it:
>puts modules in place so that node can find them, and manages dependency conflicts intelligently.

The good news is that once you have successfully downloaded Node.js, NPM will automatically be usable!

## Downloading Node.js

Go to [Node.js](https://nodejs.org/en/) to begin installation.  If you are using a Mac like I am, you should see a screen that looks like the following image: 
![Node.js Download](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ko4klemyujahtrmm42rx.png)

You are going to want to download the "Recommended For Most Users" version.  Once installation is complete, you can go to your terminal and run `node -v`. 
![Checking installation](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xw7kipx0klh72mb9k1kp.png)

If you have correctly installed Node.js, then you should see the version of it that was recommended.  To check NPM, simply do `npm-v`.  If everything is in working order, you will see that there is a version of NPM running on your machine. 

![npm](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wp6xpa12ggikmg37tkb9.png)


## Working with GitHub
The first thing you're going to need to do is create a profile for [GitHub](https://github.com). Once you have created a profile, you can create a new repository by clicking the "New" button, as shown below. 

![repo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3oe0gy63g09ivjd0jjnb.png)

If you haven't already, install [Git] (https://git-scm.com/downloads).  This is going to make it possible to interact with GitHub via your terminal.  To ensure Git is installed, run `git --version` in your terminal.  If you have successfully gotten git, then you will see a similar screen (below): 
![git](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/am1qi3pewm5jqtzi2o5t.png)

## Making a Directory via Terminal
Following these steps you can make a directory straight from your terminal:

1. Open the terminal.  Run `cd Documents`. _This is going to navigate you to the Documents folder on your machine.  This is where I made my directory._
2. Run `mkdir sampleDirect`.  _You can name it anything, but for the sake of the example I named mine "SampleDirect"._
3. Run a `ls` if you want to be sure that it has successfully been created.
4. `cd sampleDirect` _Note: if you run a `ls` here, its going to appear empty because you haven't added anything to it yet._


## Bringing it all Together
Keep your terminal open!  If you closed it, simply run the following (name specific!) to get back to your directory: 
`cd Documents/sampleDirect`

The first step you should take is to clone your repository.  To do so, copy the link for your specific repo: 

![the setup](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wg2mwx3o52iytwle1mf3.png)

Back in your terminal, run `git clone` and then your specific link.  It should look something like this: 

![clone](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rojl4rc2rt186amghs5y.png)

Run a `cd`.  I named my Repo "sample-" so for me, I would run `cd sample-`".

The next thing you are going to want to do is run this command:
`npm init @open-wc`.

![opening](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/b34g5fhrm6s8ci3jvq8r.png)

From here: 

1. _What would you like to do today?_`scaffold new project`
2. _What would you like to scaffold?_`Web component`
3. _Would you like to use a typescript?_ **No**
4. _What is the tag name of your component?_ **hello--World** (you can name it anything)
5. _Would you like to write this file structure to a disk?_ **Yes**
6. _Do you want to install dependencies?_ **Yes, with npm.**

![fsetup](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7x5kemm7lfdzvbykhdx3.png)

Successful setup will show: 

![success](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/h3d6ol1cr6vumgz428hb.png)

1. In the terminal, run `cd hello--world`
2. Run `npm run start`

Running `npm run start` in the terminal will yield: 

![completed!](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wzqduw9gva1dh7bbj355.png)

##Opening with Visual Studio Code
Use the following steps to open with VS Code:
1. At the 'Start' page in VS Code select the **open** button
2. Navigate to 'Documents'
3. Select your directory (mine was _sampleDirect_)
4. Open your 'hello--world' file


![vsCode](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xkyjhtzisg0qf87s1b9x.png)
## More Help
Here is a helpful cheat-sheet for [Git](https://education.github.com/git-cheat-sheet-education.pdf) commands.
This is a helpful tool to learn [more] (https://lit.dev/playground/#sample=examples/full-component).
Here is my [GitHub repo] (https://github.com/TaylorMorini/402-lab).
