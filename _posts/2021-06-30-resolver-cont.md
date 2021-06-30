---
title: "Finishing the resolver"
excerpt_separator: "<!--more-->"
categories:
  - Project
tags:
  - Coding
---
I am still working on adding the resolver for the application. I had to fix a bug yesterday with the car review not working despite the cards being past the due date. In the process of adding a resolver, I decided to create a service which the resolver will update with a message about the data still loading. This service will then communicate with the component resonsible for the template that displays the messages to the user.
