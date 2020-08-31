---
layout: post
title:      "How to make a fetch request for your index!"
date:       2020-08-31 04:04:57 +0000
permalink:  how_to_make_a_fetch_request_for_your_index
---


Starting a this project, I was so stressed. I didn't know how to start it, I was overwhelmed, and I had no idea how to even see if my Ruby backend was communication with my JavaScript frontend. Once I created my files, I just started small. An index functions is a great place to start. Not only does it confirm your backend and frontend are communicating, but it also makes you feel like you are a "real developer". The amount of onvidence I had after I displayed my index to the dom was astounding. Now, enough about me. Let's get coding!

First, you are going to want to make sure no functions run until the DOM is loaded. I'm definitely a "write the code you want" type of person, so I decided to just add my function in, even though I havent defined it yet. I know my fetchDogs()(aka index funtion) function is going to be in my dogsAdapter file. So I went ahead and defined it as follows.

![](https://imgur.com/7E107zQ)

![](https://imgur.com/n9r2Jw1)


In my constuctor, I defined a base url. You are going to chose the url from your server that contains all of your objects. The object I am using is dog so my URL will be "http://127.0.0.1:3000/dogs". Next, you are going to define your fetchDogs() function. In this function you are going to (remember to open up your console to see where your objects exist. they may not exist in .data or .attributes):
1) fetch the URL
2) turn the response into json
3) iterate over the elements that were fetched
4) with each element you are going to attach it to the dom

![](https://imgur.com/CzpuO30)

In my index.html, I created a div class with the id of 'dogs-list'. I defined that as a constant in my constuctor. I also defined all my other properties. 

![](https://imgur.com/zfTBuzb)

Now, let's define attach to DOM and fullRender. We are going to get our dogList and append it to the DOM using fullRender(). In fullRender(), we are going to take the innerHTML of the element and add all of the attribtes using HTML.

![](https://imgur.com/jL5LhNE)

Now, BOOM. You have a functional index page.



