---
layout: post
title:  "dotsec is here!!"
date:   2025-06-23
categories: [projects, cli]
tags: [rust, terminal]
---

# [`dotsec`](https://github.com/junhsonjb/dotsec) is here!!

I've always had a hard time picking personal projects. I love programming, but I cannot be bothered to do it outside of work *unless it's something I care about*. And, for me, finding something I care about was a constant struggle.

All throughout college, I'd start projects and never finish them. For a while, I thought I was lacking something, but I eventually realized that I'd never found *my thing*. Eventually, I finished school and landed a job, and I was content to write code during the day and spend my free time doing other things.

But lately, I've been wanting to write some Rust code, which was a bit of a problem because Rust is not part of our stack at work. This meant I was going to have to do a personal project.

And that meant finding something I cared about.

I started asking myself what I wanted. I had no idea. But instead of panicking, which is my specialty, I started to pay close attention to my workflow. Every time something annoyed me at work, I took note of it. Before long, I had a mental list of things that I could improve. From those candidates emerged a clear choice: _dotsec_.

## What is dotsec?

`dotsec` is short for ***Dot***file ***Sec***urity. It doesn't work directly with one's dotfiles, so it's a bit of a misnomer, but it's also the name that I came up with, so here we are. Essentially, it's a tool to locally manage *secrets*, or sensitive bits of information that live on one's computer. For example, you can use `dotsec` to safely keep track of your API keys and tokens.

In short, it's a CLI-based secrets manager that stores everything locally. It's built in Rust and intended for those who don't like leaving the terminal (although anyone is free to use the program, regardless of their CLI enthusiasm).

## Why dotsec?

Honestly, `dotsec` was born out of my anxiety. Every time I created a Personal Access Token for GitHub, I was terrified that I'd lose access to it and be locked out of my account forever. This never happened, but the fear still gripped me every time I made a new one. And it was during a mini panic session that I realized one day, "Hey, this can be a personal project!" The rest is history.

After mulling it over for a bit, I felt that `dotsec` could be legitimately helpful to me and others. So I started writing it. 

## How does it work?

`dotsec` uses an in-memory key-value store, [Sled](https://github.com/spacejam/sled), to map identifiers to secrets. Secrets are encrypted using [ChaCha20Poly1305](https://en.wikipedia.org/wiki/ChaCha20-Poly1305). That's it. 

Of course, there was a bunch of code written to make this happen. But the older I've gotten, the more I've learned that simplicity should be the highest goal, especially when it comes to things like software. As the project evolves, the complexity will grow, _but only when it's necessary_.

## Learnings

Now for the good part! If nobody else reads this blog post (or any of them, for that matter), I can't wait to read these myself one day. I can't wait for future Junhson to stumble on this page. Maybe my kids or their kids will read this someday. I hope that I have a positive impact. And what better way to have a positive impact than to share what I've learned?

Let's get into it.

### 1. I love Rust

This one is kind of a cheat. I already knew I loved Rust. But I had forgotten, just a tiny bit, how much fun it is to write Rust. I have a few favorite programming languages, and I'm fortunate enough to use a subset of them at work. But alas, I don't often get to write code in Rust at work. And, like I mentioned above, I hadn't been coding much outside of work.

These past few weeks have been a blast. And on top of the good times, I get to continue investing in myself as an engineer. It's a win-win, and I'm grateful for it.

### 2. OSS is a Commitment

I've loved Open Source Software for a long time. As a terminal enthusiast, I've benefited greatly from the contributions of Open Source contributors. But dotsec is the first project that I've ever released into the wild. Even these first few weeks of maintaining a project that I built alone has required a lot of thought about users and what's best for them. Fortunately, I have a great love of writing code for other engineers, so it's been a fun learning process!

There's so much to think about, and I'm willing to bet that I still have a ton to learn. I certainly hope that this project takes off and that a community builds around it. I'm looking forward to seeing where this goes!

### 3. Licensing ain't easy

Maybe I'm being a bit dramatic. Choosing a license was far from an arduous task. But it wasn't trivial, either. As a longtime OSS user, I've done my fair share of reading on the different licenses out there. But when it came to choosing a license (or licenses) for my project, I wanted to take extra care to set the right boundaries. So I spent some time doing additional research to pad my existing knowledge. My research helped me uncover which license(s) I felt the most comfortable with, but it also reminded me that there's so much that I don't know. I'm excited to keep learning more as this project grows and as I dive deeper into the world of OSS.

## Conclusion

I'm gonna cap it off here. I don't want this to get too long. If you want more, [then go check out the project!](https://github.com/junhsonjb/dotsec) I'm super excited about it, and I hope others will be as well.
