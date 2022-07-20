# README

_This README is in constant flux, like me!_ :sweat_smile:

There's no ego here, I just want us to understand each other, and I figured this little handbook may help! I like to be transparent and uncomplicated; hopefully this document goes someway towards achieving those goals!

Before we go any further though...

![Graphic showing sign that says "Black lives matter", "Women's Rights are Human Rights", "No Human is Illegal", "Science is Real", "News isn't Fake", "You can't grab anyone there", "Love is Love", "Kindness is Everything"](https://images-na.ssl-images-amazon.com/images/I/619pPybybfL.jpg)

## Me

I am human, I make mistakes; that's normal and a good thing! If I make a mistake, we'll both learn something (hopefully)!

Ultimately, I like to **cause and drive change**. Some call this "progressive"; fine with me! Some call this trouble-making; :smiling_imp:

More specifically I like to

- Teach
- Innovate
- Create
- Alleviate
- Collaborate
- Elevate
- Motivate

### How I learn

Essentially, I'll read some theory, go and play with whatever the thing I'm learning about is, explore it practically, find out what doesn't work, look for solutions to fix what I broke, and implement those fixes. After a while, I'll know what does work, where to go to find answers to problems, some rote fixes, and working knowledge of best practices.

I've found that _only_ reading makes me dogmatic: and dogmatism is stifling for experimentation! I've found that I only get a shallow understanding of whatever the thing I'm learning is too, I need to apply what I'm learning in order to fully appreciate the lesson! Playing and breaking things also keeps me humble.

I also work visually: telling me something can help me to understand, and if the topic is something I'm familiar with, I'll get it, but I really get it if there are visuals used too!

## Me and you

We're both human, we make mistakes; that's normal and a good thing! If we make a mistake, we'll both learn something (hopefully)!

I'm not showy, I like to get my head down and collaborate with others to help them build things that will make people's lives better, including the engineers and people I work with :smile:

I like to have a laugh, and not take a job too seriously. Obviously, there's always a line, but I think we all do our best work when we are at ease, and are willing to make mistakes. I genuinely love doing work with friends, and that's the dynamic I hope our relationship has.

I really admire people who exhibit the following traits. If you do, we'll get on great (hopefully!). If we don't, and we need time to navigate each other's personalities, that's totally fine with me, let's be honest with each other!

- Fearlessness
- Empathy
- Artisinality
- Curiosity
- Trustworthiness
- Authenticity/Integrity
- Honesty
- Clarity
- Adaptability
- Respectfulness (**NOT** reverence)
- Humility
- Gratitude
- Humour

I have three traits I want to inspire and nurture in you if we work together:

1. Fearlessness
1. Empathy
1. Artisinality

### Fearlessness

- Push for innovation
- Question the status quo, relentlessly; shake it up
- Be bold, **be you**

### Empathy

- Kindness is everything
- Seek to understand others and ease their journey
- Support, don't admonish

### Artisinality

- Take pride in what you do
- Always ask "can I do this better?"
- Strive to create things that exhibit [QWAN](https://wiki.c2.com/?QualityWithoutaName) (the link concerns software engineering, but I think it can be generalised too :smile:)

## Me and Software Engineering

I am a scientist at heart[^1]. I believe the scientific method is the most powerful tool we have in order to create good software ![An infographic showing the cyclical nature of the scientific method with the steps: observation, question, hypothesis, experiment, analysis, conclusion](https://miro.medium.com/max/468/1*rc_EeVrnpcqAfwvVp0whRQ.png). Ultimately, the smaller I think we can make this loop, the better, and the more we can do to enable experimentation and analysis in a live environment: the better!

How do we make the loop smaller? I think we do this via [XP principles](http://www.agile-process.org/), and I do evangelise them wherever possible (apologies in advance). By the way, I knew of XP, but never cared to read about it in detail. It was only after an interview I had with a company called Codurance that I was told that what my guidelines for writing good software are, are actually the XP principles. Regardless, I think this speaks to the almost[^2] universal nature of the XP principles? Here they are for reference:

1. Communication
2. Simplicity
3. Feedback
4. Courage
5. Respect

I also think we can make the loop smaller via [The Three Ways](https://www.youtube.com/watch?v=nUOXDEvplRc)

1. Flow/Systems Thinking
2. Amplify feedback loops
3. Culture of Continual Experimentation and Learning

Essentially, I advocate for creating environments where small, cross-functional teams of people can work together easily to:

1. Get customer feedback on what currently works/what's needed next
1. Design experiments based on that feedback, i.e. implement different ways of addressing the customer's feedback
1. Run those experiments

...and round and round we go. This is essentially the [Many More Much Smaller Steps](https://www.youtube.com/watch?v=FLusbyBpugs) concept created by GeePaw Hill.

### Communication

:warning: Under construction! :warning:

### Simplicity

For _everything_. We should always work to what we're limited by and software enginering is limited by people: what we can understand, what we can do, etc. With this in mind, I evangelise for simplicity at all times. That applies to technology choices, team organisation, system architecture etc. Life is better when its simple.

Write less code: design problems away.

- [Trunk Based Development](https://trunkbaseddevelopment.com/) FTW
- [Feature Flags](https://trunkbaseddevelopment.com/feature-flags/) FTW

Work in small teams: less comms, easier to communicate, schedule, etc.

### Feedback

Feedback comes in many forms and at many stages in the software development lifecycle. From left-to-right I think we have the following milestones. For most of these, I've noted useful practices that I'll discuss in detail a bit more below:

1. During requirement creation/refinement
1. During code modification
	- Pairing
	- Mobbing
1. Before code deployment
	- Code reviews
1. After code deployment
	- Testing in production

#### Pairing

:warning: Under construction! :warning:

#### Mobbing

:warning: Under construction! :warning:

#### Code Reviews

I struggled with code reviews. In my first job as part of a software team (rather than a lone wolf: my first engineering job our of university), I had a horrible experience with them, but I think they're incredibly valuable. I'm also aware that code reviews are somewhat anti-thetical to some but I think they're a powerful tool!

<!-- TODO: could add in a link to the Kent Beck exchange I had on Twitter here to illustrate the divide in opinion? -->

1. They can act as a broadcast mechanism to a team of core maintainers who look after a code-base i.e. "heads up! This codebase is about to change!". This especially useful if core maintainers are working separately to each other and are taking contributions from non-core maintainers!

1. They allow for human editing: no matter how profilific a writer you are in any discipline, your work should _always_ be reviewed since what you think is good writing [may be terrible for others](https://www.youtube.com/watch?v=Ng3haLMh-qg&list=PLF2228B872233270A). Everyone needs an editor, that editor should preferably be the people who have to live with what you've written (in the software engineering game)!

1. Machines are great at running repetative tasks that can be scripted with no attention to nuance. They're bad at activities that require general intelligence i.e. understanding context, evaluating known unknowns to make them known, understanding language etc. However, humans are good at these things. Therefore, I believe that code-reviews can be useful to allow humans to reduce complexity, check for missing test cases, check for explicitness of code intent, good names, etc.

So, I think that code reviews should be a natural place to stop and consider what's being changed, why, and how. This is useful since writing a first draft of something is never the best output for you or a team. If you let the ideas sink in a little, you can refine them; think of the [red-green-refactor-commit cycle](https://www.codecademy.com/article/tdd-red-green-refactor) when testing!

I think that we should use code reviews to consider the following:

1. Has the change up for review been made in response to some requirement i.e. does it have an associated ticket? If not, why not? Does the change reflect only what the requirement has stipulated, if not, why not? Has the code been changed in the correct place (component), if not, why not? The business value should already be clear: this is a condition that should be met when creating the requirement, so try to avoid discussions of this in the code review, unless there is no requirement associated with the change!

1. Has documentation been updated in a way you would expect? If documentation has been added, is it understandable easily, does it relate to the change? Have any decisions that lead to the change (architectural decisions, optimizations, design principles etc.) been recorded somewhere in the code base? This information should preferably be somewhere explicit when you come to the codebase so that newcomers can understand why a codebase is the way it is i.e. a `Decision Record` section in the `README`.

1. Are all tests you would expect to see given the requirements present? Are those that exist understandable and valid?

1. Is the source code understandable, maintainable, and in-keeping with the design spirit of the codebase/maintenance team? Are there any opportunities for learning that could be pointed out, any simpler ways of achieving the same result, are class names nouns, do methods have verbs etc.?

1. Has the author done anything notable? If so, give them recognition! A review should also be positive!

I also think that any discussions should have the code as the subject, not the author, and its always best to question, rather than make definitive assertions: _collaboration over confrontation_. Code reviews are a valuable tool to build team relations and help each other upskill!

#### Testing In Production

:warning: Under construction! :warning:

### Courage

Good judgment comes from experience; experience can be good and bad.

Engineers need to play and break things, but in a way that is safe. 

How do we make it easy, fast, and safe to explore? The scientific method. When the scientific method is applied to engineering you get [Many more much smaller steps](https://www.youtube.com/watch?v=FLusbyBpugs).

How do you implement this other than TDD? I advocate heavily for [Progressive Delivery](https://launchdarkly.com/blog/what-is-progressive-delivery-all-about/) in this regard. This video from [Dawn Parzych](https://www.youtube.com/watch?v=u8RprFlSJhM) should adequately clarify my stance too :smile:

- [Testing in production/Minimal long-lived environments](https://www.youtube.com/watch?v=b2oota_FhGY)

- [Test all the f\*\*king time](https://www.youtube.com/watch?v=iwUR0kOVNs8)

- [Write tests. Not too many. Mostly integration](https://kentcdodds.com/blog/write-tests)
	
	- There's no magic code coverage number, in fact, I think we should forget about code coverage metrics. The number of tests should somewhat equal as many features as the thing you're building/maintaining has.

	- Write integration tests first. If there's really a need to test a single function in isolation then do that after the integration tests. Most of the time though, I've found that I don't need single function tests if I've written intrgeation tests.

	- Integration tests are easier to understand (for me any way) since they interact with the API at the level I would if I were using the thing in earnest! 

## Engineers I Admire

:warning: Under construction! :warning:

### Charity Majors

Charity completely blew my mind when I first heard her discussing the concept of testing in production. I am fully with her on this idea: I know there'll always be situations where an environment before releasing to live may be needed, but I think that testing in production and minimal long-lived environments (more on that later) should be the default for applications. [I Test In Prod](https://www.youtube.com/watch?v=DfAwKS1NShs).

### Ian Cooper

Ian finally led me to testing [nirvana](https://www.youtube.com/watch?v=tGc8jL4dzao) (couldn't resist, sorry): his ["TDD, Where Did it All Go Wrong?"](https://www.youtube.com/watch?v=EZ05e7EMOLM) talk finally made [the pieces fit](https://www.youtube.com/watch?v=MM62wjLrgmA) (again, sorry) when it comes to TDD. I now write, and will advocate that you should too, high-level tests that some of us call "integration tests". I get much more confidence from this approach, and I enjoy writing software when I do this too!

### Sandi Metz

If Ian Cooper led me to testing nirvana, Sandi was my initial guide. [99 Bottles of OOP](https://sandimetz.com/99bottles), is a work of art, as is [POODR](https://www.poodr.com/). Those books have really helped me to write easy-to-understand and easy-to-change code, and the explanations are nice and simple. Check Sandi out, you won't regret it!

### Dr Michaela Greiler

Dr Grieler's advice on code reviews has been invaluable to me and has helped me to turn something that I dreaded into a really good team-building tool. [This video](https://www.youtube.com/watch?v=NNXk_WJzyMI) in particular really spoke to me, and [this is another great video of hers](https://www.youtube.com/watch?v=gRR-UhusQe8). Dr Grieler's videos are great, and her suggestions are backed by solid research! Check out her [YouTube channel](https://www.youtube.com/channel/UCWVxDd-f0EbQ_t56MyLobqw) for more :smile:

### Geepaw Hill 

:warning: Under construction! :warning:

### Kent C. Dodds

:warning: Under construction! :warning:

## Engineering Books

Admittedly, I don't read many books nowadays since having a small child takes up a lot of my spare time (amongst trying to exercise, spend time with my wife, do household chores, work etc)! Instead, I tend to read Tweets from prolific engineers, read internet articles by them, watch videos etc. However, I want to try and hold myself accountable, let you see what I like, and make some recommendations since these books have absolutely helped me become a better engineer. So here's a little section on engineering books :smile: You may be surprised that I don't mention certain books here, but there are good reasons[^3] :smiling_imp:

### Top 3

1. [99 Bottles of OOP](https://sandimetz.com/99bottles)
2. [A Philosophy of Software Design](https://web.stanford.edu/~ouster/cgi-bin/book.php)
3. [The Phoenix Project](https://www.amazon.co.uk/Phoenix-Project-DevOps-Helping-Business/dp/0988262592)

### Currently Reading

- Radical Candor
- An Elegant Puzzle

### Incoming!

:warning: Under construction! :warning:

## Engineering Tools I Love Using

Here's some tools that I always make use of if I'm engineering on a machine (and provided I have the rights to install this stuff :joy:). I hope they help you out too :smile:

- [oh-my-zsh](https://ohmyz.sh/)
- [Spock](https://spockframework.org/)
- [Testcontainers](https://www.testcontainers.org/)
- [Cookiecutter](https://cookiecutter.readthedocs.io/en/1.7.2/README.html)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [SDKMAN](https://sdkman.io/)

[^1]: For my sins I worked for 4 years on a PhD and embarked on a post-doctoral degree, with the aim of becoming a professor someday!
[^2]: I am very much a nerd when it comes to software engineering and I love listening to podcasts, talks etc. and reading about how we can do it better. The creators of that content are generally people who were involved in designing XP, so I guess that's where this serendipity came from?!
[^3]: [Its probably time to stop recommending Clean Code](https://qntm.org/clean). I agree with the author of that article, there: after reading the book a few years ago, there is some very good advice in it i.e. [SOLID](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design). However, the examples are horrible, some of it is now outdated because IDEs have progressed _a lot_ since Clean Code was written, and his advice is **very** dogmatic which I'm not a fan of (I think this sets engineers up to be very puritanical, especially newer engineers who are looking for steady ground to stand on; collaboration over confrontation). My other issue is with Martin's general views of the world. They're (in my opinion) harmful in a general social sense and he tends to use his engineering platform to push these, which to me is an abuse of that platform. You can read more about it [here](https://blog.wesleyac.com/posts/robert-martin).