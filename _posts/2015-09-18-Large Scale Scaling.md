---
layout: post
title: Scalability for Web Applications
categories: [general, techstuff]
tags: [tech]
---

Attended Friday Hacks, which are hosted by [NUSHackers](http://nushackers.org/), where each week a guest speaker is invited to give talks on the latest tech developments etc. Today's talk was on scalability by [Ryan](http://ryandao.net/) from PayPal, who provided some good insights [1]. Personally, I am keen on web development and am currently working on some web applications as side-projects apart from university projects.

The first part of the presentation focused on measuring your web application's performance. Some great tools that were introduced include ApacheBench and [webpagetest](http://www.webpagetest.org/). 

The importance of latency was also stressed during the introduction. To understand latency, let's consider the scenario when someone from Singapore is accessing a web application hosted from the US. Here, we are concerned how fast can a packet be sent over? These packets typically are routed through several servers and poor cable networks before reaching you.

A key point on the things not to do was having too many JavaScript files. Simply don't have too many of these:
`<script src="myjsfile.js"></script> `

As a web development enthusiast myself, I could agree to this. Having multiple file references also means that more number of requests are being made to refresh/load these files. This can be simply minimised by unifying the separate files into one large file during deployment. Of course, minify them.

The second part introduced Amdahl's Law, which states:
> the speedup of a parallel algorithm is limited by the fraction of the problem that must be performed sequentially; that is, your design is only as strong as its weakest link. [2]


An example of a building evacution was given. For example, all the people in a building are evacuating a building through a single door. Ultimately, the entire evacuation process will be slowed down. However, compare it with having 2 doors (x2 faster) or an infinte number of doors (takes no time at all). 

This then brings the topic of instances of web applications. For example, having a single instance means that a single request received by the server is processed fully first, and then it moves onto the second difference.

In web development, it is crucial to consider both concurrency and parallelism. These are two of the most confused as being the same. Though not the same, they are related.

Simply put, concurrency is about *dealing* with many things at once (deals with the structure), while parallelism is about *doing* a lot of things at once (deals with the execution). Hence, concurrency is basically a way to structure a program by breaking it into pieces that can be executed independently [3]. The Go language, for example, is built with concurrency in mind [4].
Then we have asynchronous IO (AKA non-blocking IO) is a form of input-output processing that allows us to continue with other processing/actions before the current task has completed fully. Node.JS is an example of a JavaScript runtime environment that employs this technique.

The last part focuses on infrastructure. Today, the best ways for scaling without having to buy expensive bare metal servers, would be cloud hosting and deployment. For example, Netflix is hosted on Amazon Cloud, whereas GitHub employs hosting from bare metal physical servers. Cloud advancements have provided great scope for scalability.

A simple example is autoscaling (pre-requisite is having stateless apps). Autoscaling allows us to monitor resource exhaustion/redudance and spawn or kill as many instances as required by the situation. While this is cost-effective and resilient, it is also harder to test/debug/implement etc.

The above information and factors come in crucial when attempting to scale as your demand grows. I feel the advancement of cloud technologies and deployment is great and has provided us with an easy way to scale and monitor our apps. As compared to the past, where people had to purchase/set up/maintain huge bulky physical servers, this is so much more hassle-free.

---

##### The above content was delivered at NUS Friday Hacks on 18th Sep 2015. 

##### **References: [1](http://ryandao.net/), [2](http://www.embedded.com/design/mcus-processors-and-socs/4006486/What-Amdahl-s-Law-can-tell-us-about-multicores-and-multiprocessing), [3](http://blog.golang.org/concurrency-is-not-parallelism), [4](http://talks.golang.org/2012/waza.slide#10)**