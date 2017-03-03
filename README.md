# Lodash Discovery - Car Mileage Estimation

### Directions

Write your own interpretation of _.each, _.map and _.reduce from the Lodash library: https://lodash.com/

### Process

Each interpretation of a Lodash method in this exercise supports the end goal of estimating a car's mileage based on manufacturing year.

I started by studying the documentation for each Lodash method. I was aware that Lodash is a library somewhat similar to Underscore.js, but I haven't used Lodash very often in projects. I intentionally try to use native JavaScript as much as possible to reduce project dependencies and ensure that my knowledge of JavaScript fundamentals remains current.

First I wrote out each Lodash method and checked it in the browser. I then created an array of objects based on the solar system, but quickly decided to switch from planets to cars. I wanted to complete the exercise using integers, and didn't think order from the sun, number of moons, or number of rings would result in a creative solution that someone might find useful in everyday life.

### Solution

._each - I gathered a collection of DOM nodes (cars in an unordered list), then looped through each car and performed methods and functions to extract each car's manufacturing year from a string (before pushing each year into an array). I also included the setTimeout method because ._each takes a function as a second argument. If I apply a JavaScript framework to this exercise in the future (like React or Angular), I could use setTimeout for notifications or alerts.

._map - I found ._map to be somewhat challenging because I needed to iterate on an array, leave the existing array intact, and return a new array. I also needed to invoke a separate function on each iteration. At first it was difficult, but the difficulty was resolved when I realized I needed to bind the value of 'this' before passing an object to the callback function. The callback function finds the difference between a car's manufacturing year and the current calendar year, then multiplies the difference by 12,000 (the average number of miles added to a car per year in the USA).

._reduce - This method came more naturally to me. I wrote reduce in native Javascript, then quickly figured out how to iterate on each mileage estimation to produce a total mileage sum for all three DOM nodes (cars).

