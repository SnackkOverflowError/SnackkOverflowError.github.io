---
title: "Go-email"
date: 2021-07-30T00:12:15-04:00
draft: false 
---

[link to project](https://github.com/AadityaChaudhary/go-email)
### tldr
Developed an open-source library that interfaces with various IMAP, SMTP, and OAuth implementations in Go, to facilitate email app development.

### Purpose
The purpose of this library is to provide a simple way to interact with SMTP and IMAP servers by providing an easy to use wrapper around existing SMTP and IMAP implementations in Go. The existing implementations provide a lot of flexibility, however, with that comes a steep learning curve for developers. This library provides easy to use functions that encompass the most common features of SMTP and IMAP. It also works with XOauth2 as most major email providers support this authentication protocol and it is more secure compared to using usernames and passwords.
### Implemented Features
This library currently supports two methods to authenticate. One using the user's password and email, and one using their email and token. The library also supports the openID flow to get tokens. In terms of IMAP, the libray supports getting a range of email envelopes that contain information like sender/reciever, cc, bcc, time, etc. From these envelopes, the developer can also call a seperate function to grab the message content, formatted as a slice of message parts (because messages can be a combination of text, files, images, etc). The last IMAP feature is the easy to use and comprehensive search feature. The library also supports sending simple emails over SMTP.
### Future Changes/Updates
There are quite a few changes I want to make to this library. It was developed to aid with another project I was working on, so while it does work well and meet its original purpose, there are things that I'd like to add to it. First of all, I'd like to improve the documentation of this project. I want to make the README comprehensive and clear and I'd like to comment all of the functions and remove commented out functions and code. I'd also like to fix some formatting issues with the code. In terms of functionality I'd like to improve the SMTP functionality. It met my requirements at the time, but it could be better to meet more developer's requirements. Depending on the existing STMP implementations in Go, I may have to improve one or make my own to add this feature to go-email.

