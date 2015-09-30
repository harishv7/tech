---
layout: post
title: Tutorial - Introduction to HTML (Part 2)
categories: [general, techstuff]
tags: [tech]
---

#Recap

In [part 1](http://harishv7.github.io/tech/general/techstuff/2015/09/20/Introduction%20to%20HTML%20P1.html), we covered the basics of HTML, the structure, declaring headings, paragraphs and adding images in a HTML file.

<hr>

# Introduction
In this section, we look at hyperlinks, making lists (ordered/unordered/nested), making comments, adding styles (fonts, colors, background color, bold, italics) & tables.

<hr>

# Hyperlinks
Hyperlinks are links such as [this](). These are the words or images you click to go to a new page! To link a word to point to another page/image etc., we can use the `<a>` tag.

A simple example will look like this:
````
	<a href="www.google.com">Google</a>
````

This translates into: <br>
<a href="www.google.com">Google</a>

Now when you click on "Google", it brings you right to Google's homepage. You can observe this by simply hovering your mouse on "Google". Your browser shows where the link points to at the bottom of the browser.

Hyperlinks come in handy when you need to redirect your users/viewers to another webpage.

<hr>

# Lists
Lists have mainly 2 forms: ordered and unordered. We can create an ordered (numbered) list of things in HTML by using the `<ol>` tag.
Similarly, we can create unordered(bullet) lists in HTML by using `<ul>` tag instead of `<ol>`.

*Example: Ordered List*
{% highlight html %}
<ol>
	<li> List point no. 1 </li>
	<li> List point no. 2 </li>
</ol>
{% endhighlight %}

This translates into: <br>

<ol>
	<li> List point no. 1 </li>
	<li> List point no. 2 </li>
</ol>


*Example: Unordered List*
{% highlight html %}
<ul>
	<li> List point no. 1 </li>
	<li> List point no. 2 </li>
</ul>
{% endhighlight %}

This translates into: <br>
<ul>
	<li> List point no. 1 </li>
	<li> List point no. 2 </li>
</ul>

We can also create nested lists. Simply, include your list inside the parent `<li>` tag. 

*Example: Nested Lists*
{% highlight html %}
<ul>
  <li>Vegetables</li>
  <li>Fruits
    <ul>
      <li>Apples</li>
      <li>Oranges</li>
	  <li>Pears</li>
    </ul>
  </li>
  <li>Snacks</li>
</ul>
{% endhighlight %}

will translate into:

<ul>
  <li>Vegetables</li>
  <li>Fruits
    <ul>
      <li>Apples</li>
      <li>Oranges</li>
	  <li>Pears</li>
    </ul>
  </li>
  <li>Snacks</li>
</ul>

Here, "Apples", "Oranges" and "Pears" are nested list items under Fruits.

<hr>

# Font Size, Colors, Families & Emphasis
It is boring to look at a website entirely presented in a same font like Times New Roman or Arial. Also, we can specify a certain font size for the words. We can change this font by using the `style` property. This property must be included within the tag (i.e. before closing the tag).

*Example: Font Size*
{% highlight html %}
<p style="font-size: 12px"> Your Paragraph here </p>
<p style="font-size: 30px"> Your Paragraph here </p>
{% endhighlight %}

translates to:

<p style="font-size: 12px"> Your Paragraph here </p>
<p style="font-size: 30px"> Your Paragraph here </p>

We now realise our entire output is in plain black and white. That's so boring. Let's add some colors now, with the `color` property. This is really simple and similar to the `font-size` property.

*Example: Font Color*
{% highlight html %}
<p style="color: blue"> Blue Paragraph here </p>
<p style="color: green"> Green Paragraph here </p>
{% endhighlight %}

And this gives us:

<p style="color: blue"> Blue Paragraph here </p>
<p style="color: green"> Green Paragraph here </p>

Apart from the font size and colors, to change the font-type, we use the `font-family` property. This is utilized in the same way as font-size.

*Example: Font-Family*
{% highlight html %}
<p style="font-family: Garamond"> Your Paragraph here </p>
<p style="font-family: Verdana"> Your Paragraph here </p>
{% endhighlight %}

translates to

<p style="font-family: Garamond"> Your Paragraph here </p>
<p style="font-family: Verdana"> Your Paragraph here </p>

Sometimes we need to highlight certain important information. Commonly, we use the bold and emphasis of words to highlight something important. To achieve this in HTML we use the `<strong>` and `<em>` tags for bold and italics respectively.
	
*Example: Text Emphasis*
{% highlight html %}
<p><strong>Hello There!</strong></p>
<p><em>Hello There!</em></p>
{% endhighlight %}

and this gives us:
<p><strong>Hello There!</strong></p>
<p><em>Hello There!</em></p>

To combine multiple properties, we simply use: `<p style="font-size:20px; font-family:Garamond;">Sample Paragraphy</p>`

which produces:

<p style="font-size:20px; font-family:Garamond;">Sample Paragraphy</p>

Simply, separate the various properties with the use of the semi-colon: `;`

There are many other properties that can be included such as color, font-weight etc. which will be covered under CSS which stands for Cascadin Style Sheets. CSS can simplify and is the professional method to style web elements.

<hr>

#Tables
We can add tables to our HTML code by using tables. To achieve this, we utilize `<table>`, `<th>`, `<tr>`, `<td>`. That may be a lot of tags, but it helps to structure our table nicely. `<tr>` refers to the table row, `<td>` refers to the table column and `<th>` refers to the row heading.

*Example: Tables*
{% highlight html %}	
<table>
  <tr>
  <th>Jack's Details</th>
  <th>Mary's Details</th>
</tr>
  <tr>
    <td>Jack</td>
	<td>Mary</td>
  </tr>
  <tr>
	  <td>Anderson</td>
	  <td>Smith</td> 
  </tr>
  <tr>
	<td>21</td>
    <td>24</td>
  </tr>
</table>
{% endhighlight %}

This gives us:

<table>
	<tr>
  <th>Jack's Details</th>
  <th>Mary's Details</th>
</tr>
  <tr>
    <td>Jack</td>
	<td>Mary</td>
  </tr>
  <tr>
	  <td>Anderson</td>
	  <td>Smith</td> 
  </tr>
  <tr>
	<td>21</td>
    <td>24</td>
  </tr>
</table>

If you look at what is being written, we can see that we define the table is a very structured way, row by row. The top row is the heading and uses the `<th>` tag. Subsequent rows (`<tr>`) uses `<td>` to indicate the details such as First Name, Last Name and Ages. The entire table is enclosed with the `<table>` and `</table>` tags which mark the start and end of the table respectively.

<hr>

With the above information, we can create a simple website! Here's a sample:

{% gist harishv7/414c2db23055af890658 %}

The output will look like this:
[Image](http://i.imgur.com/SmHrvHN.png)
