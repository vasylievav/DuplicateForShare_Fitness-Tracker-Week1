# Fitness Tracker Project - Week 1

Over the course of the next few weeks, you'll be building a fitness tracker app. You'll be able to add *workouts*, which include a list of *exercises*. An analytics panel will give you a breakdown of your workouts, including the number of minutes you've worked out, the exercise you've spent the most time doing, and the percentage of workouts you've completed so far.

This week, you're given a mockup of what we want the front-end to look like. Your job is to create the HTML, CS, and JS so that it looks and behaves more or less like this:

[INSERT_MOCK_UP_HERE]

In addition, we'll get some practice deploying a website, so that anyone on the web can go to the URL and see our work. GitHub Pages is a great, free to start deploying webpages, and that's what we'll be using today.

![Cool Internet Kid Thumbs Up](https://media.giphy.com/media/XreQmk7ETCak0/giphy.gif)

Ready? Let's get started!

## Getting Started

If you haven't done so already, fork this repo to your own account. Your address bar should look like this:

`https://github.com/YOUR_GITHUB_USERNAME/Fitness-Tracker-Week1`

Great! Now clone this repository to your computer (`git clone https://github.com/YOUR_GITHUB_USERNAME/Fitness-Tracker-Week1`) and open it up in your editor of choice. Take a look around.

This project has a  `package.json` file. That's where we keep track of information like "what dependencies does this project need?" and "what scripts can we run for this project?". There's only one dependency here, namely `live-server`. From our terminal, we can run the command `npm start`, which uses live-server to serve whatever is in the public directory.

Speaking of that public directory, take a peak inside. Notice the `index.html` file. That's the **root of our webpage**. If we were to host our website on `mycoolhost.com`, any user that fired up a browser and went to `http://mycoolhost.com/` would be served this `index.html` file (they don't need to specify `http://mycoolhost.com/index.html` -- it is served by default).

First things first: let's serve the webpage locally. Install project dependencies (`npm install`), and then run the start script (`npm start`). If your browser didn't automatically open to the localhost, go there now (it ought to be served from http://127.0.0.1:8080). You should see content that matches what's in the `index.html` file. Now add something flashy to the HTML (something like a `<h1>Hello, World!</h1>` in the body) and save the changes. If `live-server` is working correctly, it should appear automatically.

> NOTE: Using `live-server` is handy, but using it is **completely optional for this exercise**. If you prefer, you're welcome to just open up the public directory in your browser, and refresh manually.

## Deployment

Now, before we really start developing our UI, let's get our website published on the interwebz. GitHub Pages lets us do this for free, and all we have to do is tell it which git branch to keep an eye on.

# TODO
