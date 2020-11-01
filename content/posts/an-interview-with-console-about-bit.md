---
author: "Chris Walz"
date: 2020-10-18
linktitle: An Interview With Chris Walz of bit
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: An Interview With Chris Walz of bit
weight: 10
---

# An Interview With Chris Walz of bit

### What is your background?
j
I was born and raised in NY. I started off with the privilege of working as an intern at Google. I then moved on to working in FinTech, InsurTech, and now Construction Tech (ConstruTech?). I enjoy my fair share of table tennis and gaming. (Fun fact: I once reached the #1 rank on the StarCraft 2 ladder (2v2s))

My first foray into programming was in High School. I took a computer science intro course and made some cool things like a flash game where each sprite was a meme from Reddit rage comics. However, I didn’t feel confident in my programming abilities and ended up majoring in Accounting instead. I quickly realized that Accounting was not for me 😅 and switched to Finance. Halfway through college, I started reading about programming and it “clicked”. I began experimenting with Android programming (Shout out to [The Big Nerd Ranch Guide](https://www.amazon.com/Android-Programming-Ranch-Guide-Guides/dp/0321804333)) and never stopped coding since then. You can check out my old Flappy Bird inspired Android game [here](https://play.google.com/store/apps/details?id=com.walz.joltimate.downfall2&hl=en_US). All in all, I graduated with a B.S. in Finance and a minor in Computer Science. 

My favorite language is Go but I mostly use Java and JavaScript during work. I try to steer away from using frameworks when I can but I like the Go web framework Echo. I use React + Redux although I’ve come to realize over time that Redux is overused and leads to too much global state. 

### Why do you try to avoid frameworks? 

Frameworks tend to have magic which can be convenient but also frustrating to work with when you want more customization or you’re dealing with a nasty bug which turns out to be the framework silently undermining you. This is not to say that you shouldn’t use frameworks and it goes on a case by case basis.  Frameworks are usually “high level” and hide details. This is convenient but if you’re simply seeking to learn how to code this may not be beneficial. 

 Libraries are easier to wrap your head around since it will only do something if you explicitly tell it to do so. In turn, one can more easily rule out whether a bug is due to a library for example. The whole system of a computer operates like this to an extent. There are applications built to run on an operating system that runs commands on the kernel which in turn interfaces with the hardware. This system of components and layers is only possible due to API’s/Libraries.

### Why was bit started?

Bit is the summation of a passion for UX, laziness, and a healthy frustration with git’s CLI. Git’s CLI, as many of its users know, has a plethora of commands and options. When you multiply out all the combinations of commands by the number of options and their potential parameters you get A LOT of choices. On top of that, there’s the cornucopia of jargon (detach, head, ref, commit to name a few) and abstruse know-how that, in conjunction, can seduce you into a monotonous hell hole of learning the internal workings of git. Or perhaps put another way – you begin to understand why there is a 500-page book about git. It’s worth pointing out that I like git – but I also enjoy the cathartic pleasure of poking fun at it. Much respect to Linus and all the maintainers that have brought git to where it is today. 

So anyway… the inklings of bit began when I started asking myself why doesn’t git’s CLI do this? Why doesn’t git have an undo button? At some point, I said enough is enough, opened an editor, and started writing some code. Bit started out as this grand new git workflow that would completely change the way people would use git. Or at least that was the plan. After developing it and showing it to some friends I got the vibe that perhaps bit was too opinionated and I decided to dial back some of the changes and focus on an improved UX experience. It started all coming together – intelligent suggestions, branches sorted by most recent, proactive fast-forwarding to avoid merge conflicts and full compatibility with all git commands. A lot of this either alleviates the “maintenance” type tasks of git or helps reduce the working memory that git takes to allow you to focus more on the task at hand.  

Bit has come a long way in such a short period of time considering the very first commit was only just over a month ago. Seeing all the overwhelmingly positive feedback is almost surreal and I’m thankful to all its supporters.  It’s even cooler working with folks across the world to make bit a bit better each day.  

### Are there any overarching goals of bit that drive design or implementation?

Ease. Of. Use. I love simple interfaces (Google Search, Docker Run, the “Easy Button”).  Google Docs is a powerful interface as well (albeit not quite as simple). It does some complex work behind the scenes such as automatic saving, automatic synchronization & distribution, automatic versioning (yes, Google Docs does that as well). It made me wonder how those principles can be applied to version control.  This became the inspiration for the `bit sync` command. 

Put the onus on the program, not the user. Some of bit’s naysayers claim that higher-order commands (e.g. bit sync, git pull) take away from the user’s understanding. Personally, I find that to be a rather weak argument. Abstractions are powerful. Small interfaces are better than large ones. Bit allows you to use all git commands anyway so the trade-off is mitigated in this way. 

### What is the most challenging problem that’s been solved in bit so far?

There have been many challenges:  creating a uniform experience across Operating Systems and Shells,  implementing tab completion, displaying fast interactive prompts, simple installs, and lastly learning lots about git itself 😅. I’d say the biggest challenge I solved(ish) is marketing! Marketing is hard. Even harder for programmers. I posted all over the internetz. Reddit, Discord, Twitter, StackOverflow, and even got my first couple of Stars via a link from another Github repo. Of course, Hacker News was the most successful, hitting #2 on the front page. Interestingly, the first time I posted it fell by the wayside with a measly 5 points 🤷‍♂️. All of this marketing took a lot of time and consideration to get the messaging right on the posts and the landing page (Github README). Not to mention the worry that it’d all be for naught. 

### Is bit intended to eventually be monetized if it isn’t monetized already?

Git is free and open-source so I feel it is only right to continue forward in that spirit and keep bit free and open-source.

[Donations](https://github.com/sponsors/chriswalz) are welcome though (wink, wink)!

### Where do you see bit heading next?

Continued innovation of the UX. Polishing the small details that “delight the user.” The dream goal would be to make such an impact that Git’s CLI UX itself would improve due to the success of bit. Another interesting avenue would be bit aliases that could be written in Go. I hope bit inspires future developers about how the CLI experience, in general, can be improved. I think [Fish](https://fishshell.com/) is doing great work on this front (I had the pleasure of discovering it during my research for bit).  I look forward to the continuing innovation of the shell/CLI space. 

### Where do you see software development, in general, heading next?

Tough question! There are many possibilities considering how quickly innovation happens nowadays. My instinct tells me “No-Code” and “Low-Code” solutions will become increasingly common. Perhaps it will be more visually based where a designer literally draws out a system and an AGI figures out the details (or vice-versa). Maybe even further into the future we will all be hooked up to a Neuralink and code will just spew out of our brains and then we’ll all understand why there’s a programming language called Brain****.

### Where do you see open-source heading next?

I’m rather new to open-source so take my thoughts with a grain of salt. Open-source appears to have a bright future. There seems to be a need for continued innovation around licensing to prevent companies from taking advantage of open-source projects. 

GitHub introduced Sponsoring is a fantastic way to [give back](https://github.com/sponsors/community) to the open-source community.

I think there should be significantly more financial support for projects. It’s unfortunate to see so many projects stop getting maintained over time considering how fundamental they are to companies, big and small. Perhaps implementing some sort of government open-source Incentive program that encourages businesses to donate to open-source projects would make open-source flourish even more.

Also, bringing more attention to open-source through what Console is doing is really great to see.

### What is one question you would like to ask another open-source developer that I didn’t ask you?

How do you go about resolving an issue (specifically bugs) that a user files?

### What is the best way for a new developer to contribute to bit?

Submitting issues & pull requests is nice. Also, changes to the README is quite useful (even with all the fallout from Hacktoberfest!). Look at the [issues](https://github.com/chriswalz/bit/issues) page and look for “good first issue” labels. Also, if you feel like you [don’t know what you’re doing](https://en.wikipedia.org/wiki/Impostor_syndrome) – don’t worry, no one does 😛.  