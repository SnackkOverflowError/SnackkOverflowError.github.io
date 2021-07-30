---
title: "Spaceapps"
date: 2021-07-30T02:03:00-04:00
draft: false
---
[link to project](https://github.com/AadityaChaudhary/space_apps)
### tldr
Developed the front end for a site that uses Machine Learning topredict whether a city will be a covid hotspot given certain parameters. Also did data collection for the ML model, and worked on the python backend.
### Purpose
The point of the competition was to utilize data gathered by different government agencies (such as NASA) to aid with the covid outbreak in some way. My team decided to make a website that could predict if your town will become a covid hotspot based on past data of covid hotspots.
### Features
The website was written with flutter, and asked the user for information about their city. These values would be sent to a flask server where they would be passed into a classifier trained using data provided by different government agencies (as well as data we manually collected). The flask server would then return whether it was likely that the city would become a covid hotspot or not.
