# Source: https://www.testwithlabrador.com/blog/your-first-accessibility-audit

[Back to Blog](https://www.testwithlabrador.com/blog)

![](https://labradorprodstorage.blob.core.windows.net/blog-media/1783000035962-49ozobrzav2.jpg)

What your first accessibility audit should look like, what tools you should use and what it should contain.

## **Your first audit**

I'll start with a confession. My first audit was dreadful, at the very least it was light on information. I could identify most issues by myself, but I needed a lot of help from others. I was the only accessibility champion on my team but I did have some smart and enthusiastic developers around me that gave me a lot of support. These days there are many more resources available and a much larger community of people you can go to for help. And you should.

Your first audit is where you will be doing a lot of learning. In fact the learning never really stops, but the curve is steep and your first audit is likely to be dizzying and take longer than you expect. So the first thing you’ll want to do is give yourself a little bit of time and space to help take the pressure off.

In an ideal world, you won’t be doing your first audits alone. You’ll have a mentor with at least a few years of experience, and they’ll do a quality assessment of your finished work before it goes anywhere.

Because of the steep learning curve I'll recommend that your first audits are done on practice sites and then maybe for a customer for free or in exchange for services like design or web development. Think of it as your opportunity to learn how to deliver your reports and support your clients.

## Before you start

Here’s a handy list of things you’ll need before you get started.

### **Guidelines**

We’re going to use [WCAG 2.2 (opens in new tab)](https://www.w3.org/TR/WCAG22/) as our guide and focus only on the A and AA criterion. It’s not that AAA criterion aren’t useful. It’s more that, in reality, you'll almost never use them. Read over them so that you know what’s there, and there are some that you may want to add into your audit assessment from time to time, but AA conformance is already very difficult for most organisations to fully achieve and AA is where you should start.

If you’re new to accessibility then you’ll want to do at least a couple of test audits to give you an opportunity to work through the criterion one by one. This is the best way to learn.

### **Operating Systems and Tools**

The [Webaim Screen Reader survey (opens in new tab)](https://webaim.org/projects/screenreadersurvey10/#primary) gives incredibly useful insights into the tools that screen reader users use. And while we aren’t focussed on one group of users, understanding screen reader users experience is absolutely essential for a career in testing.

The survey tells us that most screen reader users have a Windows Laptop running [JAWS (opens in new tab)](https://vispero.com/jaws-screen-reader-software/) and/or [NVDA (opens in new tab)](https://www.nvaccess.org/download/) screenreaders with less than 10% using a Mac. If you are a Mac user then it built-in screenreader; Voiceover is pretty good and will probably be sufficient for your first few audits. But it is very clunky to use compared to Windows based screen readers and you really need to be using Safari to ensure best compatibility.

If you plan on doing this as a career then I’d highly recommend getting a decent Windows Laptop and doing most of your testing on that. I know. That’s probably not what you wanted to hear. I’m really sorry.

Other tools you’ll want to familiarise yourself with are switch devices and voice control (like [Dragon Naturally Speaking (opens in new tab)](https://dragonstore.uk/product/dragon-advance-plan/)). These tools can be incredibly expensive and I wouldn’t necessarily recommend that you buy them initially. But you do need to have a clear idea about how they work and the types of accessibility issues that users of these technologies might run into. For an introduction to how people with mobility impairments use this type of technology, watch this video by [Bill Miller (opens in new tab)](https://www.youtube.com/watch?v=cl2ZuomvKG8). Towards the end of this short video Bill demonstrates how to browse websites using just his voice.

To learn more about switch access controls I’d highly recommend watching videos by [Christopher Hills (opens in new tab)](https://www.youtube.com/user/icdhills). I use his videos in my training courses and they really help people to understand how and why people use this type of technology. 

You’ll be emulating switch access controls to some degree throughout your testing as you’ll need to be able to navigate a page without using a mouse in order to test it fully, [nomouse.org (opens in new tab)](http://nomouse.org) has some guidance to get you started.

### **Recording your results**

This is a Labrador Blog and I’m obviously going to recommend Labrador ([https://www.testwithlabrador.com/ (opens in new tab)](https://www.testwithlabrador.com/) ). It’s a professional tool that will greatly reduce the amount of time you spend testing and writing up reports. It has built-in guidance in plain English and It will output a professional looking list of issues ready to share with your clients. You get 2 free, full tests every month and it will store your reports indefinitely. It’s a great asset, we put a lot of thought and effort into making it as easy to use as possible. Go check it out.

If you’re not using Labrador, there are a few options for bug tracking software such as Jira. But you will still need a proof-of-work document for your own self-assurance and to demonstrate that every criterion in WCAG AA has been checked. The ‘traditional’ way of doing this is using spreadsheets. Record each page or component in your sample in the columns, and each WCAG criterion in your rows. Then check every page against every criterion and enter any issues that you find. Spreadsheets have some severe limitations, the main one being that including images as evidence of the things that you find is a real PITA, along with some challenges with versioning. Save yourself all the trouble of finding out about the other issues by signing up for Labrador.

Whichever way you choose to do it, consider treating some of the page content as a separate component so you don’t need to record the same issue multiple times on multiple pages. For example, a website header and footer is likely going to appear on every page in your test sample, (more on the test sample a bit later), so you only really need to record the results once. In Labrador you’ll create a separate component, in a spreadsheet you’ll give each repetitive component its own column.

### **Component vs page testing vs blended**

There’s another approach to testing and that is by identifying all of the components in your sample and testing those individually. The advantage is that most websites re-use the same components and so if you test a component on one page, you probably will get the same results on any page that you find. For some bits of content such as the header and footer, these should almost always be tested at the component level. But things like forms, these are better tested at the page level, because you may find some significant differences between forms on different pages. 

For these reasons a blended approach is normally your best option. Have a list of pages in your sample and then list common components within those pages that only need testing once. Things like header, footer, video player, carousel, side-menu and anything else that appears across multiple pages that don’t change. Then for things that do change, like articles, product pages, apps and games etc. you’ll test and record issues at the page level. The main purpose of this is so that you’re not recording the same issues over and over again. This is as tedious to read as it is to write. So do everyone a favour and keep repetition to a minimum.

### **Screenshots and video**

A picture speaks a thousand words or so they say, and an image of an issue can really help designers and developers to locate and understand each issue. In almost every case where you raise an issue you should include a screenshot. Use markup tools to highlight each issue so it is easy to find. Use video recordings wherever necessary where a picture might not do the job well.

### **Content sample size**

Websites and applications can contain hundreds or even thousands of pages. Nobody tests all of them. It would take too long, cost too much and it’s a law of diminishing returns.

What you’re looking for is a representative sample of pages. Examine the site to find pages that contain unique content, such as forms, video, applications, games, different template types etc. It’s worth meeting with your client to help identify these pages as they’ll be much more familiar with the website. As a very rough guide you’re looking at 10-20 pages in your sample.

Some companies will claim to test many more pages than this, but they’ll be using automated scans and not full manual testing on all pages. It’s a bit sneaky and agencies should be more transparent. It might be worth you doing this too and being clear with your own clients. I’m not going to recommend any specific tools to do that here, but a quick Google search will bring up plenty of options.

Make sure that the scope is agreed with your clients before you start the audit.

### **What each issue should contain**

Almost nobody wanted to spend money on accessibility when I first started. They were underfunded and rushed. My early audits were very low on detail; a screenshot and maybe a paragraph of text with a “pass” or a “fail” attached.

Your reports should have much more detail:

- Location of issue with screenshot and/or video
- WCAG reference number
- Explanation of the issue
- Steps to recreate the issue
- Severity
- Priority
- Expected result
- Remediation advice

These points should mostly be pretty self-explanatory, however severity and priority are subjective. Use a scale of severity something like this:  Advisory, Minor, Moderate, Serious, Critical. Only use Advisory for things that are not WCAG AA non-conformance issues, but may have an impact on the user experience or best practice. For example, if a link has visible text of “Go to basket” and a title attribute of “Go to basket” then this is text that may be read out twice in some circumstances. It’s an irritation for screen reader users and should be called out, but it’s not a WCAG AA failure. At least I don’t think it is. That’s another point. Different accessibility professionals will have different opinions about whether things pass or fail or the level of severity. That’s fine. As long as you are clear on your rationale for your decision that’s all that matters. 

Be aware that the decision you make can impact the product’s release or mean costly remediation. So never inflate the severity of an issue for the sake of impact. And never deflate an issue either. Severity should be judged on the impact on the user, not how easy or difficult an issue is to fix.

As a rough guide, the priority rating generally can follow the severity rating, but in some circumstances you may want to increase it. For example, an issue which has low user impact when experienced once, can have a higher impact if they experience it frequently. So you may occasionally decouple the priority from the severity. Another example of where you might want to do this is where a fix is incredibly simple for a low severity issue and worth doing to get an immediate improvement for the user.

### **Tone**

I think that my first audits weren’t particularly friendly. I’m not sure why. I probably wanted to make some sort of an impression and I ended up making a poor one. 

Your job beyond finding issues is to try to help your client teams understand what they are, how these issues affect users and to help them to fix them. You’re an ambassador for accessibility. Be helpful, friendly and provide as much support as your client needs to resolve the issues that you’ve found. Make people feel better that they chose to work with you and not worse. Leave your customers with the feeling that they’re making the world a better place. 

### **The fix: how far do you go?**

This largely depends on how much you know. I had some idea about HTML when I started with accessibility and it’s actually quite easy to pick up - at least from the point of understanding what the code is doing. CSS and Scripts are more difficult but you’ll pick up what you need over time.

If you don’t have any coding experience then I recommend doing at least a beginner course on HTML. It’s really hard to recommend fixes if you don’t know how to read the cause of the issue. AI can help here but it makes mistakes, and you don’t spot them then you’re going to be recommending fixes you don’t understand and which may be incorrect.

If you have little or no understanding of the code, then you need to point people in the direction. For example, if a form field does’t have a label, find a resource that let’s people know how to do that, like this one: [for HTML attribute (opens in new tab)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/for) don’t try to bluff it. Make sure you describe the fix in plain language.

You’ll get better at this over time.

### **The executive summary nobody reads (except everybody does)**

Half a page at the start of the document - but write it last once you have all of the information. Include:

1. What was tested
2. What was found (list some critical and severe issues)
3. Impact on users - state whether they’re likely to be able to use the product or not

Don’t use Jargon or WCAG numbers, and if you need to use a term like “screen reader” then explain what it means. This is the bit the person with the budget will read.

### **The delivery**

Never hand over an audit without a delivery meeting. I normally refer to this as a "Playback".

A Playback is your opportunity to talk your findings through with the client, to show them what the issues actually mean for users and to help the team who'll be doing the fixing to understand them properly. It's also a chance to build a bit of a relationship with that team, which matters more than the report does in the long run.

Don't just read the report at them. They've either read it already or they haven't, and either way reading it out word for word isn't a great use of anyone's hour. Walk through the highlights. Demonstrate the screen reader experience where you can. Show the keyboard issues. Make it visceral. Findings land a lot harder when people see what's happening than when they're reading a PDF on a Friday afternoon.

You may get some pushback. There's the reasonable kind ("we use this third party widget and we can't change it"), the defensive kind ("it works fine when I test it myself"), and the occasional bit of full denial ("we ran an automated scan and it came back at 95%"). All of it is normal. Don't argue. Acknowledge, explain, move on. You're not in the room to win the meeting. You're there to make sure the right things get fixed.

And if you've got a finding wrong, just say so. It happens. especially when you're starting out.  Even after all these years I’m not to it. Holding your hands up on the spot earns you far more credibility than digging in.

### **The day after**

A common mistake new testers make is treating the audit as the end of the engagement. You send the PDF, you raise the invoice, you move on.

But the audit isn't the product. The improved website is. And nobody fixes accessibility issues in a vacuum. Your client will have questions. They'll find things in your report they're not sure how to interpret. They'll wonder whether their proposed fix actually solves the issue. They'll want a direction and a second pair of eyes before they push something to production.

So follow up. A short check-in two to four weeks later. "How's the remediation going? Anything I can clarify? Anything you'd like a second opinion on?" Sometimes it turns into more work. Sometimes it doesn't. Either way it builds trust, and it makes you the obvious person to call next time.

The clients I'm still working with twenty years on aren't the ones who got the best reports. They're the ones I followed up with after the first audit.

### **Some words of encouragement: You'll get better!**

Your first audit will be worse than your second. Your second will be worse than your tenth. Your tenth one might still make you cringe in five years time. That's the job, and you'll just have to make peace with it.

The thing nobody tells you is that getting better isn't really about getting cleverer about WCAG. The WCAG bit you'll mostly pick up in your first year. After that, the improvement is all in the meta-skills. Scoping properly. Pacing your work so you're not running on fumes by page 180 of a 200 page report. Getting the tone right. Knowing what to leave out. Knowing how to disagree with a developer without making it personal. Knowing how to say "I don't know" without losing credibility.

None of that is in the guidelines. All of it is “the work”.

### **Where next**

Part 4 of this series is about the bit that comes after you've delivered a few decent audits. How to build a reputation, how to find your way into a network of people doing this work, what to be known for, and the difference between being visible and just being shouty.

See you there.

![](https://labradorprodstorage.blob.core.windows.net/blog-media/1782834469775-qwrfgtudz7g.jpeg)

Grant Broome

Co-founder, CEO

[Back to all articles](https://www.testwithlabrador.com/blog)