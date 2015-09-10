---
layout: post
title:  "A simple MEAN+ application in Bluemix"
date:   2015-09-08 18:01:11
categories: bluemix node.js
tags: bluemix node.js
---

MEAN is a combination of MongoDB, Express.js and Angular.js running on Node.js. This tutorial will walk you through the steps of creating a MEAN application on Bluemix with the added flair of layout by Bootstrap and templating by Jade.

Note: If you prefer to take a shortcut, see Deploying a MEAN application to Bluemix in one click. Otherwise continue with the step-by-step instructions below.
Steps

    Create a Node.js with Express.js App
    Create a Git repository and clone to localhost
    Add Angular.js
    Add Bootstrap
    Add MongoDb
    Add Jade
    Add an API for GET /people
    Connect to MongoDb
    Create a sortable table with Angular

Create a Node.js with Express.js App

I will be using Bluemix to host, build and deploy my Node.js application and the MongoDb service. I am developing on my localhost for unit testing before I upload my application to Bluemix, but you can also use the online editor and online Git instead.

    If you do not have a Bluemix account yet, sign up for a free trial
    Once you have an account, go to your Bluemix console
    Go to your Dashboard
    In the 'Cloud Foundry Apps' box, click 'CREATE APP',
    Choose 'WEB'
    Select 'SDK for Node.js' and press 'CONTINUE',
    Enter an application name, e.g. '<alias>-mean1' (remkohdev-mean1) and Click 'FINISH'.

Cloud Foundry creates your Node.js application and stages the application in the 'SDK for Node.js' runtime using a Node.js buildpack. Cloud Foundry is an open source container technology similar to Docker and Bluemix uses Cloud Foundry to create, deploy and manage your application. For more information, go to www.cloudfoundry.org.
Create a Git repository and clone to localhost

    If you are not on the application detail page, go to the Bluemix console, to the Dashboard, and click on the <app name> box, which will take you to the application detail page:
    Click on the Overview link,
    In the top right corner of the Overview page, click 'ADD GIT',
    Check the 'Populate the repository with the starter application package and enable Delivery Pipeline (Build & Deploy)' checkbox.
    Press 'CONTINUE' and then 'CLOSE'
    You now should see a link to your remote GIT repository and an 'EDIT CODE' button, in the top right corner instead of the 'ADD GIT' link.
    Click on the git link then on the 'EDIT CODE' button, or click the 'EDIT CODE' button directly to go to the git repository,

You don't have to clone the Git repository to your localhost to upload changes, alternatively you can use the online editor and commit changes online. If you use the online tool, you can skip the steps below.

    In the Git repository on hub.jazz.net, in the 'EDIT CODE' page, find the 'Git Url' of our project
    Copy the Git Url of your project
    In your favorite Git client clone the remote repository to your local development directory, authenticate with <alias> and password. From the command line:

    $git clone https://<alias>:<IBM_ID_password>@hub.jazz.net/<alias>/<project_name>



