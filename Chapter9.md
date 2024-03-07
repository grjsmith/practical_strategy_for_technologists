# Chapter 8: Real world examples

In this chapter I’ll share examples of where I’ve solved problems using the strategies explored in previous chapters.

## The Department for Work and Pensions DevOps Strategy

In Chapter 3 I shared some of my experience at the Department for Work and Pensions (DWP). This was where my journey into the world of strategy began. I had just published my book Next Gen DevOps. At the time I didn’t realise it was a DevOps strategy book. My new boss, Dewi Price, did though. I took on the role of Head of Strategy for DevOps at the DWP. There was a nascent DevOps department that had built some core capabilities using the tools the DWP made available for them. They had achieved some success but they needed to do more and do it faster. The DWP were embarking on a huge programme of work to move services out of their data centres and into the public cloud. That meant the DevOps initiative needed to mature and scale quickly.

We had three urgent priorities. One was creating a template and repeatable process for helping teams deploy securely into the cloud. The second was to provide teams with the capabilities they needed so they could support their own services once they were deployed into the public cloud. The third priority was protecting ourselves from the numerous challenges from within the DWP who felt they needed to disrupt us.

As this was mine and Naomi’s first formal strategy it came together iteratively. We started out creating a document that looked like a strategy. We got the format from publicly available British military strategies. These are published by the Ministry of Defense as part of their funding announcements. These strategies are designed to be read by any interested party; they start with a context statement that concisely explains the global military context and the national context the military expects to operate in.

One of the interesting aspects of these strategies is what they don’t contain. They don’t contain an explanation of how the strategy will be implemented. I had to read a few of these before I understood why that was missing. The military has a long history that has resulted in a mature organisational structure and operating model. It knows exactly which branches of the service implements the different aspects of any strategy they adopt. In addition to this the military is constantly training so they know exactly what they can achieve with any relevant combination of teams and individuals. The implementation aspect isn’t present in military strategies because they don’t need to write that down in a strategy; it's already defined in their standard operating procedures, training and military exercises. 

The strategy was successfully used to fend off the next couple of attacks in a way that required almost no effort for the leadership. Naomi and I knew we had achieved what we were asked to do. Our next goal was to proactively use the strategy to provide direction to the DevOps department. I know that’s backwards but life’s like that sometimes.

We incorporated the OODA loop into the strategy and I’d recommend everyone does the same. There is no scenario in modern business that doesn’t require rapid observation, assessment and decision making. The purpose of the OODA loop was entirely to help us cope with the CTO’s regular visits and the inevitable requests he would make.

The DevOps department functioned as a platform team. There was a support function that supported all the services that had already launched in the pseudo-cloud that was a precursor to the public cloud. There was a development function that built the configuration management, infrastructure as code and observability capabilities teams needed. Key to our OODA loop implementation was a small team of architects who would work with teams to scope their infrastructure requirements to ensure they were ready for public cloud and that the DevOps capabilities were ready for them.

We would learn that a team was open to receiving some help in a variety of different ways. Sometimes we would hear about it through official channels. Our bosses would get contacted by their bosses and we’d go and talk to them. Sometimes we’d find out through the grapevine that a team was considering the public cloud as a hosting option and we’d go and talk to them. Sometimes teams would be completely oblivious to the public cloud strategy and attempt to migrate a service to or launch a new service in the old data centres and the migration team would refer them to us or us to them. Again when that happened we’d go and talk to them. This conversation was another key to our success.

It meant that we always knew what technologies teams were thinking about using. This is where we learned that a pensions team was going to build a new service using containers. When we discovered this was their plan we built container management and deployment into our plans. The next time the CTO visited he asked us how we’d support containers. We had a plan and a demo of a prototype pipeline. The CTO went away happy and we suffered no unmanaged disruption to our work. This was possible because of the OODA loop strategy. The architects would return from their meetings with the team, debrief the rest of us, we’d investigate and design a solution and fit it into our existing plans, the prototype for that new work was usually underway in the next two week sprint.

Another impressive feature of our service was designed by our architects. They would take an IDE to these meetings with the teams. The IDE contained a tool that generated UML from an architecture diagram. So in the meeting the architect would share their screen and design the infrastructure the team wanted during the meeting. Once the meeting agreed that the diagram was what they wanted the UML was generated and then a script turned that UML into Cloudformation, the architect could execute that on their laptop and by the end of the meeting the team had their cloud infrastructure ready to go. If you know your infrastructure as code you’ll know that was only possible by making a large number of decisions before the meeting. Those were made as a matter of course because the government had very strictly defined standards for network architecture based on the type of data the application was processing and hosting. I mention this because I’m very proud of my little part in this work but also because it was an unintended consequence of the rapid decision making culture we adopted in the strategy. It got everyone thinking about how fast we could be about how we could transform the DWP just by being faster than everyone else. This is the kind of thing I design for now because I know how people’s brains respond to the narrative in a compelling strategy.

This culture of speed was just one aspect of the culture we fostered. When we had written the strategy we knew no one would just sit and read it. That wasn’t what it was built for but we knew that it was useful for more than just defence. The second major iteration of the strategy was extracting some soundbites from the strategy that we could give to our leadership and the engineers so they could prevent challenges from arising in the first place. The idea was that if we had a few pithy messages about what we were doing, people could share them with colleagues in other teams while making tea or getting a coffee. We hoped that these would be shared and unshared across the organisation.

We had good reason for thinking this would work. Government Digital Services have a history of using this approach. When entering the Leeds office where the engineering team was based there were enormous posters and free standing banners talking about agile ways of working. The previous message had been about the importance of user research and this was inescapable because it was one of the first challenges presented to the department that the strategy had to defend against.

The key soundbites that I can remember were things like:

- Every project will have its own AWS account so teams are in charge of their own costs.
- Every project will have its own AWS account so data is secured from other projects by default.
- Our goal is to get teams their infrastructure and then get out of their way.
- Teams don’t have to use our pipelines, they just need to adhere to government standards. Our pipeline just has all that stuff baked in already.

This technique worked exactly as we hoped it would. We know it worked because we’d hear our engineers repeating this stuff to each other as tests during ticket refinement. We’d overhear conversations in the kitchen where these statements were shared with engineers on other projects and we’d hear our leaders come back from meetings where they had heard their peers in other departments repeat these statements and they would ask us if they were really true.

I learned several lessons from this experience:

- Challenges from within the organisation are usually well intentioned
- A strategy document is a great tool for addressing the sorts of challenges that come from inside the organisation
- A well designed strategy is adaptable. It can meet several needs simultaneously and it can be changed to meet unforeseen challenges when they arise
- The people involved with implementation need to be able to share the core principles of the strategy with each other and their colleagues
- Simply being faster than everyone else can be an important aspect of a strategy particularly if you're operating a centralised function.

These lessons built on other things I had learned from my time at AOL and Electronic Arts:

- It’s much harder to change people’s opinions than it is to change software.
- Changing people’s opinions requires multiple tools used in various different contexts and a lot of repetition.

If your organisation is embarking on any significant change a strategy is a great way to organise people around an idea. Planning documents that go straight to a set of requirements won’t engage the people who need to action the strategy. Presenting a business requirement like increasing acquisition or growing revenue and then presenting a plan with no strategy will leave many people in the organisation disenfranchised because a plan lacks context and narrative that people need in order to connect with it.

The strategy document must contain a description of how the change will be implemented. The strategy document isn’t a plan so it doesn’t need to accurately predict the future. This sets the boundaries that constrain how detailed the strategy needs to be. The strategy needs to be detailed enough to engage people’s imaginations about how it might work in practice and allow them to understand their place in it. They must have enough information to consider what they will be accountable for but it needs to leave room for them to consider what they can do to plan to deliver the changes the strategy describes.

The principles of the strategy need to be easy, for people at all levels of the organisation, to share with each other over a coffee. This will help cement the strategy Into the consciousness of the organisation.

## Just Eat, multiple strategies for multiple problems

I’ve written about various different experiences from my time at Just Eat. I want to pull it all together here to help you identify how the different strategies I employed at Just Eat might be useful for you.

When I joined Just Eat in 2016 it was already a successful business. There was a feeling, among the leadership, that Just Eats’ biggest adversary was itself. Coming into Just Eat was a disorienting experience. The problems were obvious, probably anyone in the Technology department could have told you what they were. What was complicated was agreeing solutions with the teams who would need to implement them. This wasn’t just an exercise in being polite. Just Eat had lost control of its microservice interactions and so every proposed change came with a fear that it would have an unexpected knock-on effect. This required a lot of examination of the code to try and identify the service dependencies and a lot of discussion to share what was learned from that examination with the teams. This would then allow conversations to take place where I could try and lead the teams to form their own conclusions about the types of changes they could make to improve the resilience of their services and therefore impact the overall reliability of the platform.

In order to earn the respect and trust of the engineering managers I need to live and work among them. I was following Machiavelli's principle of governing a captured province:

In Chapter 5 of Letters to the Prince Machiavelli talks about a prince taking over a new territory that has been accustomed to its own rule and concludes:

> "…therefore the surest way of holding them is either to destroy them, or for the conqueror to go and live there."

I didn’t have an aspirations of leading these teams in any hierarchical sense but I did need to influence them without any authority. I needed to:

### Make the host and the guest exchange roles (反客為主, Fǎn kè wéi zhǔ)

> Usurp leadership in a situation where one is normally subordinate. Infiltrate one's target. Initially, pretend to be a guest to be accepted, but develop from inside and become the owner later.

I chose to introduce myself as a Product Manager from the DevOps team. My purpose for having any kind of relationship with the engineering managers, their heads of department and their teams was that I was trying to bring a customer-centric, product focused approach to the DevOps tools that engineers used to deploy and host their services. Taking on this mantle allowed me to have a legitimate reason to talk about how services were deployed. This allowed me to lead an initiative to build a blue/green/phased rollout deployment mechanism that would allow teams to test changes in product with portions of their users. With this rolled out I had now established myself as someone who had contributed something to Just Eats teams that gave me a little more influence. I then set about making it easier for Just Eat to identify their service dependencies by leading an initiative to introduce an Application Performance Management (APM) solution. This allowed us to significantly shortcut the conversations about service dependencies and the impact a change to a particular service might have.

This was another OODA loop implementation. At this stage in Just Eat’s life just having a conversation about a change and its potential impact was exhausting for all concerned. Getting the relevant service owners and their product managers together was a herculean task, let alone doing all the research to understand everyone’s service interactions well enough to propose a solution and then proposing that solution in such a way that it wouldn’t make people defensive. This all meant there was literally no way out of any problem. The problem I decided to solve was making it obvious exactly what service interactions needed modification. That reduced the number of people involved in the conversation to two engineering managers. Meaning we could actually plan some proactive changes to improve recovery times and test changes.

During this time the Search team experienced a very serious problem that significantly impacted the Just Eat platform and as a result the entire UK takeaway industry. If the Just Eat platform went down at peak time the rush of customers flocking to other delivery services would bring those other services down too. This severely reduced the number of orders going to restaurants around the country.

This was a horrible situation for the search team. The particular problem they experienced was not a trivial mistake. It didn’t slip into production through a lack of testing. They got hit by a poorly handled undocumented error in .Net itself. This outage gave me another opportunity to use an ancient military strategy:

### Loot a burning house (趁火打劫, Chèn huǒ dǎ jié)

> When a country is beset by internal problems, such as disease, famine, corruption, and crime, it is poorly-equipped to deal with an outside threat. Keep gathering internal information about an enemy. If the enemy is in its weakest state, attack them without mercy and annihilate them to prevent future troubles.

When a team is embattled and struggling that's when they are most susceptible to being helped.

I was able to make progress with a conversation that had previously seen great resistance. The solution to making a real-time search service resilient is pretty straightforward. You make a pre-generated version of the search results available as a static asset. It’s not ideal, it will be less accurate and will give some poor responses but it is significantly better than not having a service at all. In the past this was the resistance presented to the idea. The team would be distracted by the additional work, it would deliver worse results and the bad order rate would go up. This team was primarily motivated by managing this bad order rate metric. The team wanted a solution that meant the search service would never fail. Their reasoning was that most of the times that the search service failed was because of a Thundering Herds problem upstream. They wanted rate limiting and throttling implemented to protect their service. They weren’t wrong, those things should have been done but implementing those solutions was a cross-domain problem and in fact it would be another 18 months before that work even started. The static search results took just a few weeks to implement and Search never caused another platform outage again.

At this point we had fixed some of the obvious problems with relatively easy to implement solutions. I had been joined by a consultant, Brett Johansen. Brett and I concluded that the next point of failure was the database. Just Eat had done what a lot of organisations do when decomposing a monolith and that is they had created new applications to replace functions of the monolith but they had left the monolithic database behind. The microservices that handled core parts of the customer and menu interactions were still reading from and writing to a single database. We convinced the menu team to cache a copy of the menus in Cloudfront and read the menu from there rather than reading it from the database. That removed some activity from the database but still left a lot of interactions. Brett and I then worked in parallel. I found a messaging library that Just Eat had built and was being used in the Restaurant Microservices but wasn’t seeing much use on the customer order tech. That was when I decided to:

### Borrow a corpse to resurrect the soul (借屍還魂, Jiè shī huán hún)

> Take an institution, a technology, a method, or even an ideology that has been forgotten or discarded and appropriate it for one's own purposes.

Brett and I managed to get Just Saying adopted across the whole organisation. That enabled any team to write and read messages asynchronously. That meant no new transactions were being added to the database. That left something like 80,000 transactions still in the core database. Brett pulled an absolute hero move and personally recoded each of them to be parametrised so they could be more easily migrated to the relevant Microservices own data store, decommissioned or modified so they wrote or read messages from SNS.

At Just Eat the political landscape was extremely complicated. Unlike the DWP I wasn’t given a role with any obvious authority. I had to do everything through pure influence. This didn’t leave any room for formulating an overall strategy. I had to find an ‘in’ and demonstrate that I was worth listening to and build on that. That meant being opportunistic and relying on my DevOps experience to show Just Eat’s engineers that, as experienced as they were with DevOps, they still had something they could learn. I didn’t use any strategies instead I relied on system design patterns such as edge caching, deployment strategies and event-driven architecture. I would argue these are strategies they are just smaller in scope but they are:

An identifiable pattern of actions that when performed in similar conditions will achieve predictable results.

Once I had some early successes and had broken the deadlock on a few difficult problems I then had scope for some strategic work. 

## Zoopla Modernisation strategy

When I joined Zoopla in 2019 they had been on quite a journey. They had been a start up and got themselves into a number 2 spot in the market behind Rightmove. Most estate agents listed most of their properties on both Rightmove and Zoopla. Zoopla had an amazing advantage over Rightmove in that it not only offered a consumer service that generated leads for estate agents it also sold and operated a number of specialist CRM solutions that many estate agents used. This gave them an unparalleled opportunity to create synergies for consumers and estate agents. Zoopla had IPO’d and then recently been purchased by a group of investors. This turbulence had caused people to leave and had also resulted in a complex technology landscape some of which was based on languages that were out of fashion and so were difficult to hire for.

When I first joined Zoopla I was expecting to work on decomposing the monolithic Perl codebase that ran most of the website and all the data processing for the consumer side of the business. Between my interview and joining Zoopla things had changed. The priority now was reinvigorating the website so that Zoopla could get on top of managing it’s SEO ranking and showing the senior leadership team and the investors that the technology organisation could make good use of engineers if it got them. This was encapsulated in a time to onboard metric. At the time I joined it took 2 weeks, on average between an engineers induction and the first time they committed useful code. Our goal was 1 day and that was useful code, not just getting the engineer to add their name to a YAML file and pushing it to production.

Three things were weighing on everyone’s mind:

- Zoopla were struggling to maintain their SEO ranking
- Google were changing how they rated SEO introducing Core Web Vitals.
- Zoopla couldn’t confidently change most of their website in less than two weeks

The strategy we came up with was to add another tech stack. If that sounds absurd then you too may be an XKCD fan.

<img src="images/standards.png" alt="XKCD Comic about standards">

This comic is [https://xkcd.com/927/](https://xkcd.com/927/) see xkcd.com for more hilarity.

We needed to make radical changes to the website to address a huge list of requirements from the SEO team. There was no way we were going to be able to hire engineers who knew Perl and Mojolicious and there was no way anyone would want to train on that tech stack. We reviewed all the CV’s Zoopla had ever received for front-end and fullstack engineers and we saw that the most common tech stack was React.
 