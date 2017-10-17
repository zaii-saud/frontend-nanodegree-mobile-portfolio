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

##### PageSpeed Insights Score
Before optimization:
Mobile  75
Desktop 86

After optimiztion:
Mobile  96
Desktop 97


#### Part 2: Optimize Frames per Second in pizza.html

* Changed all the query selectors to get element by ID or class as needed
* Moved variable definitions outside the loops if their value is not affected by the loop
* Minimized number of generated sliding pizzas based on screen size

##### Sample Output

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
