---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /assets/intro.jpg
# some information about your slides (markdown enabled)
title: Software Development | Foundations
info: |
  ## Software Development | Foundations
# apply unocss classes to the current slide
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
---

# JavaScript - part 6/8
JavaScript Foundations
- [ ]  Explain differences between synchronous and asynchronous execution
- [ ] Event Loop and Callbacks
- [ ] Code asynchronous functions
- [ ] Handle errors

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
TODO: fill in anchor href above to point to github repo for these slides
-->

---
transition: slide-left
---

# Recap
(15 min) 

- recall functions input and output, callbacks (ex: in setTimeout)
- Challenge: use `contenteditable` on an h1 allowing text to be edited, then listen for appropriate event once text update is done 
- Challenge: create a todo list

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
- listen for events 'blur' and 'input'
-->

---
transition: slide-left
---

# Call Stack and the Event Loop
(30 min) What is the Event Loop?  

- JS is single threaded
- What is a stack? see [tire holder](https://images.homedepot.ca/productimages/p_1001062810.jpg?product-images=l)
- How a Call Stack works (analogy: Escape Room)
- Challenge: create a function called/calculates `factorial(x)` 
```js
debugger; // Keep your eye on the right side "Call Stack"
function puzzle2() {
  console.log('unlocked puzzle2') // error: console.log(person.name.first);
}

function puzzle1() {
  puzzle2(); // infinite loop error: puzzle1()
  console.log('unlocked puzzle1')
}

puzzle1()
```

<!--
-->

---
transition: slide-left
---

# Synchronous Functions
(10 min) 

- Synchronous functions
   - Create 3 functions with different `setTimeout()`
   - Make them happen one after the other and log something in the console

```js
// Note: JS is asynchronous by nature, so we're faking synchronous behaviour
function puzzle3() {
  setTimeout(() => {
    console.log("puzzle3 done");
    console.timeEnd();
  }, 3000);
}

// insert functions puzzle1 and puzzle2 here

console.time();
puzzle1();
```

<!--
function puzzle1() {
  for (let i = 0; i < 1000000000; i++) {
    if (i === 999999999) console.log(i);
  }
}

puzzle1(); puzzle1(); puzzle1();
-->

---
transition: slide-left
---

# Callback hell
(5 min) If you were to refactor last slide to use anonymous functions, it would look like:

```js
// sideways Christmas tree pattern 
function puzzle1() {
  setTimeout(() => {
    setTimeout(() => {
      setTimeout(() => {
        console.log("puzzle3 done");
      }, 3000);
      console.log("puzzle2 done");
    }, 3000);
    console.log("puzzle1 done");
  }, 3000);
}

puzzle1();
```


---
transition: slide-left
---

# Asynchronous Functions
(35 min) Tim Hortons analogy: Have you ever waited in line, ordered, only to have your food served after the person behind you got theirs served first?  (See [Loupe](http://latentflip.com/loupe/?code=JC5vbignYnV0dG9uJywgJ2NsaWNrJywgZnVuY3Rpb24gb25DbGljaygpIHsKICAgIHNldFRpbWVvdXQoZnVuY3Rpb24gdGltZXIoKSB7CiAgICAgICAgY29uc29sZS5sb2coJ1lvdSBjbGlja2VkIHRoZSBidXR0b24hJyk7ICAgIAogICAgfSwgMjAwMCk7Cn0pOwoKY29uc29sZS5sb2coIkhpISIpOwoKc2V0VGltZW91dChmdW5jdGlvbiB0aW1lb3V0KCkgewogICAgY29uc29sZS5sb2coIkNsaWNrIHRoZSBidXR0b24hIik7Cn0sIDUwMDApOwoKY29uc29sZS5sb2coIldlbGNvbWUgdG8gbG91cGUuIik7!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D))
- Asynchronous functions
   - Create previous 3 functions but make them asynchronous
   - Show the time it takes overall
- Challenge: Yes/No Api

```js
function puzzle3() {
  setTimeout(() => {
    console.log("puzzle3 done");
    console.timeEnd();
  }, 3000);
}

// insert puzzle1() puzzle2() here

console.time();
puzzle1();
puzzle2();
puzzle3();
```


<!--
- demo yes no api using Promises, then async/await
-->


---
layout: image-right
transition: slide-left
image: /assets/jake.png
backgroundSize: 500px 400px
class: text-left
---

# 10 minute break

🍦 Cool Tips, Trends and Resources:

- 💡 [App Idea Generator](https://appideagenerator.com/)
- 🧠 [App Ideas](https://github.com/florinpop17/app-ideas?tab=readme-ov-file)
- ➿ [Event Loop, Tasks, Microtasks...](https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/)
- ▶️ [What the heck is the event loop anyway?](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
- ➰ [Event Loop](https://dev.to/nodedoctors/an-animated-guide-to-nodejs-event-loop-3g62)
- ☎️ [Callbacks](https://www.w3schools.com/js/js_callback.asp)
- 🥞 [Call Stack](https://www.youtube.com/watch?v=Q2sFmqvpBe0)
- 📊 [Web Almanac - state of JS](https://almanac.httparchive.org/en/2024/javascript?utm_source=convertkit&utm_medium=email&utm_campaign=Syntax%20Snack%20Pack:%20React%20Trends%20in%202025%20-%2016985243)
- 🌮 [Event Delegation](https://www.youtube.com/watch?v=YL1F4dCUlLc)
<hr>

- 🧪 [Enter anonymous lab questions](https://docs.google.com/forms/d/e/1FAIpQLSevvGARdHQikso-uLqFCO481MABKE5HofuSrlzEPMNQ2ZLykw/viewform?usp=dialog)
- ℹ️ [Course feedback survey](https://circuitstream.typeform.com/to/ZoyYk7px#course_id=SoftwareAN&instructor=9514)

<!-- 
- take attendance
-->

---
transition: slide-left
---

# Handling errors
(15 mins)  How to code for exception handling

- How to use `throw` statements for error handling
- How to use `try...catch` statements to have a default function in case of errors

<!--
- errors can occur because invalid input, failed network requests, or the unexpected 
- good to be graceful in error handling, ensuring app doesnt crash
-->

---
transition: slide-left
---

# Exercise
(remainder of time)  

- Challenge: Weather App
- Goto: https://www.weatherapi.com/api-explorer.aspx#forecast

<!--
-->


---
transition: slide-left
---
# Group Exercise / homework:
Describe in pseudocode (English words) all the things you need to do in JavaScript to make this happen

<img src="/assets/weather.png" alt="weather app" style="height: 400px">