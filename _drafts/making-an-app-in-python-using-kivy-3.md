---
layout     : post
title      : "Making an App in python using Kivy - Part 3 - Screen Manager"
categories : tutorial
tags       : blog python kivy
author     : Timothy
comments   : false
---

In the [first part][part1] I talked about how to create an app. In the 
[second part][part2] I talked about the some of different widgets that can be
used in Kivy, that I found helpful. 

Now I am going to explain how I used the [screen manager][smanager] to help me
create the app. Some of this is repeated from part 2. 

The reason for using the screen manager was because I found that I needed to
have a way of switching between different layouts of the widgets within the
app. This could have been achived by altering the widget tree, however this can
very easily get messy and misakes were easy to be made. As is state on the 
[widgets][widgets] help page:

```
Warning
Never manipulate the children list yourself, unless you really know what you 
are doing. The widget tree is associated with a graphic tree. For example, if 
you add a widget into the children list without adding its canvas to the 
graphics tree, the widget will be a child, yes, but nothing will be drawn on
the screen. Moreover, you might have issues on further calls of add_widget,
remove_widget and clear_widgets.
```

There is an alternate to using screen manager which is the [carousel][carousel]
widget. I am not going to talk about this as I don't feel its as flexiable as
the screen manager.

Firstly the widgets that you add to the screen manager are called screens. 


[part1]: {% post_url 2015-01-16-making-an-app-in-python-using-kivy-1 %}
[part2]: {% post_url 2015-01-28-making-an-app-in-python-using-kivy-2 %}
[carousel]: https://kivy.org/docs/api-kivy.uix.carousel.html
[smanager]: https://kivy.org/docs/api-kivy.uix.screenmanager.html
[widgets]: https://kivy.org/docs/guide/widgets.html
