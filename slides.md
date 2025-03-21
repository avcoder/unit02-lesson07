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

# JavaScript - part 7/8
JavaScript Foundations
- [ ] Use APIs to leverage dynamic data
- [ ] Handle data in JSON format
- [ ] Use Postman tool
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
(30 min) 

- recall asynchronous functions
- localStorage
- Challenge: create search input box to search for cities, show dropdown suggestions that filter city name based on key stroke...
   - ...After selecting the city, add a marker to leaflet map

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
- mention jQuery's role
-->

---
transition: slide-left
---

# Dynamic Data, APIs and REST
(40 min)

- Why is dynamic data important for software development?
- Why do websites need to connect to each other?  What problems need to be solved in doing so?
- How does the web work?   
- What is RESTful architecture and how do computers use it to communicate?
- Intro to HTTP methods (GET, POST...) and Status Codes (200, 404...)
- Challenge: recreate email inbox using [PureCSS template](https://pure-css.github.io/layouts/)

<!--
-->

---
transition: slide-left
---

# Postman, Make an API request
(30 min) 

- What is Postman?  (Alternatives: Insomnia, Hoppscotch, Bruno)
- Main format to get responses include: JSON, XML, CSV
- Exercise: Use Postman to request from [Giphy API](https://developers.giphy.com/docs/api/) to search for gifs.  (Show Promise way, then show async/await)
- Challenge: Create a webpage that searches gifs fetching from same API
   - once gif selected, insert text to create a meme, then save it as an image

<!--
-->

---
layout: image-right
transition: slide-left
image: /assets/cj.png
backgroundSize: 500px 400px
class: text-left
---

# 10 minute break

🍦 Cool Tips, Trends and Resources:

- ▶️ [Format: Dates Numbers Durations](https://www.youtube.com/watch?v=DyHXvcX0BGQ)
- 😸 [Cat API](https://thecatapi.com/)
- 🤖 [Avatar APIs](https://medium.com/nocodeshift/5-best-user-avatar-apis-saas-project-4bcac393220d)
- 🎲 [Hoppscotch (Postman alternative)](https://github.com/hoppscotch/hoppscotch)
- 👹 [JSON](https://www.json.org/json-en.html)
- 👀 [JSON cheatsheet in LMS](https://courses.circuitstream.com/d2l/le/lessons/9514/topics/49781)
- 🚩 [Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status)
- ▶️ [APIs for Beginners](https://www.youtube.com/watch?v=WXsD0ZgxjRw&t=290s)
- 🔋 [MDN Generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)

<br>
<hr>
<br>

- 🧪 [Enter anonymous lab questions](https://docs.google.com/forms/d/e/1FAIpQLSevvGARdHQikso-uLqFCO481MABKE5HofuSrlzEPMNQ2ZLykw/viewform?usp=dialog)
- ℹ️ [Course feedback survey](https://circuitstream.typeform.com/to/ZoyYk7px#course_id=SoftwareAN&instructor=9514)

<!-- 
- take attendance
-->

---
transition: slide-left
---

# JSON + Handling errors
(30 mins)  Intro to JSON

- Why is JSON widely used?
- JSON is not JavaScript
- JSON Format
- Parsing JSON
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

- Use this [Joke API](https://official-joke-api.appspot.com/random_joke) to display the question, then upon clicking a button, displays the punchline
- Stretch goal: Create a new button that fetches a new joke; Accumulate jokes in an unordered list below current joke

---
transition: slide-left
---

# Homework

- Work on Assignment 2 due Apr. 13
- There are 3 exercises in LMS 