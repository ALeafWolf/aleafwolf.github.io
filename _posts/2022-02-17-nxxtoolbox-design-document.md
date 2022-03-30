---
title: "NXX-Toolbox: Design Document"
layout: single
categories: 
    - Study
tags:
    - Angular
    - Project
header: 
    teaser: "/assets/img/davis.jpg"
---
# Introduction
[NXX-Toolbox](https://www.nxxtoolbox.com) is my first lived, fullstack website project I build for study propose, I want to apply and pratice with the tech stack I familiar with based on the topic I like. This project is not perfect, and have many place need to improve, but I learnt a lot, will continue maintaining this site, and bring the experience onto other future project.

# Project Overview
[NXX-Toolbox](https://www.nxxtoolbox.com) is a WIKI-like site for the mobile game Tears of Themis, which includes the essential data from game for other players to browse and search, and also other facility, like in-game power calculator, to assist player's game experience. 

Originally I just want to build a calculator to calculate the battle power in game, but I need to get all cards' data in order to make this calculator to work. After I finished collect the required data, I made a simply filtable table for these cards and corresponding skills. Then just keeping build up the functionality I can think of, NXX-Toolbox gradually become the look as you can see today.

## Architecture
The site can be seperate into three parts: frontend, middleware and backend.

## Frontend
### Choose of Framework
The reason I choose Angular is at the time, I want to learn a modern frontend framework (Jamstack), and I saw **Angular** first when I go through the job post, so I pick it, no fancy reason here. At the moment Angular 11 is the newest stable version (I believe), so I started build the frontend while learning the schema of the Angular at the same time.
### Site Deployment
For deploying the frontend, I choose Github Page. 

Because, it's FREE. ;)

Since I'm not (and should not) gainning any profit from using the data belong to Mihoyo (the developer of the game), I need to cut the cost as much as possible. And it's fairly easy to deploy the site on Github Page, just need to build the project, pushed the built project onto a seperate branch, deploy Github Page on that branch, and done. Simply and easy.
### CSS Styling
Since I need to make the site responsive, so the mobile user have an optimized view on the smaller screen. I choose **Bootstrap** to manage the breakpoints of the site, as well as using the classes and components from them to unify the overall UX of the site.
### Future Improvement

## Middleware
For the moment, I just learnt writing REST API with Express.js on Node.js, so 

As for deploying the API, I choose to host it on Heroku. 

Because, it's FREE, with a decent amount of free credit per month. 
### Attempt to switch to Graphql
After the time I knew the existance of Graphql, 
## Backend
### Data Relationship
The data relationship of all entities are not complicate, can be shown as following diagram:

## Other Aspect
### Image Format and Storing

### i18n

# Conclusion