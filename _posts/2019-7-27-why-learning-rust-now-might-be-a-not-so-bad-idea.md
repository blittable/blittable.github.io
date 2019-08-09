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

Benchmarks are a bit like algorithms - it kind of depends - but here's one: <a href="https://benchmarksgame-team.pages.debian.net/benchmarksgame/which-programs-are-fastest.html">benchmark</a> Here's another: <a href="https://www.techempower.com/benchmarks/">web server response times.</a> 

Having said that, GO is fast. Crystal is fast.  C++ is fast.  JVM languages, dotnet languages, python and many others are fast, or at least, and more importantly, fast enough.  There are shining examples of where Rust's performance matter.  Here's a favorite tool built in Rust that you can use regardless of your preferred coding language:  a command line grep replacement:  <a href="https://github.com/BurntSushi/ripgrep"> ripgrep </a>


### It's Memory Safe  

Security compliance audits for credit cards and host of other verticals target what we expose in memory.  Buffer overflows, dangling pointers, null pointers... in Rust, these are 'handled' upstream at compile-time.  Or more fairly, the compiler mitigates the risk of code not explicitly marked as unsafe from exposing those vulnerabilities.  Some security conscience persons in industry have recently noted precisely <a href="https://msrc-blog.microsoft.com/2019/07/22/why-rust-for-safe-systems-programming/"> that </a> The crypto chain community as likewise taken notice, including Crypto-Chain, Binance and Parity.  
Baidu SDK's for Intel's SGX <a href="https://github.com/baidu/rust-sgx-sdk">uses Rust</a> 

### Packaging, Runtimes, and libraries 

The designers got it right. Pluggable runtimes, package naming, versioning, features, modules, references, etc.  It works as expected. <a href="https://github.com/golang/go/wiki/Modules"> wrong </a> 


