---
layout: post
title:      "How to start a basic Sinatra Web Application "
date:       2020-06-29 05:55:15 +0000
permalink:  how_to_start_a_basic_sinatra_web_application
---

Going into this project, I was a lot less nervous than going into the Ruby CLI project. When I started this basic Sinatra application, I felt confident. I had set up Sintra projects at least three times prior, so I didn't feel like I was going in blind. Because I understand the struggle of not knowing how to start a project, I will give you some pointers. 

First, you are probably going to want to come up with an idea.  This isn't something to take lightly. You want to build something you are excited and passionate about or you won't be motivated to complete the project. Think about things outside of coding that make you motivated. What do you do in your free time? What makes you happiest? What are some life problems you, big or small, can solve with this simple web application?

I'm passionate about photography. I also love the community that comes with it! Everyone, for the most part, really loves helping each other out. But one thing I always struggled with is finding the perfect outdoorsy location. My app,  [Adventure Awaits](https://github.com/kikuishimoto/adventure-awaits),  is a basic Sinatra application where users can post their favorite adventure photography locations. 

This is your time to shine, and it's your time to build something you can be proud of. 

After you have gotten your idea, you are going to want to install the [corneal gem](http://thebrianemory.github.io/corneal/). Through the magical powers of the gem, it will create a whole Sinatra application just for you. 

In Sinatra, we set up our projects using an MVC model. This stands for Models, Views, and Controllers. The models will inherit from ActiveRecord::Base and be the home for our database. The controllers will decide our URLs and what each URL does. It will also save information the client inputs to the proper database. The views folder controls what the user sees using HTML. They can display forms, create a header, and even incorporate some CSS!

Next, you are going to want to figure out your models and their relations to each other. I had a User model that has-many adventures, and I have an Adventures model that belongs-to a user. Set up your corresponding controllers. Make sure to create your table and Boom! The base of your project is all set up! Now all you have to do is code your controllers and views.
![](https://drive.google.com/file/d/1YP_SMbLp5PH7ylWVAOyq1tf5vwlml_0r/view?usp=sharing)
![](https://drive.google.com/file/d/1-2lqBtPMIyPeRF5a_KYgT_vvNjsOWJEv/view?usp=sharing)


Extra notes about the controllers:
You are going to want to enable sessions, set a session_secret, and set method_override to true. 
You'll also want some helper methods that will help you determine if a user is logged in or not. This will come in handy when you are making sure a user can not edit another user's post and some other things too.
![](https://drive.google.com/file/d/1YGncZMdVw-4WfYA_QVGpWx4l2TGHvXWs/view?usp=sharing)

You can check out my project [here](https://github.com/kikuishimoto/adventure-awaits).


