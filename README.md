# Fitness Tracker Project - Week 1

Over the course of the next few weeks, you'll be building a fitness tracker app. You'll be able to add *workouts*, which include a list of *exercises*. An analytics panel will give you a breakdown of your workouts, including the number of minutes you've worked out, the exercise you've spent the most time doing, and the percentage of workouts you've completed so far.

This week, you're given a mockup of what we want the front-end to look like. Your job is to create the HTML, CS, and JS so that it looks more or less like this:

![Fitness Tracker Pro Mockup](https://user-images.githubusercontent.com/1832043/53041454-a959c380-3449-11e9-90b2-52d98a9d99e4.png)

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

At the top of your GitHub repository click on the Settings tab, and scroll down until you see the GitHub Pages section, which should look like this:

![GitHub Pages Settings](https://user-images.githubusercontent.com/1832043/53041923-c17e1280-344a-11e9-9309-5e2216231756.png)

Now click the dropdown under Source and select the first option, master branch. Hit Save.

You should now be able to visit the repo at `https://YOUR_GITHUB_USERNAME.github.io/Fitness-Tracker-Week1/`

But wait! It looks like it's serving our README file instead of our HTML page.

Go ahead and visit `https://YOUR_GITHUB_USERNAME.github.io/Fitness-Tracker-Week1/public/`, and you should see your HTML page. But this isn't ideal. We don't want visitors to have to go to that public directory every time. And they don't need to read our README file.

Git to the rescue! We can tell Git to create a special branch that *only* has the public directory in it. Then tell GitHub Pages to publish that special branch.

Head on back to the terminal, and run the following command:

`git subtree push --prefix public origin gh-pages`

Once that finishes, go look at the repository on GitHub and checkout the newly created branch:

![Switch Branches on GitHub](https://user-images.githubusercontent.com/1832043/53046147-060eab80-3455-11e9-98ca-a1c5baab21ab.png)

From the point of view of this `gh-pages` branch, everything in the public directory is moved up to the root of the repo! Now, all we need to do is tell GitHub Pages to publish this branch instead of `master`:

![Set GitHub Pages branch](https://user-images.githubusercontent.com/1832043/53046350-71f11400-3455-11e9-9033-2eb4bdc40765.png)

It might take as long as a minute for the changes to take effect (deployment isn't always a speedy process). But you should soon be able to see your HTML page at `https://YOUR_GITHUB_USERNAME.github.io/Fitness-Tracker-Week1/` Hooray!

![Squidward Hooray](https://media.giphy.com/media/l0HlTUsy3ZOuDSQtG/giphy.gif)

Now, whenever we want to deploy our website to the real live web, we'll commit our changes enter `git subtree push --prefix public origin gh-pages`. Hmmm, that...might get a little tedious.

Instead, let's take this command (which we expect to use pretty frequently) and save it as an npm script. Edit your `package.json` file to include the following a "deploy" npm script, like so:

```json
"scripts": {
  "start": "live-server public",
  "deploy": "git subtree push --prefix public origin gh-pages"
},
```

[NPM Scripts](https://docs.npmjs.com/cli/run-script) are a really handy way to store commands that you expect to use frequently, or that you want your collaborators to be able to use.

Back on the terminal, type `npm run deploy` and watch the deployment process kick off just as before! Now we won't have to remember the special git command each time.

## Layout and Styles

From here on out, your job is to iteratively make the webpage look reasonably like the mockup above. Remember to diagram out the box model for your webpage.

