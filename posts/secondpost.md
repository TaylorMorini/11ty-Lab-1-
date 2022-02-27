---
title: Getting Started with Docker
description: This is a post on My Blog about Docker
date: 2022-02-27
tags:
  - number 2
layout: layouts/post.njk
---
## Why is Docker a Powerful Tool?
One of the main reasons Docker is a powerful tool is its architecture. Docker uses a client-server architecture.  According to the Docker documentation, 

> The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers

A visualization of this occurring: 

![Docker Architecture](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/93vcr7djmemx2nmhhpjh.png)

##Starting out with Docker
To begin using the Docker Playground follow these steps:

- Go to this [link] (https://www.docker.com/play-with-docker)

- Navigate to the section labelled "Play with Docker" 

![docker starting out](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sfbcnjvw0qda1bqcb6k6.png)

- Log in or create an account 

- Press the start button and add a new instance

##How to Create a Dockerfile for NASA Image Search 

###Setup
1. In the Docker Playground add a "New Instance". This will open a terminal on the screen.  
2. On GitHub, navigate to the Nasa Image Search repository and click "Code". Copy the link, and in the Docker Playground run a `git clone` and `cd` into the cloned repo

![console img](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/020s6mni2vvicqv5l5ws.png)

###Configure
- Run this command: `touch "Dockerfile"`.  This will create a new file called `Dockerfile`.  This is where custom settings can be added.  
- Access your new file via the "Editor" in Docker Playground.

![editor](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/76ai4xr31j3okbmgs7us.png)
- The document that you have added will need to be configured.
![docker](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/422splygsghkjwzevfqh.png)

- Now we must reference an endpoint for Nasa Image Search.  For this example, the endpoint would be `https://402a.github.io/ip-project/ `

In the News example, this is where you would run `cp dot.env.example dot.env`.  This would give you the ability to open the `dot.env` file and populate it with specific data (a generated API Key and the NewsAPI endpoint): 

![endpoint](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2knch7l4au6j24mc9r6u.png)

For the Nasa Image Search example you can first run another touch command.  For this, I ran `touch "dot.env"`.  Here, you would populate the document via the editor.  The endpoint, `https://402a.github.io/ip-project/` is added to this document.

###Open Port
- Once you have completed the configuration, you can now click on the "Open Port" button at the top of the Docker Playground screen. 

![open port](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vjzx72eplr2v78h1zy7o.png)

- You will be prompted to enter a port number. For this example, I inputted "4000"

![4000](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jkekv4f9upqnive80vp2.png) 

- You will not immediately be able to open the desired page.  To do so, you will need to copy the URL of the page that opens when you input "port 4000".

![4000-2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2e45rv2rykod77l3o6sp.png)

- This URL should be added to the `dot.env` file as the endpoint.  Click 'Save' after this has been added. 

###Starting the application
- After everything has been added, run the line `docker-compose up` in the playground. This will open port 4000.  

![4000 opens](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/65tvbvpbf9qjn1dfpwxd.png)

- Click on port 80.  If all was successful, you will be able to view the working application. 

News Example: 

![port 80](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9i9r7ievvr858cwuxva8.png)



####Helpful Links:

1. [Docker Documentation](https://docs.docker.com/get-started/overview/)

2. [Nasa Image Search Code] (https://github.com/402A/ip-project)

3. For the News API Key: [News API Site] (https://newsapi.org/register/success)


