---
layout: post
title: Learning Rust 
categories: Code
---

Nationalism, religion, politics, identity... programming languages.  Tread carefully.  Let's talk about Rust. Javascript aside,
it's been a while since I threw things while coding, and it feels, oddly, good.  I've definitively quit Rust 3 times in 4 months, but keep coming back. Below are some notes.        



### |move| your but(t)s
---

- "But I can already do everything in language X, so..."
- "There are no Rust jobs..."
- "Rust is hard."
- "Rust doesn't have libraries/packages to lean on..."

  OK(())

Before getting into some details, a couple points: 

- You'll need some time and motivation.
- Rust is categorized as a *systems* programming language, but overflows the category in lots of places.  
- It's still not *great* for building user interfaces, doing websites, data science, and a long list of other things.  


### Rust Overview
---

Rust is a programming language and ecosystem that generates native code with the support of a couple of libraries.  So, there's a runtime, of sorts, but only via those libraries, and optional. There's no garbage collection. Memory allocation in code is enforced by the *compiler* - so Rust helps you from doing stupid things.  There's some "normally" and "usually" required by the aforesaid, but onward! 


### It's <s>wicked, blisteringly</s> Fast 
---

IMHO, benchmarks are a bit like algorithms - it kind of depends best, worst, average - but here's <a href="https://benchmarksgame-team.pages.debian.net/benchmarksgame/which-programs-are-fastest.html">one</a> 
Here's another: <a href="https://www.techempower.com/benchmarks/">web server response times.</a> 

Having said that, GO is fast. Crystal is fast.  C++ is fast.  JVM languages, dotnet languages, python and many others are fast, or at least, and more importantly, fast enough.  
There *are* shining examples of where Rust's leading performance matter.  Here's a favorite tool built in Rust that you can use regardless of your preferred coding language:  a command line grep replacement:  <a href="https://github.com/BurntSushi/ripgrep">ripgrep</a>


### It's Memory Safe  
--- 

Buffer overflows, dangling pointers, null pointers... in Rust, these are 'handled' upstream at compile-time.  Or more fairly, the compiler's design mitigates the risk of code not explicitly marked as unsafe from exposing those vulnerabilities.  
PA-DSS (mostly credit cards) auditors enjoy spilling application memory and picking through the contents.  
Some security conscience persons in industry have recently noted precisely <a href="https://msrc-blog.microsoft.com/2019/07/22/why-rust-for-safe-systems-programming/"> that </a> The crypto/chain community has likewise taken notice, including Crypto-Com, Binance and Parity.  
Baidu SDK's for Intel's SGX <a href="https://github.com/baidu/rust-sgx-sdk">uses Rust</a> to wrap the native libraries on the SDK.

The point: Rust definitely buys you something here - and I had to pick a Rust hill to die on, this would be my choice.


### Packaging, Runtimes, and libraries 
--- 

The designers got it right. Halelujah, thank you.  Configurable runtimes, package naming, versioning, features, modules, references, etc.  It works as expected - it's dull and transparent. 
Not to pick on lovely GO, but: <a href="https://github.com/golang/go/wiki/Modules"> go modules</a> that article is too long.  Enough said.   


### Parallel Processing is Fearless, and with Rayon (a crate in Rust lingo) it's Crazy Easy
--- 

If I want to write code that limited to one core:

{% highlight rust %}

use rayon::prelude::*;

fn sum_of_squares(input: &[i32]) -> i32 {
    input.iter() 
         .map(|&i| i * i)
         .sum()
}
{% endhighlight %}

If I want to write code that utilizes multiple cores:

{% highlight rust %}
use rayon::prelude::*;

fn sum_of_squares(input: &[i32]) -> i32 {
    input.par_iter()  // <-- par_ is the difference 
         .map(|&i| i * i)
         .sum()
}
{% endhighlight %}

Wow.  Cool.


### The Documentation is Excellent 
---

There's a learning curve, no doubt.  It takes some discipline, but going through the documentation, especially <a href="https://doc.rust-lang.org/book"> The Book</a> is a really good idea. 
There's no unneeded formalism.  The content is linear.  There's little assumed about your background, but it doesn't pull punches on the more challenging content.  The writing is good.


### Getting Started - A Couple Suggestions
---

- Rust's rising star, in search, has yet to exceed the stuff you wire-brush off your grill.  So, qualify your searches for <a https://www.rust-lang.org/Rust> Rust</a>.
- Follow the book in the beginning.  It pays dividends.  This is crazy unintuitive for experienced programmers - we have github - we know all sorts of loops and variables.  

But, there's a main function:

{% highlight rust %}
fn main() {
  println!("Hi");
}

{% endhighlight %}

And a main function:

{% highlight rust %}
fn main() {
   procmacro2::misc_syntax!(
      where while abcd : u64 >> 1 + 2 * 3; where T: 'x + A<B='y+C+D>;[M];A::f
   );
}
{% endhighlight %}



### A Pinch More Motivation 
---

- macros, generics, closures, concurrency and parallelism are important Rust features, but you can write tight Rust code without them. There's fun stuff to do as you make progress.
- There are many excellent crates and projects (https://github.com/rust-unofficial/awesome-rust) - too many to mention: but a top-ten, humorless, countdown:

9  - <a href="https://github.com/actix/actix-web">Actix</a>  - A performant web framework   

8  - <a href="https://docs.rs/nom/5.0.0/nom/">Nom</a> Parser combinators 

7  - <a href="https://github.com/ogham/exa">exa</a> - A modern version of ls 

6  - <a href="https://github.com/rustsim/nalgebra">nalgebra </a> - Linear algebra library and some eye-pleasing, well-structured code 

5  - <a href="https://github.com/BurntSushi/xsv">xsv</a> - You'll never look at a csv file the same way again. 

4  - <a href="https://docs.rs/crate/criterion/0.2.11">Criterion</a> - statistical benchmarking library with intelligent function sampling and awesome charts/reporting.  

3  - <a href="https://github.com/crossbeam-rs/crossbeam">Crossbeam</a> - Concurrent programming primitives and tools     

2  - <a href="https://github.com/tikv/tikv">TIKV</a> A key-value database powered by etcd and rocksdb with an optional, stateless, mysql compatibility layer (TIDB) 

1  - <a href="https://github.com/BurntSushi/ripgrep">Grep Replacement</a>

0  - <a href="https://github.com/firecracker-microvm/firecracker">Micro VM Framework</a>   


























