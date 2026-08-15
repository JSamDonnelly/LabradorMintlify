# Source: https://www.testwithlabrador.com/blog/how-to-start-a-career-in-accessibility

[Back to Blog](https://www.testwithlabrador.com/blog)

![Conceptual image: A new flower blooming. Light pink and glowing in the morning sun. ](https://labradorprodstorage.blob.core.windows.net/blog-media/1777636566416-vuldogpgff.jpg)

A guide on how to actually get started in a career in digital accessibility.

So you've decided you're doing this. Good.

Part 1 was the pep talk. This one is the practical piece. What you actually need to know, own, and do before someone will pay you to test for accessibility.

## **Learn the domain**

The most important thing to do here is understand how each criterion applies to real people.

The guidelines themselves can be a bit of a shock, especially if you've never written code. The guidelines consist of many criteria tackling specific aspects of design and development. Back when I was getting in to accessibility for the first time I had very little idea about what they were actually trying to say. The language is extremely technical and frankly speaking, it's probably a blocker to many people getting into the industry. It takes some patience to learn them.

When we built our testing tool [Labrador (opens in new tab)](https://testwithlabrador.com) we were very aware of the learning curve and so wrote all of our guidance in plain English to help people learn and understand each requirement.

So once you learn that "non-text content" generally means images, and "multimedia" generally means "video" it all starts to make sense.

Today there's a few of ways you can tackle learning WCAG. You could book on a course, ask AI (if you're happy to use it) to give you a plain-language version and how a criteria might apply, or just immerse yourself in a test using [Labrador (opens in new tab)](https://testwithlabrador.com) which will go a long way to help you learn and understand each criterion out as you go along.

Beyond the standards themselves, follow people. [LinkedIn (opens in new tab)](https://www.linkedin.com/in/grantbroome/) is the main hangout for the accessibility crowd, for better or worse. [Reddit (opens in new tab)](https://www.reddit.com/) and [Slack (opens in new tab)](https://slack.com/) both have thriving communities. You want a feed that's a mix of practitioners, people with lived experience of disability, and the occasional lawyer posting about the latest lawsuit. That mix will teach you more in six months than any course will.

A word of caution here. The accessibility community online is mostly brilliant, but it has its share of people who mistake being loud for being right. You'll work out who's who soon enough. Follow the ones who teach, not the ones who shout.

## **Learn some HTML (and then some more)**

You don't need to be a developer to work in accessibility. But you do need to be able to read code and know what it's supposed to be doing, and the more you can read, the better you'll be at your job.

The baseline is HTML. Know what most of the tags do. Understand why a <div> means nothing to a screen reader and a <button> means everything. Know what the landmark elements are and why they matter. Know enough to look at a page's source and spot when someone has built an entire interface out of divs and spans, because they almost certainly have.

Then ARIA. And here I'm going to give you the single most important thing I've ever been taught about ARIA: it can fix almost anything, AND you should never use it if they don't have to. Native HTML does the job for free. ARIA is what you reach for when the job can't be done in HTML alone (for a variety of reasons). If you learn one rule, learn that one. It'll save you a hundred audits' worth of arguments.

Past HTML and ARIA, get familiar with what a developer's workflow actually looks like. You don't need to be able to write React, but you should know roughly what React is, what a component is, what a build step is, have an idea of what an Agile development process involves, and why the engineer you're talking to is pulling a face when you ask them to change the colour of a button. Accessibility work happens inside engineering teams, and the more you understand about how those teams actually operate, the more useful you become. And the harder you are to dismiss.

## **Kit yourself out**

You can't test for accessibility without the right kit. Starting out, all the kit you need is completely free. All you need is a half-decent laptop.

At minimum you want… 

### **A screen reader**

Start with [NVDA (opens in new tab)](https://www.nvaccess.org/download/). It's free, it's fully featured, it runs on Windows, and in my experience it's a more honest reflection of what a screen reader is actually doing than some of the paid (and very expensive) alternatives like [JAWS (opens in new tab)](https://vispero.com/jaws-screen-reader-software/). 

VoiceOver is built into Mac and iOS and you'll want to know your way around that too. You may be surprised to find that most accessibility specialists won’t do their main screen reader testing on a Mac. This is because only 9% of screen reader users use a Mac. As a tester the VoiceOver experience is truly awful but it’s difficult to describe why. If you don’t have access to a Mac, don’t stress, it’s something you can invest in later down the line.

JAWS is the industry standard in a lot of enterprise settings, so it's worth downloading the demo and getting familiar with it, particularly for comparison when NVDA is doing something that feels a bit goofy and you want a second opinion. One caveat on JAWS: the demo has licensing terms that may not cover commercial use, so check before you bill anyone for time you've spent in it. 

Whatever combination you land on, learn at least two, because they behave differently and part of your job will be knowing which bugs are actually in the website and which are the screen reader being weird.

### **A browser extension or two**

Note: You probably already know this, but automated tools like the browser extensions mentioned here only cover 30-40% of accessibility issues. They are also probably a little bit inaccurate; especially where colour contrast is concerned so be mindful. After you’ve run your automated checks there’s still 60-70% of the work left to do by hand.

### **[WebAim Wave (opens in new tab)](https://wave.webaim.org/)**

I think we’ll both agree that WebAim Wave is a great tool to start with. It provides a ton of information and it’s easy to see where the issues are coming from. It is a LOT of information in one go though, so it can be a bit much if you just want to check out a few image text alternatives.

### **TPGI’s** **[ARC Toolkit (opens in new tab)](https://www.tpgi.com/arc-platform/arc-toolkit/)**

I’ve really come to love this tool. I started using it last year after doing a comparison of multiple paid and unpaid tools. For some reason I’d glossed over it but I think that for automated testing it’s the best tool out there. It did really well in my comparison and accurately picks out more issues than the other tools in the test.

### **The browser's own dev tools**

Learn the accessibility panel in Chrome or Firefox. It's free, it's powerful, and most people ignore it. Also learn how to edit the HTML in the dev tools window. This way you can see how changes to HTML can improve (or ruin) the experience for assistive technology users.

On devices, ideally you want to test on more than one. Windows and Mac behave differently. iOS and Android behave differently. A bug that's catastrophic on one platform might not exist on another. If you can only afford one setup to start with, pick one (I’d go for Windows with Chrome and NVDA), and then also learn how to use the screen reader on whatever mobile device you currently have.

One last thing on kit and looping back to screen readers. The single most valuable thing you can do is watch someone who actually uses a screen reader every day use the thing you're testing. You will learn more in twenty minutes of that than you will in twenty hours of using NVDA yourself.

A note on how you go about that. If you're doing volunteer work, and someone is happy to volunteer their time alongside you, that's brilliant. Volunteering to volunteering is a fair exchange and a lot of people are genuinely willing. But if you're being paid for the audit, the person helping you should be paid too. Disabled users who do this professionally are specialists, not favour-doers. Their time is worth money, the same way yours is. Know which situation you're in, and act accordingly.

## **A way to record and store results**

Labrador is the tool we’ve built to make the kind of audit I was describing above less of a slog. It's a guided WCAG testing tool. It uses plain-language that you'll understand. It walks you through the checks, it helps you record evidence as you go, it keeps your scope straight, and it turns the whole thing into a report at the end that doesn't look like it was written at 2am the night before delivery (even if it was). It's aimed specifically at the person reading this article: someone who's new enough that the blank page of "where do I even start with this audit" is the scariest bit of the job.

It won't make you a great accessibility tester. Nothing will, except practice. But it'll get you to the point where you're practising the right things, faster. Have a poke around if any of that sounds useful. 

Oh and there’s a free version which is perfect for getting you up and running. Sam and I want to make sure we’re supporting people new to accessibility testing as much as we can.

Go to [testwithlabrador.com (opens in new tab)](http://testwithlabrador.com) - you’ll love it.

Right. Plug over. Back to it.

## **On qualifications**

So. I don't have any formal accessibility qualifications. I started in this industry when there weren't any. I've never taken a CPACC or a WAS, and I’m probably never going to. Labrador’s co-founder Sam has CPACC and he may have some different things to say but here’s what I think.

What I’m going to say next is controversial, so please get a second or third opinion or ask Sam.

From what I've heard from people who have taken the IAAP exams (one of them blind) the exams themselves are often inaccessible (which is a whole other conversation), much of the content isn't particularly relevant to modern practice, and the learning itself isn't especially useful if you've been doing the work for a while. So why would you get a qualification like this?

Well I think that the best reason is because there’s not really any other options out there for a qualification, so if you seriously want to get into this field then it would seem like a good place to start. I salute you.

The other reason I can  think of is bots. Recruitment bots filter CVs before a human ever sees them. A CPACC after your name gets you past the filter. Twenty-plus years of experience might not. I'm really not sure I'd make it through a recruitment funnel at a big company today. Thankfully there are some specialist organisations out there like [PCR Digital (opens in new tab)](https://www.pcrdigital.com/) that match the right accessibility skills to the right work, so if I am ever wondering what to do with myself then that’s where I’d go. 

So here's my take. If you're new, and you need a way to prove to a recruitment system that you're serious, get the qualification. I know it sounds harsh but in my opinion it's a tax, not a signal of competence. Pay the tax if you need to. Don't confuse having the letters with having the skill. The skill comes from doing the work.

If you're lucky enough to be moving into accessibility via an employer who already knows you, a recruitment firm that specialises in web accessibility or via a network that can vouch for you, you can probably skip it entirely.

## **Your first piece of work**

At some point, the learning has to stop being learning and start being work. This is the bit most people get stuck on.

And one thing I can almost certainly guarantee is that your first audit will be bad.

Mine were. I said as much in [Part 1 of this series (opens in new tab)](https://www.testwithlabrador.com/blog/thinking-about-a-career-change). You'll miss things. You'll flag things that aren't actually issues. Your tone will probably be wrong, either too soft to land or too militant to be useful. You'll spend three times as long on it as you will a year from now and it'll be half as good.

That's fine. That's the job of a first audit. Its real purpose isn't to be brilliant. It's to be finished, so you can do a second one. If you are brave enough and lucky enough, I would ask a mentor to review it for you.

A few thoughts on what your first audit actually needs:

- **A clear scope.** What did you test? Which pages, which flows, which platforms, which assistive tech, which browsers? An audit without a scope is just an opinion and it’s impossible to know later what you actually looked at.
- **Evidence.** For every issue, the page, the element, what you did, what happened, what should have happened, and which WCAG criterion it fails against. Screenshots or video clips are essential.
- **Severity.** Not everything is equally broken. A missing alt on a decorative image is not the same as a form that can't be submitted by keyboard. Your report should make that clear at a glance.
- **A fix, or at least a direction.** "This is broken" is half an audit. "This is broken, here's the WCAG reference, here's roughly how to fix it" is a whole one.
- **A human tone.** You are writing this for a developer who has deadlines, a product manager who's under pressure, and a stakeholder who probably doesn't know what a screen reader is. Write accordingly. Explain, don't lecture and try to reduce their learning curve as much as you can.

How do you get a first piece of work in the first place? A few routes:

- Volunteer. Charities, small non-profits, and community organisations frequently need accessibility help and can rarely afford to pay for it. You get real work on a real site, they get a better site, everyone wins.
- Audit your own employer's site, even if it's not your job. Turn it into a report. Send it to someone. The worst that can happen is they ignore it. The best is that you've just invented yourself a new role.
- Join the mentorship programme, which is one of the things I'm currently building. Please get in touch with me if you're interested in joining. Part of the plan is matching new people with small pieces of real work, some paid and some volunteer, so that the first audit isn't a hypothetical exercise.

## **You won't feel ready**

Here's the bit I wish someone had told me when I was starting out.

You are not going to feel completely ready. Not after reading this article. Not after reading the next one. Not after six months of studying the guidelines, or after passing whatever qualification you end up taking, or after your first paid piece of work. The feeling of "I'm qualified to do this now" does not arrive. It just doesn't.

What arrives instead, if you keep going, is evidence. A piece of work you finished. A client who came back. A developer who said thanks. A report you wrote that made something better. The confidence comes from the pile, not from the preparation. You’ll start to see that you are developing knowledge that you’ll only ever get by doing the work.

So if you're reading this and thinking there's too much to learn before you can start, that's the wrong frame. You learn by starting. The list of things in this article isn't a checklist you complete before you're allowed in. It's a map of what you'll pick up while you're already doing the work.

Find the smallest real piece of work you can. Do it. Do it badly. Do it again.

## **Where next**

The next article in this series goes deep on the thing you're now staring at: your first actual audit. What goes in it, what to leave out, how not to sound like you're telling everyone off, and how to write the kind of report that people actually act on.

See you there.

![](https://labradorprodstorage.blob.core.windows.net/blog-media/1777649143149-npdk46qv26.jpeg)

Grant Broome

Co-founder, CEO

[Back to all articles](https://www.testwithlabrador.com/blog)