---
title: "Quinoa"
date: 2021-07-30T01:29:42-04:00
draft: false
---
[Devpost Link](https://devpost.com/software/quinoa-your-virtual-secretary)
[Backend Code](https://github.com/LunarCoffee/Quinoa)
[Flutter App Code](https://github.com/AadityaChaudhary/PersonalAssistantApp/)
[Alexa Code](https://github.com/1whatleytay/quinoa/)
### tldr
Developed a smart personal scheduling app that learns from the user and suggests times to schedule events based on past decisions the user has made using machine learning. This was made for HackTheNortheast and won the machine learning prize.
### Purpose
Quinoa is a personal assistant scheduling app that can automatically schedule events according to user preferences. It does this by learning what times the user would like to schedule specific events with a custom machine learning model designed specifically to learn how to schedule events over time.
### Features
Quinoa is made up of 3 parts. The first is a backend written with Kotlin that stores a user's calendar in a MongDB database. This backend serves the users schedule to the other components in the system. When a user schedules an event the the backend records it and starts “learning” how the user prefers to set up their schedule. For example if the user schedules a party on friday night from 7pm to midnight, the backend records that event and then records that the user prefers leisure activities on friday nights. The next time the user asks for a time to schedule a party, the backend will suggest friday night.
The main frontend of the project is a mobile app that runs on ios and android, built with Flutter. The app is responsible for displaying the schedule, and taking input from the user. It uses a Tensorflow model to classify the type of event that the user registers. So, if a user wants to schedule a study group meeting on a specific day, the app will identify that the event is for school, and will ask the backend for a time slot for a school event on a certain day. The backend sends a potential time slot and the app presents that to the user. If it’s rejected by the user, the app tells the backend and requests another slot. The model learns from both time slot approvals and rejections. The third part is the alexa application. This application uses AWS Lambda to allow the alexa to function in the same way as the app, but without the event classifier. Without that classifier the type of the event is determined by keywords in the event.
### Awards
This project won a machine learning prize at Hack the Northeast. It also won the 1517 prize, which is a grant of 11k dollars in cash and AWS credits.
