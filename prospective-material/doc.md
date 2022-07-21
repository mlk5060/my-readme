# Coding Principles


## Code Design

1. Get code in front of users quickly and safely

	1. Build pipelines should be efficient and safe

		1. Use tools that encapsulate best practices for free i.e. JIB

		1. Minimal testing for maximum confidence

		1. Minimise environments. Ideal is local -> build pipeline -> live. Envrionments add to operational complexity, and are an exception, rather than a norm.

		1. DRY in build steps, leverage artifact repositories etc.

		1. Smoke testing should be the last step: acts as a blue/green

	1. You'll never replicate production, so stop trying. Invest your efforts in making production great, and empower engineers within it: no one should be scared of live (unless you're going near databases, that's always risky!).

	1. Enable quick recovery from failures, and test from low to high risk customers in a safe and controlled manner (feature toggling with user groups)

1. KEEP IT SIMPLE, STUPID

	1. Maintenance is a big cost: simplification reduces it

	1. Shallow interfaces, deep functionality

	1. Immutability is king!

	1. Single-threaded over multi-threaded!

	1. Cycles in components and interactions between them should be removed with impunity!

	1. Document as much as you can: inline comments are great, not bad; any change should have accompanying documentation if appropriate; documentation should be written for my neighbour, Derek, etc.

1. TDD and BDD

	1. ALWAYS test first, helps to wrap your mind around the problem

	1. Just do enough to make the test green: no one will thank you for doing more!

	1. ALWAYS REFACTOR AFTER GOING GREEN

	1. ALWAYS verify outputs against inputs, not how outputs are determined by inputs

1. High-level testing

	1. More bang for-your-buck: less code covers much functionality. Allows allows for refactoring

	1. How much confidence do you really need? Don't chase metrics. Use metrics to drive conversations, but don't block builds

	1. Helps others understand system better

	1. Low-level tests should be treated with caution: they penalise refactorability for confidence in operation

	1. If other components require sidecars for correct operation, run tests in Docker envrionments with real side-cars. Embedded sidecars never capture actual behaviour! This is the whole "mocks poke holes in reality": avoid them if possible!

	1. Test frameworks that allow for plain language ARE AMAZING: USE THEM!!!

## Architecture Design Flow

1. User stories
	a. Who are the users?
	b. What are the SLA's?
	c. Domain driven design: what are the entities and actions that will occur?

2. Use output from 1 to implement a MVP abstract architecture. Keep it simple, stupid! Add as little as required to achieve the goals given constraints.

	1. Can now look at system like a production line and identify flow points, bottlenecks, race conditions, complex interactions, acyclic flows. Work to remove these!

	1. Go monolith first and break apart later: monoliths are easier to maintain until they get to a certain size (when a single team can no longer fit it inside their heads). Microservices have significant costs due to their distributed nature (debugging is a nightmare)

		1. Use event storming 
	
	1. Writing to disk is always a major constraint!
		1. Any data writing should be transactional if possible, eventual consistency is a special case! Distributed transactions is a special pain, use it only if there's no other option...
		1. Consider sharding to alleviate writing bottlenecks, this works against reads
		1. Consider replication to reduce reading bottlenecks, this works against writes

	1. Data exchange is always a major constriant!
		1. Unless a response from a component is needed immediately during an interaction with it, use an async model to decouple system and allow for non-blocking reactive flows rather than blocking ones.

		1. Any data exchange points should be under contract control. Consider each exchange point and determine if we using producer or consumer-driven contracts there.

	1. Model user sequence diagrams for further detail and to flesh out component responsibilities.

	1. Identify risks
		1. What services are public-facing? These will need high levels of security
		1. Data sinks will need fault tolerance and backup strategies.
		1. Access to components should be on an as-required basis, i.e. consider ACLs.

	1. Note down major architectural principles for each component and its responsibilities: this will help guide their maintenance moving forwards.

	1. Identify what teams will look after each component group, and involve them to help flesh out the picture. Ensure they're comfortable with SLAs and component responsibilities.

3. When abstract view is complete, and component groups are happy, make architecture concrete using actual technologies, in conjunction with component teams.

	1. **Always** enable observability and implement alerts around SLAs via observability tooling
	
	1. Are we operating in the cloud? 
		1. If so, what services could satisfy the component responsibilities given their guiding principals? Always try to offload operations to cloud provider too so engineering teams can focus on features and business specifics!

		1. If not, why not? What would be needed from on-prem systems to make each relevant component available?

	1. Ratify concrete decisions with all relevant parties and ensure they've had input. Use KDDs to make objective decisions.

4. When rolling out system, do so incrementally with low to high risk users, if possible. Fix bottlenecks etc. as we go. This may require component tweaking, or major system tweaks. If the latter is needed, go back to step 2.

5. Any new requirements, go to step 1.


# Questions

These were questions I asked people I line managed when first meeting them and I answered them myself, below: 

1. How do you like to receive feedback, what works best for you?
	- I like people to be honest, and for them to take constructive criticism.
	- I don't like answers such as "well what have YOU done to fix the problem?" if the problem is insurmountable, or
	if I've made it clear that I'm not comfortable with the problematic situation
	- I like regular feedback: its all too easy for my mind to wander to the worst case situation!
	- I like well reasoned criticism, and the chance to discuss such feedback if necessary.
	- I need time to process feedback, and to generate questions. I find it very difficult to think "on the spot". I need space!
	- I like feedback in person, backed by writing. In person you get all the non-verbal stuff, but its hard to keep
	track of all the info and sit with it. This is where the writing comes in... I feel that writing it down ensures that the
	feedback provider also has to think about what they're saying, and to commit to it.
	- I like visuals: the more diagrams, the better!

2. What's your current career trajectory: where have you come from, where do you feel you are now, and where do you want to go in the next 6 months?
	- I was a layabout in school: didn't try hard enough
	- Wanted to be a microbiologist when I was 16-18 because I liked the Offspring...
	- School forced us into university to some degree, but i don't know what I'd have done otherwise!
	- Didn't get the grades to do microbiology at uni, so did marine biology through clearing
	- Got a 1st in my first year, but didn't want to smell of fish every day after work, and first lecture from the head of
	marine biology we were told "If you want to make money, don't do this course..."
	- Thought long and hard about what I *really* wanted to do, always loved computers...
	- Loved CS, ended up getting a 1st 
	- Wanted to be a primary school teacher, got some work experience at my old junior school but, teaching is a dark place as
	far as professions go... so switched to wanting to be a lecturer (love of teaching...)
	- Went on to do a Ph.D in simulating emotions in multi-agent system public goods games
	- Funding was only for 3 years, needed a job since me and my wife had moved in together
	- Worked in 2 companies to pay bills
	- Got a post-doc at Liv Uni (Fernand, what did I do)
	- Didn't continue with lecturship dream because Brexit...
	- Struck out into industry proper
	- Unexpectedly hired as Tech Coordinator

3. Is there anything you would like me to do/avoid when we're working together?
	- Be honest
	- Don't stifle what you want to say, please!
	- Have a laugh: life's too serious
	- Tell me what makes you, you. I want you to enjoy this aspect of your life as much as possible
	- Don't want to talk about other people behind their back. If you have a legit grievance though, please tell me!
	- Tell me how I'm doing, as much as you like!
	- Tell me your achievements, no matter how small. They should be celebrated!

4. What do you enjoy/dislike working on?
	- Love coding: the art of it.
	- Enjoy breaking big tasks into small ones
	- Enjoy helping people learn, giving them that spark of ingenuity and passion
	- Enjoy thinking laterally: using techniques from other disciplines
	- Enjoy reassesing beliefs I held to be true, by way of reasoned arguments and discussion!
	- Enjoy applying scientific method to code
	- Don't enjoy GUI work (I'm a backend guy)
	- Don't enjoy passive meetings where I sit and listen and nod my head...
	- Don't enjoy monotonous tasks, I need to be creative!

5. What are your 3 most salient strengths and weaknesses?
	- Organised
	- Good problem-solver
	- Humble

	- Can't let go of problems: NEED to solve them ASAP
	- Self-doubt: I constantly ask myself if I'm doing things to the best of some too highly held expectations!
	- I like to fully understand issues before wading into them!
