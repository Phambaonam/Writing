# Charting the Stock Market with React
[<img src="https://images.unsplash.com/photo-1504197618732-93c3d955d927?dpr=2&auto=format&fit=crop&w=1199&h=799&q=80&cs=tinysrgb&crop=">](
https://unsplash.com/photos/a6z2tYFEjR8)
Photo by peggy pardo on Unsplash - https://unsplash.com/photos/a6z2tYFEjR8

Once again I was working on an app from the [FreeCodeCamp curriculum](https://www.freecodecamp.org/challenges/chart-the-stock-market). In this article you can read the full documentation on the building process. 
Enjoy


[➡️ Github Repo is available here ⬅️](https://github.com/DDCreationStudios/ChartTheStockMarket)


## 📄 Table of contents


---
>“Failure isn’t a necessary evil. In fact, it isn’t evil at all. It is a necessary consequence of doing something new.” 
― Ed Catmull
---

## The challenge 

See the full challenge [here](https://www.freecodecamp.org/challenges/chart-the-stock-market).

The user stories are pretty simple: 

- I can view a graph displaying the recent trend lines for each added stock.
- I can add new stocks by their symbol name.
- I can remove stocks.
- I can see changes in real-time when any other user adds or removes a stock. For this you will need to use Web Sockets.

It looks like this:

<img src="http://g.recordit.co/RlH1aQ7o9Q.gif" alt="gif"/>

## Roadmap

I learned from [my last full-stack app](https://github.com/DDCreationStudios/Writing/blob/master/articles/LearningsFirstFullStack.md) that starting with the backend can induce some issues when you are working on the frontend later on. Therefore this time I will start with the frontend and finish with the backend.

1. Setup the environment with create-react-app
2. Lay out the basic React component structure
3. Set up the Redux eco system
4. Work over all components, divide them into container components and wire everything up with the Redux store
5. Build the Chart component with React-Vis
6. Build the backend using socket.io
7. Deploy to Heroku

## Frontend

I will only highlight the key cornerstones and not provide a step-by-step tutorial.

#### Setup with the [create-react-app package](https://github.com/facebookincubator/create-react-app)

This time I wanted to use this boilerplate because I have used it many times before but never on a full-stack project. Although it has some limitations with the pre-configured structure, the benefits outweigh the problems by a mile. 

Basically it provides an environment, that: 

- React, JSX, ES6, and Flow syntax support.
- Language extras beyond ES6 like the object spread operator.
- A dev server that lints for common errors.
- Import CSS and image files directly from JavaScript.
- Autoprefixed CSS, so you don’t need -webkit or other prefixes.
- A build script to bundle JS, CSS, and images for production, with sourcemaps.
- An offline-first service worker and a web app manifest, meeting all the Progressive Web App criteria.

Pretty early actually I came to the point where I had to eject the configuration ( = opening the environment configuration for changes) to modify the webpack config. 

The problem was that I wanted to add jQuery for Materializecss and there always were some troubles. 
Solutions:
- Import jquery in ES6: https://stackoverflow.com/questions/37213647/es6-code-not-working-with-jquery
- Provide jquery plugin in webpack config: https://github.com/erikras/react-redux-universal-hot-example/issues/596

#### React, Redux, React-vis

This time I wanted to use [react-vis](https://github.com/uber/react-vis) for visualizing the chart. It is a visualization library based on D3 and developed by Uber. To summarize and quote their docs:

> A collection of react components to render common data visualization charts, such as line/area/bar charts, heat maps, scatterplots, contour plots, pie and donut charts, sunbursts, radar charts, parallel coordinates, and tree maps.

Some notable features:

- Simplicity. react-vis doesn't require any deep knowledge of data visualization libraries to start building your first visualizations.
- Flexibility. react-vis provides a set of basic building blocks for different charts. For instance, separate X and Y axis components. This provides a high level of control of chart layout for applications that need it.
- Ease of use. The library provides a set of defaults which can be overridden by the custom user's settings.
- Integration with React. react-vis supports the React's lifecycle and doesn't create unnecessary nodes.

Some practical issues I came across and solved were:

- Make react-vis chart responsive: https://github.com/uber/react-vis/issues/262
- To use gradients in react-vis properly, make sure tu include them in the Plot and adapt the reference points: http://uber.github.io/react-vis/#/documentation/general-principles/colors
- Use LineSeries instead of LineMarkSeries for better performance: http://uber.github.io/react-vis/#/documentation/series-reference/line-series

___
At this point the app was already pretty nice. Now I had to check the last User Story, which is to display real-life changes using a "web socket" backend.
___

## Backend


## Useful links & credits
- [📄 "Begin"](afgafgadgads)



Thanks for reading my article! Feel free to leave any feedback! 


<!-- Written by Daniel Deutsch (deudan1010@gmail.com) -->
