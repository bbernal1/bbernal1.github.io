---
title: "Finishing the resolver"
excerpt_separator: "<!--more-->"
categories:
  - Project
tags:
  - Coding
---
I am still working on adding the resolver for the application. I had to fix a bug yesterday with the card review not showing any cards up for review even though cards were past their due date. In the process of adding a resolver, I decided to create a service which the resolver will update with a message about the data still loading. This service will then communicate with a messages component which will be responsible for the template that displays the messages to the user.
