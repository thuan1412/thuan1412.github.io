---
layout: post
---

I've coded with both Reactjs and NodeJS, which both are Javascript, and also provide the "Timer" functions which are `setTimeout` and `setInterval`. I have thought these functions are the same on both Javascript run in browser and Javascript in NodeJS. But I was wrong.

In the browser, the returned value is a `number` which you can use to remove that timer by `clearTimeout` or `clearInterval` function.

In NodeJS, the returned value is a [Timer object](https://nodejs.org/dist/latest-v14.x/docs/api/timers.html#timers_timers). With the timer object (`ref` and `unref`), you can control the callback of the timer function. For example, if you want to stop an interval, `interval.unref()`, then, after some function call, you want to run the interval again by calling `interval.ref()`
