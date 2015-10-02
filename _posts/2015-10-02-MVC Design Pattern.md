---
layout: post
title: MVC Design Pattern
categories: [general, techstuff]
tags: [tech]
---

# Introduction

Model-View-Controller (MVC) is one of the most popular design patterns in the software/web development world. The MVC model was popularised by the Spring Framework, Ruby on Rails and Django. 

As the name suggests, there are three main components of this pattern: Model, View and Controller. An application can be divided into these components which will then interact with one another to achieve the intended objective.

# Interaction Overview

<img src="http://i.imgur.com/U7Z1Eir.png">

# Model

The model component can be summarised to contain objects that provide the logic implementation for the application. Typically, these objects correspond with the storage to retrieve/update/store data.

As stated on [the MSN MVC Overview](https://msdn.microsoft.com/en-us/library/dd381412(v=vs.108).aspx), for small applications, the model does not necessarily refer to a physical layers and its subclasses. If an application just reads a dataset and passes it to the view, then the dataset there takes the role of the model.

# View

View essentially contains the objects/components dealing with the user interface (UI) of the application. The view typically reflects and outputs the data from the model layer. If the model consists of a dataset of students, then the view probably contains a table view of the details of the students with fields such as the First Name, Last Name, Age, Matriculation Number and so on.

# Controller

Controller are components which handle the user interaction and communicate directly with the model, depending on what the user's request is. Based on this communication and response, it then selects a view to render. For example, if the user searches for a specific student's name, the controller then passes the query to the model which then looks up the database, applies necessary filters and then returns the data representing the student (assuming it is a valid search). The controller will now select the appropriate view to present the data to the user. For example, views may change based on the platform (PC/mobile phone/tablet) or the type of user accounts (root/admin/guest) etc.

# Implementation & Advantages

There are several ways the MVC can be implemented. For example, one can choose to divide the interactions both on the client and server side for a web application.

The MVC model can come in particularly handy to organise the structure of an application during development. It can help in parallel development as different members of the team can work on the various components together. Another advantage is that we can separate the concerns of the application in a distinct manner which allows for better developer focus.

