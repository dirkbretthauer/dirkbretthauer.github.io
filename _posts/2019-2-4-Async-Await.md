---
layout: post
title: async-await the right way
github_comments_issueid: "3"
---

I want to recommend two blog posts about the usage of the async await pattern in C#.
The first one is a blog by [Stephen Toub, "Await, and UI, and deadlocks! Oh my!"](https://blogs.msdn.microsoft.com/pfxteam/2011/01/13/await-and-ui-and-deadlocks-oh-my/ "Await, and UI, and deadlocks! Oh my!")
which is already a few years old (from 2011), but is still valid.
And the other one is by [Jon Goldberger, "Getting Started with Async / Await"](https://blog.xamarin.com/getting-started-with-async-await/ "Getting Started with Async / Await").
Both posts present common pitfalls like accessing .Result on the UI Thread.
