---
layout: post
title: Tutorial - Introduction to HTML (Part 1)
categories: [general, techstuff]
tags: [tech]
---

# Introduction

In this first part of the Introduction to HTML, I will be going through the basics of HTML. 

HTML stands for HyperText Markup Language. This is the standard markup language which allows web browsers (such as Internet Explorer/Firefox/Chrome) to render content into the webpages you visit (yes, including this one). If you haven't been acquainted with HTML at all, you might want to try right-click and "view page source" on Chrome/Firefox browsers. A typical screenshot of the page source (from Apple.com) is this:
![HTML page source of Apple.com](http://i.imgur.com/Hsg4sWu.png)

Please don't be daunted by the intimidating lines of code. We will start right from the basics.

<hr>

# Structure of a HTML File

{% gist harishv7/6896f30b6453a9cc5ae7 %}

The above is the basic structure of a HTML file. The document starts with `<html>` tag which defines the start of the document. The file is basically divided into 3 major sections, namely, `<head>`, `<body>` and `<footer>`. 
	
The head contains basic information such as the title of the webpage and some scripts or resources to be loaded when the file is opened. 
	
The body contains the main content of what the user is to see and the optional footer typically contains links to the various sections of the website etc.

Firstly, in the head tag, we can include the site's title. For example:
```
	<head> 
		<title> My Title </title>
	</head>
```

The above snippet will specify that the title of the webpage is "My Title".

Now you can also try this out by copying the above snippet(s), pasting it into an editor of your choice (eg: Notepad/TextEdit/TextMate). If you are clueless which editor to use, I would suggest using [Sublime Text](http://www.sublimetext.com/).

<hr>

# Headings

We can highlight certain parts of the page by selecting different sizes of headers. This is done with the header tag. Headings range from `<h1>` to `<h6>`, where h1 defines the largest heading and h6 is the smallest. 

For example:

	<h1> This is a big heading </h1>

translates to:	
<h1> This is a big heading </h1>

and

	<h6> This is a small heading </h6>

translates to:
<h6> This is a small heading </h6>

<hr>

# Paragraphs

We can include paragraphs with the `<p>` tag.
	
	<p> hello, i am harish. this is a sample paragraph. </p>

translates to
<p> hello, i am harish. this is a sample paragraph. </p>

# Images

No webpage is complete with just some simple text. So how do we add images?
You do it with the `<img>` tag.

The full tag looks like 

`<img src="https://upload.wikimedia.org/wikipedia/en/6/65/Hello_logo_sm.gif">`

translates to

<img src="https://upload.wikimedia.org/wikipedia/en/6/65/Hello_logo_sm.gif">

There you go. You have just added an image to your page. 

Adding from local folders (pictures residing on your computer, offline) is slightly trickier. For example, if the picture is in the same folder as where you save your html file, and is called "picture.jpg", then your image tag will look like this:

`<img src="picture.jpg">`. If it is in a subfolder of your current html file, then it would look something like `<img src="subfolder/picture.jpg">`

<hr>

That's all for the first part. A sample webpage that you should have by now should be something like this:
{% gist harishv7/051a48b69f31e427ece7 %}

that looks like this:

![Screenshot of Sample HTML Page](http://i.imgur.com/sRCwIoD.png)

Part 2 coming up soon.

Cheers, <br>
V.Harish