---
layout: post
title: Why learning Rust Now Might not be a Terrible Idea 
categories: Code
---

Nationalism, religion, politics, identity... programming languages.  Tread carefully.  But, I wanted to take a pekak at Rust, at least at a high-level, and make its case. Javascript aside,
, it's been a while since I threw things while coding, and it feels, oddly, good.        

### | move | your but(t)s

- "But I can already do everything in language n, so..."
- "There are no Rust jobs..."
- "Rust is hard."
- "Insufficient libraries/packages to lean on..."

If you dislike challenges, have found a comfort zone, view coding strictly as a trade, and want mountains of god-knows-what code to depend on... agreed, Rust is not for you. 

OK(())

### Rust Overview

Rust is a programming language and ecosystem that generates native code with the support of a couple of libraries.  So, there's a runtime, of sorts, but only via those libraries, and optional. There's no garbage collection. Memory allocation in code is enforced by the *compiler* - so Rust helps you from doing stupid things.  There's some "normally" and "usually" required by the aforesaid, but onward! 

### It's <s>wicked</s> *Glinda* Fast 

The wicked witch of the East was fast, and she landed under a house...  

Benchmarks are a bit like algorithms - best, average, worst cases - but here's one: <a href="https://benchmarksgame-team.pages.debian.net/benchmarksgame/which-programs-are-fastest.html">benchmark</a> 
GO is fast. Crystal is fast.  C++ is fast.  JVM languages, dotnet languages, python and many others are fast, or at least, and more importantly, fast enough.  Let's leave Rust's performance as a necessary but not sufficient condition for your consideration.    

### It's Memory Safe  

Security compliance audits for credit cards and host of other verticals target what we expose in memory.  Buffer overflows, dangling pointers, null pointers... handled upstream at compile-time.  Some security conscience persons in industry have recently noted precisely that <a href="https://msrc-blog.microsoft.com/2019/07/22/why-rust-for-safe-systems-programming/" that /a> The OMG it has to be secure crypto world has likewise taken notice.


