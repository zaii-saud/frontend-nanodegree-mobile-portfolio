## Zainab's Website Performance Optimization portfolio project

Here is a description of what I did to optimize this project.

#### Part 1: Optimize PageSpeed Insights score for index.html

* Got rid of the Google font, which did noting but slow down the page
* Inlined the critical css to reduce calls
* Got a minimized version of the css for the rest of it and added a script to the end to handle it using [sitelocity](https://www.sitelocity.com/critical-path-css-generator) that helps determine the critical css
* Loaded Google analytic script asynchronously
* Inlined perfmatters.js and loaded it asynchronously as well
* Made another version of th pizzeria picture in the needed size 100 px to use in index.html
* Compressed profile picture
* Minified the HTML file using (https://www.willpeavy.com/minifier/)

#####PageSpeed Insights Score
Before optimization:
Mobile  75
Desktop 86

After optimiztion:



#### Part 2: Optimize Frames per Second in pizza.html

* Changed all the query selectors to get element by ID or class as needed
* Moved variable definitions outside the loops if their value is not affected by the loop
* Minimized number of generated sliding pizzas based on screen size

#####Sample Output

Before optimiztion:

main.js:480 Time to generate pizzas on load: 14.440000000000012ms
main.js:493 Average scripting time to generate last 10 frames: 44.013000000000005ms
main.js:465 Time to resize pizzas: 171.48000000000047ms
main.js:465 Time to resize pizzas: 183.84000000000015ms
main.js:465 Time to resize pizzas: 262.6800000000003ms

After optimiztion:

Time to generate pizzas on load: 9.174999999999955ms
main.js:516 Average scripting time to generate last 10 frames: 2.713500000000033ms
main.js:516 Average scripting time to generate last 10 frames: 0.13599999999999ms
main.js:516 Average scripting time to generate last 10 frames: 0.10399999999992815ms
main.js:516 Average scripting time to generate last 10 frames: 0.12300000000009277ms
Time to resize pizzas: 0.7899999999999636ms
2main.js:488 Time to resize pizzas: 0.5649999999995998ms



-------------------------------------------
Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
