---
layout: post
---

I'v coded with both Reactjs and NodeJS, which both are Javascript and also provide the "Timer" functions which are `setTimeout` and `setInterval`. I have thought these functions are same on both Javascript run in browser and Javascript in NodeJS. But I was wrong.

In browser, the returned value is a `number` which use can use to remove that timer by `clearTimeout` or `clearInterval` function.

In NodeJS, the returned value is a [Timer object](https://nodejs.org/dist/latest-v14.x/docs/api/timers.html#timers_timers). With the timer object (`ref` and `unref`), use can control the callback of timer function. For example, if you want to stop a interval, `interval.unref()`, then, after some function call, you want run the interval again by calling `interval.ref()`

