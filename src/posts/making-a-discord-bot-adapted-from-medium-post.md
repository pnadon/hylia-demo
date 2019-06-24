---
layout: layouts/post.njk
title: Making a Discord Bot (adapted from Medium post)
date: 2019-06-23T23:55:13.778Z
---
**Credit goes to [mupster](https://medium.com/@moomooptas) on [Medium](https://medium.com/@moomooptas/how-to-make-a-simple-discord-bot-in-python-40ed991468b4). Since that post some changes have been made to the Discord API which are covered in this post, as well as how to actually host the bot once you are finished with the coding portion**

# Introduction

The goal of this tutorial is to setup a bot for Discord which will perform actions such as automatically respond to certain messages. At the end of this tutorial, when you send the message "Hello" in the Discord server, your bot should reply with "World".

This tutorial will be divided into a server setup portion, and bot creation portion.

# Setting up a server with Amazon Web Services
Amazon Web Services (AWS) by Amazon offers a wide variety of software-related services, one of which allows us to run Linux instances on their servers. This will allow us to run our bot on the cloud, where alternatively we would have to set up the server on our own machine, and leave it running for as long as you want the bot to work. 

## 
