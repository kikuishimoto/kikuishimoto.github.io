---
layout: post
title:      "Sessions Controller. What is it and how do you use it?"
date:       2020-08-06 02:15:45 +0000
permalink:  sessions_controller_what_is_it_and_how_do_you_use_it
---

A Sessions controller is the controller a program uses to control logins, logouts, and omniauth. In my project My Trail, I used the sessions controller to help my manange my sessions. In a nutshell, a session is a group of interactions from a user with a website that takes place within a specific time frame. It heps maintain a user specific state. Rails provides a sesison object for each user that accesses the application. 

First, create a sessions controller under your controller file and ake sure in inherits from ApplicationController.

![](https://imgur.com/trS31if)

Next, define your new method.

![](https://imgur.com/trS31if)

Nothing has to exist in your new method, just make sure you have a login form in your sessions.html.erb file that should exist in your views folder.

![](https://imgur.com/MKpFUIi)

Make sure you create your routes. Your get request will route to sessions#new while your post request with route to sessions#create. Also, go ahead and create your destroy route while we are here. I also made custom URLS for my new, create, and destory methods because I wanted my URL to match what my application was actually doing.

![](https://imgur.com/h8CBelB)

Next, you have to make your create method in SessionsController. This method is going to find the user by te given username, its going to make sure the user exists and authenticate the password/username combination. If the user does exist and the password is authenticated, it is going to set the session[:user_id] to the user.id and redirect to the trails index page. If it doesnt, then its going to flash an alert and redirect to the login page. 

![](https://imgur.com/QYjPMrG)

Well, we also need a way for ou users to log out. We are going to define a method called destroy. This method is going to destoy the session and redirect to the welcome or home page. 

![](https://imgur.com/KfwQ13W)


BOOM. You did it. You sucessfully built a simple login and logout method. 
