---
title: "Frc Scouting App"
date: 2021-07-30T01:46:00-04:00
draft: false
---
### tldr
Developed a data collection app to facilitate the recording, organizing, and uploading of scouting data gathered by FRC teams. Data was collected on an app made in flutter, and uploaded to a Firebase NoSql database, and organized using Firebase Functions written in Javascript. The App was later modified to use QR codes to transfer data and SQLite databases to store data.
### Purpose
At First Robotics Competitions, teams record data on other teams, to identify opponent strengths and weaknesses. Scouting is used to aid the drivers in deciding their strategy. It’s also used to identify and compare teams so that when it comes time to choose teams to form alliances with, we know what teams we’d like in our alliance/ which alliance we’d like to be picked for.
### Scouting app V1
The first version of the system was written in Flutter and used Firebase to store the scouting data. Two apps were made, a scouter app and a head scouter app. The standard scouter app basically opened a form that allowed the scouter to enter in details from the match and team they were scouting. They could then hit a submit button to upload the data to the database. The head scouter app retrieved data from the firebase database. The head scouter app could also sort the data based on specific values, like points scored, team number, match number, etc. This app was used in the strategy meetings to help choose teams for the alliance. It was also used by drivers to quickly pull up information on the teams they would be facing in the next match.
### Scouting app V2
The second version of the system had massive changes. First of all, we removed firebase from the system. This is because we would be relying on scouters cell phone plans to send the data to the cloud database. When we went to the world championships in detroit, almost none of our team members had data. We would also hit our quotas and that resulted in loss of data.  V2 of the app used SQLite to store the data directly on the phones, and QR codes were used to pass the scouting data from scouters to the head scouter. We also only had 1 app, rather than a separate scouter and head scouter app. If data had to be sent over long distances (for example, from the scouters to the robot driveteam), the data could be exported as text and sent in an email or instant message. The receiving person could just copy that text into their scouting app and to get all the data. Besides these changes, the base functionality of the app was kept the same.
