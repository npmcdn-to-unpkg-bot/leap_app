# Leap News App

## Overview

The goal of this app, as my final project while during Immersive Course at General Assembly, was to experiment with the [Leap Motion Controller](https://www.leapmotion.com/) in a web environment. 

The app allows the user to browse RSS news feeds from the ABC* with the use of a Leap Motion controller. The user interacts with their hand to browse a feed though an image carousel gallery. 

The user can 'swipe' left and right to cycle though the gallery and read the blurb of the article. 

A 'tap down' gesture changes the RSS news feed and removes the carousel galleries content and load the next feed content. A 'screen touch' gesture sends the user to the article. 

And a 'down swipe' adds the article to the users Pocket account.

*The RSS feeds from the ABC are used in this case because it seems to be one of the few RSS news feeds that come with image links.

[Live Demo](http://fyrdmen.github.io/leap_app/)
Demo requires the use of A leap Motion controller.

## How it works

The app works by retrieving the RSS feeds from the ABC using the google RSS api, loads the feed into a carousel gallery using flickity.js and always the user to save the article to Pocket by a simple plugin. Each time a gesture is used to select the next article image is cycled through and the blur, along with the title and data is  update with jQuery. Velocity.js is used to add animation feature to the flickity.js gallery.

With the use of Leap.js, the app runs a event loop to continually monitor the data coming from the Leap controller and runs comparisons on a snippet of data to detect if a gesture has been made and which gesture it is.

When the user triggers the next RSS feed the image data for that feed is removed from the carousel and the new feed image data is appended.

## Features

+ Control an imagery gallery casserole with left and right swipe gestures
+ Cycle RSS news feed with down tick
+ Go to article with screen touch gesture
+ Add to Pocket with swipe down gesture
+A FaceBook like feature was removed because the gesture to trigger the event was too sensitive and users would trigger it inadvertently.

## Technologies

+ [A Leap Motion Controller]9https://www.leapmotion.com/)
+ [Flickity.js](http://flickity.metafizzy.co/)
+ [Leap.js](https://github.com/leapmotion/leapjs)
+ [velocity.js](http://julian.com/research/velocity/)
+ HTML
+ CSS3
+ JavaScript, including
  - jQuery

+ API
  - [Google RSS Api](https://developers.google.com/feed/?hl=en)

+ Deployment: GitHub Pages

