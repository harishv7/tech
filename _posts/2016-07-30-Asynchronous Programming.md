---
layout: post
title: Asynchronous Programming in Node.JS
categories: [general, techstuff]
tags: [tech, javascript, node]
---

Let's imagine a restaurant reservation application where 10 people are trying to book at the same time. It will be really inconvenient if the 10th person has wait for the 9 others to finish their bookings first. The database calls can take considerable amount of time. With asynchronous programming, we can run multiple requests at the same time. 

Instead of running things one by one, we can use the concepts of callbacks and promises to have our code to do something while something else is happening. For example, when one user has submitted his booking, while this request is being processed on the backend, the web application can service another request from the next user.

A simple demo:

Let's consider this program (app.js):

{% highlight javascript %}
console.log("ONE");
console.log("TWO");
{% endhighlight %}

Running this with `node app.js` will print this:

{% highlight javascript %}
ONE
TWO
{% endhighlight %}

Let's replace this code in `app.js` with:

{% highlight javascript %}
setTimeout(function() {
	console.log("ONE");
}, 1000);
console.log("TWO");
{% endhighlight %}

Running this now prints:

{% highlight javascript %}
TWO
ONE
{% endhighlight %}

This demonstrates asynchronous programming with callbacks. The function inside setTimeout is the callback function after the 1000 milliseconds have passed. During this 1000 milliseconds, the program continues on to execute the next instruction which is to log "TWO" to the console.