# Lodash Discovery - Vehicle Mileage Estimation

### Directions

Write your own interpretation of _.each, _.map and _.reduce from the Lodash library: https://lodash.com/

### Process

Each interpretation of a Lodash method in this exercise supports the end goal of estimating total mileage for a collection of vehicles.

I started by studying the documentation for each Lodash method. I was aware that Lodash is a library similar to Underscore.js, but I haven't used Lodash very often in projects. I intentionally try to use native JavaScript as much as possible to reduce project dependencies and ensure that my knowledge of JavaScript fundamentals remains current.

First I wrote each Lodash method and checked it in the browser. My first idea was to create an array of objects based on the solar system. I then decided to switch from planets to vehicles. The reason for this decision was that I wanted to complete the exercise using integers, and quantifiable data about planets (number of moons, distance from the sun, number of rings, etc.) might not result in a creative solution that's useful in everyday life.

### Solution

._each: I gathered a collection of DOM nodes (vehicles in an unordered list), then looped through each vehicle and performed methods and functions to extract each vehicle's manufacturing year from a string (before pushing each year into an array). I also included the setTimeout method because ._each takes a function as a second argument. If I apply a JavaScript framework to this exercise in the future (such as React or Angular), I could use setTimeout for user notifications or alerts.

._map: I found ._map to be somewhat challenging because I needed to iterate on an array, leave the existing array intact, and return a new array. I also needed to invoke a separate function on each iteration. At first it was difficult, but the difficulty was resolved when I realized I needed to bind the value of 'this' before passing the value to a callback function. The callback function finds the difference between a vehicle's manufacturing year and the current calendar year, then multiplies the difference by 12,000 (the average number of miles added to a vehicle per year in the USA).

._reduce: This method came more naturally to me. I wrote a native JavaScript reduce method based on each vehicle's year of manufacture, then quickly figured out how to iterate on each annual mileage estimation per vehicle. The result was a total mileage estimate for all three DOM nodes (vehicles).

