# Chapter 8: Real world examples

In this chapter I’ll share examples of where I’ve solved problems using strategies. The purpose of this chapter is to demonstrate that an organisation doesn't have to ask for a strategy in order to benefit from one.

## The Department for Work and Pensions DevOps Strategy

In Chapter 3 I shared some of my experience at the Department for Work and Pensions (DWP). This was where my journey into the world of strategy began. I had just published my book Next Gen DevOps. At the time I didn’t realise it was a DevOps strategy book. My new boss, Dewi Price, did though. I took on the role of Head of Strategy for DevOps at the DWP. There was a nascent DevOps department that had built some core capabilities using the tools the DWP made available for them. They had achieved some success but they needed to do more and do it faster. The DWP were embarking on a huge programme of work to move services out of their data centres and into the public cloud. That meant the DevOps initiative needed to mature and scale quickly.

We had three urgent priorities. One was creating a template and repeatable process for helping teams deploy securely into the cloud. The second was to provide teams with the capabilities they needed so they could support their own services once they were deployed into the public cloud. The third priority was protecting ourselves from the numerous challenges from within the DWP who felt they needed to disrupt us.

As this was mine and Naomi’s first formal strategy it came together iteratively. We started out creating a document that looked like a strategy. We got the format from publicly available British military strategies. These are published by the Ministry of Defense as part of their funding announcements. These strategies are designed to be read by any interested party; they start with a context statement that concisely explains the global military context and the national context the military expects to operate in.

One of the interesting aspects of these strategies is what they don’t contain. They don’t contain an explanation of how the strategy will be implemented. I had to read a few of these before I understood why that was missing. The military has a long history that has resulted in a mature organisational structure and operating model. It knows exactly which branches of the service implements the different aspects of any strategy they adopt. In addition to this the military is constantly training so they know exactly what they can achieve with any relevant combination of teams and individuals. The implementation aspect isn’t present in military strategies because they don’t need to write that down in a strategy; it's already defined in their standard operating procedures, training and tested in regular military exercises.

The strategy we created was similar to the military strategy reviewed in Chapter 8. It differed in that we included some responses to challenges the initiative had already received and fended off. We also knew the primary concerns of the civil service such as cost management, duplication of effort and security so we preemptively provided statements that described how these were designed into the solution by default.

The first iteration of the strategy was successfully used to fend off the next couple of attacks in a way that required almost no effort from the leadership. Naomi and I knew we had achieved what we were asked to do. Our next goal was to proactively use the strategy to provide direction to the DevOps department. I know that’s backwards but life’s like that sometimes.

We incorporated the OODA loop into the strategy and I’d recommend everyone does the same. There is no scenario in modern business that doesn’t require rapid observation, assessment, decision making and action. The purpose of the OODA loop was entirely to help us cope with the CTO’s regular visits and the inevitable requests he would make.

The DevOps department functioned as a platform team. There was a support function that supported all the services that had already launched in the pseudo-cloud that was a precursor to the public cloud. There was a development function that built the configuration management, infrastructure-as-code and observability capabilities the product teams needed. Key to our OODA loop implementation was a small team of architects who would work with teams to scope their infrastructure requirements to ensure they were ready for public cloud and that the DevOps capabilities were ready for them.

We would learn that a team was open to receiving some help in a variety of different ways. Sometimes we would hear about it through official channels. Our bosses would get contacted by their bosses and we’d go and talk to them. Sometimes we’d find out through the grapevine that a team was considering the public cloud as a hosting option and we’d go and talk to them. Sometimes teams would be completely oblivious to the public cloud strategy and attempt to migrate a service to or launch a new service in the old data centres and the migration team would refer them to us. When that happened we’d go and talk to them. This conversation was another key to our success.

It meant that we always knew what technologies teams were thinking about using. This is where we learned that a pensions team was going to build a new service using containers. When we discovered this was their plan we built container management and deployment into our plans. The next time the CTO visited he asked us how we’d support containers. We had a plan and a demo of a prototype pipeline. The CTO went away happy and we suffered no unmanaged disruption to our work. This was possible because of the OODA loop strategy. The architects would return from their meetings with the team, debrief the rest of us, we’d investigate and design a solution and fit it into our existing plans, the prototype for that new work was usually underway in the next two week sprint.

Another impressive feature of our service was designed by our architects. They would take an Integrated Development Environment (IDE or fancy text editor for the uninitiated into the mysteries of software engineering) to these meetings with the teams. The IDE contained a tool that generated Unified Modelling Language (UML) from an architecture diagram. So in the meeting the architect would share their screen and design the infrastructure the team wanted during the meeting. Once the meeting agreed that the diagram was what they wanted the UML was generated and then a script turned that UML into Cloudformation, the architect could execute that on their laptop and by the end of the meeting the team had their cloud infrastructure ready to go. If you know your infrastructure as code you’ll know that was only possible by making a large number of decisions before the meeting. Those were made as a matter of course because the government had very strictly defined standards for network architecture based on the type of data the application was processing and hosting. I mention this because it came about as an unintended consequence of the rapid decision making culture we adopted in the strategy. The strategies OODA loop implementation got everyone thinking about how fast we could be about how we could transform the DWP just by being faster than everyone else. This is the kind of thing I design for now because I know how people’s brains respond to the narrative in a compelling strategy.

This culture of speed was just one aspect of the culture we fostered. When we had written the strategy we knew no one would just sit and read it. That wasn’t what it was built for but we knew that it was useful for more than just defence. The second major iteration of the strategy involved extracting some soundbites from it. We gave those to our leadership and the engineers so they could prevent challenges from arising in the first place. The idea was that if we had a few pithy key messages about what we were doing, people could share them with colleagues in other teams while making tea or having a chat. We hoped that these would be shared and re-shared across the organisation.

We had good reason for thinking this would work. Government Digital Services have a history of using this approach. When entering the Leeds office where the engineering team was based there were enormous posters and free standing banners talking about agile ways of working. The previous message had been about the importance of user research and this was inescapable because it was one of the first challenges presented to the department.

The key soundbites that I can remember were:

- Every project will have its own AWS account so teams are in charge of their own costs and there is complete cost transparency.
- Every project will have its own AWS account so data is secured from other projects by default.
- Our goal is to get teams their infrastructure and then get out of their way.
- Teams don’t have to use our pipelines, they just need to adhere to government standards. Our pipeline just has all that stuff built in already.

This technique worked exactly as we hoped it would. We know it worked because we’d hear our engineers repeating this stuff to each other while scoping tickets during refinement. We’d overhear conversations in the kitchen where these statements were shared with engineers on other projects and we’d hear our leaders come back from meetings where they had heard their peers in other departments repeat these statements and they would ask us if they were really true.

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

The strategy document must contain a description of how the change will be implemented. The strategy document isn’t a plan so it doesn’t need to accurately predict the future. This sets the boundaries that constrain how detailed the strategy needs to be. The strategy needs to be detailed enough to engage people’s imagination about how it might work in practice and allow them to understand their place in it. They must have enough information to consider what they will be accountable for but it needs to leave room for them to consider what they can do to plan to deliver the changes the strategy describes.

The principles of the strategy need to be simple for people at all levels of the organisation, to share with each other over a coffee. This will help cement the strategy Into the consciousness of the organisation.

## Just Eat, multiple strategies for multiple problems

Throughout the book I’ve shared various experiences from my time at Just Eat. Here I'll pull it all together in context. Just Eat was an interesting experience particularly after having such a formal strategy role at the DWP.

When I joined Just Eat in 2016 it was already a successful business. There was a feeling, among the leadership, that Just Eats’ biggest adversary was itself. Coming into Just Eat was a disorienting experience. The problems were obvious, probably anyone in the Technology department could have told you what they were. What was complicated was agreeing solutions with the teams who would need to implement them. This wasn’t just an exercise in being polite. Just Eat had lost control of its microservice interactions and so every proposed change came with a fear that it would have an unexpected knock-on effect. This required a lot of examination of the code to try and identify the service dependencies and a lot of discussion to share what was learned from that examination with the teams. This would then allow conversations to take place where I could try and lead the teams to form their own conclusions about the types of changes they could make to improve the resilience of their services and therefore impact the overall reliability of the platform.

In order to earn the respect and trust of the engineering managers I needed to live and work among them. I was following Machiavelli's principle of governing a captured province:

In Chapter 5 of Letters to the Prince Machiavelli talks about a prince taking over a new territory that has been accustomed to its own rule and concludes:

> "…therefore the surest way of holding them is either to destroy them, or for the conqueror to go and live there."

I didn’t have any aspirations to formally lead these teams in any hierarchical sense but I did need to influence them without having any authority. I needed to:

### Make the host and the guest exchange roles (反客為主, Fǎn kè wéi zhǔ)

> Usurp leadership in a situation where one is normally subordinate. Infiltrate one's target. Initially, pretend to be a guest to be accepted, but develop from inside and become the owner later.

I chose to introduce myself as a Product Manager from the DevOps team. My purpose for having any kind of relationship with the engineering managers, their heads of department and their teams was that I was trying to bring a customer-centric, product focused approach to the DevOps tools that engineers used to deploy and host their services. Taking on this mantle allowed me to have a legitimate reason to talk about how services were deployed. This allowed me to lead an initiative to build a blue/green/phased rollout deployment mechanism that would allow teams to test changes in production with small portions of their users before they impacted the entire service. With this rolled out I had now established myself as someone who had contributed something to Just Eat's teams that gave me a little more influence.

During this time the Search team experienced a very serious problem that significantly impacted the Just Eat platform and as a result the entire UK takeaway industry. If the Just Eat platform went down at peak time the rush of customers flocking to other delivery services would bring those other services down too. This severely reduced the number of orders going to restaurants around the country.

This was a horrible situation for the Search team. The particular problem they experienced was not a trivial mistake. It didn’t slip into production through a lack of testing. They got hit by a poorly handled undocumented error in .Net itself. This outage gave me another opportunity to use an ancient Chinese military strategy:

### Loot a burning house (趁火打劫, Chèn huǒ dǎ jié)

> When a country is beset by internal problems, such as disease, famine, corruption, and crime, it is poorly-equipped to deal with an outside threat. Keep gathering internal information about an enemy. If the enemy is in its weakest state, attack them without mercy and annihilate them to prevent future troubles.

When a team is embattled and struggling that's when they are most susceptible to being helped. They'll reconsider ideas they have previously rejected and they'll listen to new ideas they wouldn't otherwise entertain.

I was able to make progress with a conversation that had previously seen resistance. The solution to making a real-time search service resilient is pretty straightforward. You make a pre-generated version of the search results available as a static asset. It’s not ideal, it will be less accurate and will give some poor responses but it is significantly better than not having a service at all. In the past this was the resistance presented to the idea. The team would be distracted by the additional work, it would deliver worse results and the bad order rate would go up. This team was primarily motivated by managing this bad order rate metric. The team wanted a solution that meant the full search service would never fail. Their reasoning was that most of the times that the search service failed was because of a Thundering Herds problem upstream. They wanted rate limiting and throttling implemented to protect their service. They weren’t wrong, those things should have been done but implementing those solutions was a cross-domain problem and in fact it would be another 18 months before that work even started. The static search results took just a few weeks to implement and Search never caused another platform outage again.

> The Thundering herds problem is when a service has failed, or just launched with amazing marketing and the traffic flows to it in an unmanaged fashion. Services behave differently when loads ramp up gradually than when they thunder in all at once. This is one of the many problems an immature online service faces. Most software engineers don't have the experience to build these solutions when they are first building the software for a start-up.

At this point we had fixed some of the obvious problems with relatively easy to implement solutions. I had been joined by a consultant, Brett Johansen. Brett and I concluded that the next point of failure was the database. Just Eat had done what a lot of organisations do when decomposing a monolith and that is they had created new applications to replace functions of the monolith but they had left the monolithic database behind. The microservices that handled core parts of the customer and menu interactions were still reading from and writing to a single database. We convinced the menu team to cache a copy of the menus in Cloudfront and read the menu from there rather than reading it from the database. That removed some activity from the database but still left a lot of interactions. Brett and I then worked in parallel. I found a messaging library that Just Eat had built and was being used in the Restaurant Microservices but wasn’t seeing much use on the customer order tech. That was when I decided to:

### Borrow a corpse to resurrect the soul (借屍還魂, Jiè shī huán hún)

> Take an institution, a technology, a method, or even an ideology that has been forgotten or discarded and appropriate it for one's own purposes.

Brett and I managed to get Just Saying adopted across the whole organisation. That enabled any team to write and read messages asynchronously. That meant no new transactions were being added to the database. That left something like 80,000 transactions still in the core database. Brett pulled an absolute hero move and personally recoded each of them to allow them to be cached by the database buying time for teams to migrate their database activity to their Microservices own data stores, decommission them or modify them so they wrote or read messages from AWS SNS.

I then set about making it easier for Just Eat to identify their service dependencies by leading an initiative to introduce an Application Performance Management (APM) solution. This allowed us to significantly shortcut the conversations about service dependencies and the impact a change to a particular service might have.

This was an example of luring the tiger down the mountain.

### Lure the tiger down the mountain (調虎離山, Diào hǔ lí shān)

>Never directly attack an opponent whose advantage is derived from their position. Instead, lure them away from their position to separate them from their source of strength.

The engineering teams were strongest in their territory; their territory was their services and their domain knowledge. Telling them they had to change their service was extremely difficult. That was their home turf. Remember that when describing territory we are describing an intellectual position. The territory the teams were less comfortable on was the platform-as-a-whole. The APM tool allowed us to view all the transactions moving through the platform, this allowed us to describe problems in the context of a business function or a user journey not just in the context of an individual service. This made the conversation much more even because that was no one team's territory.

> Eventually we evolved a first line support function into a position of ownership of the platform. That then became their territory where they were strong and the teams took guidance from them on platform-wide concerns.

The APM and the conversation about the platform-as-a-whole then enabled another OODA loop implementation. At this stage in Just Eat’s life just having a conversation about a change and its potential impact was exhausting for all concerned. Getting the relevant service owners and their product managers together was a herculean task, let alone doing all the research to understand everyone’s service interactions well enough to propose a solution and then proposing that solution in such a way that it wouldn’t make people defensive. This all meant there was literally no way out of any problem. The problem I decided to solve was making it obvious exactly what service interactions needed modification. That reduced the number of people involved in the conversation to two engineering managers. Meaning we could actually plan some proactive changes to improve recovery times and test changes.

At Just Eat the political landscape was extremely complicated. Unlike the DWP I wasn’t given a role with any obvious authority. I had to do everything through pure influence. This didn’t leave any room for formulating an overall strategy from the start. I had to find an ‘in’ and demonstrate that I was worth listening to and build on that. That meant being opportunistic and relying on my DevOps experience to show Just Eat’s engineers that, as experienced as they were with DevOps, they still had something they could learn. I relied on system design patterns such as edge-caching, deployment strategies and event-driven architecture. It could be argued these are not strategies that they are system design or architecture patterns but they are:

**An identifiable pattern of actions that when performed in similar conditions will achieve predictable results.**

Once I had some early successes and had broken the deadlock on a few difficult problems I then had scope for applying some smaller scope strategies.

## Zoopla Modernisation strategy

When I joined Zoopla in 2019 they had been on quite a journey. They had been a start-up and got themselves into a number 2 spot in the market behind Rightmove. Most estate agents listed most of their properties on both Rightmove and Zoopla. Zoopla had an amazing advantage over Rightmove in that it not only offered a consumer service that generated leads for estate agents it also sold and operated a number of specialist CRM solutions that many estate agents used. This gave them an unparalleled opportunity to create synergies for consumers and estate agents. Zoopla had IPO’d and then  been purchased by a group of investors. This turbulence had caused people to leave and had also resulted in a complex technology landscape some of which was based on languages that were so out of fashion and they were difficult to hire for.

When I first joined Zoopla I was expecting to work on decomposing the monolithic Perl codebase that ran most of the website and all the data processing for the consumer side of the business. Between my interview and joining Zoopla things had changed. The priority now was reinvigorating the website so that Zoopla could get on top of managing it’s SEO ranking and showing the senior leadership team and the investors that the technology organisation could make good use of engineers if it got the funding for them. This was encapsulated in a time to onboard metric. At the time I joined it took 2 weeks, on average, between an engineer's induction and the first time they committed useful code. Our goal was to get that down to one day. That was useful code mind, not just getting the engineer to add their name to a YAML file and pushing it to production.

Three things were weighing on everyone’s mind:

- Zoopla were struggling to maintain their SEO ranking
- Google were changing how they ranked sites, introducing Core Web Vitals.
- Zoopla couldn’t confidently change most of their website in less than two weeks

The strategy we came up with was to add another tech stack. If that sounds absurd then you too may be an XKCD fan.

<img src="images/standards.png" alt="XKCD Comic about standards">

This comic is [https://xkcd.com/927/](https://xkcd.com/927/) see xkcd.com for more hilarity.

We needed to make radical changes to the website to address a huge list of requirements from the SEO team. There was no way we were going to be able to hire engineers who knew Perl and Mojolicious (the Perl web framework in use at Zoopla) and there was no way anyone would want to train on that tech stack. We reviewed all the CV’s Zoopla had ever received for front-end and fullstack engineers and we saw that the most common tech stack was React.

We created a new web platform using React and Next.js. A lot of the website was already in vanilla Javascript so React wasn't a huge stretch intellectually, although I acknowledge we didn't make things simpler by adding yet another tech stack.

React was a strategic choice though:

- We could hire engineers with years of React experience.
- We could research how other people were solving for core web vitals in blogs, on Youtube and Stackoverflow.
- We could use a whole bunch of industry standard tooling that other people had already designed integrations for such as Gitlab-ci, Prettier, Yarn, ESLint, Storybook, Styled Components.

This meant that progress was made quickly. It was demonstrated that we could onboard new engineers in a day and the funding was released to allow hiring to proceed.

The first strategy I pursued at Zoopla was one of the most ancient in the world: The Pincer Movement. I had two and a half teams of engineers available to me. A team of Perl developers, two squads of Typescript developers and a couple of great polyglots.

I set the Perl developers the task of building test databases. I knew at some point I would need to take control of the processes that authored the listings and customer data. These processes were hopelessly entangled in the Perl monolith. We tried in vain to insert tests or define dependencies, only to find more and more and more dependencies. There were a million lines of Perl and I had one team and just a few weeks before we had to give up and move on to something more fruitful. So the team attempted to disentangle the code that built the databases.

In the meantime I had one squad of Typescript developers building a GraphQL server. The logic here was that whatever happened to the underlying data sources I'd need a platform that was adaptable and could optimise the data for presentation purposes. This gave me multiple **two-way doors**. Regardless of what happened with the data I would be able to cope. Even if no progress was possible with the data the GraphQL server would still make it possible to have maximum performance of the website even if the Perl APIs were slow or delivering too much data that was poorly structured for display.

I ran another Pincer Movement on routing. The developers who built the website couldn't manage the routing to their pages. This meant they struggled to test their code in an environment they felt was production-like. They had to go begging to the infrastructure team to make changes to Nginx that managed the internal routing of traffic. That infrastructure team had their own priorities and this led to the kind of us and them that DevOps was supposed to fix. In the web Typescript squad we implemented Next.js to manage the routing once the traffic got to the React site. The polyglot developers worked to unpick the routing to allow us to manage routing to individual pages and I had another developer make it possible for Typescript engineers to test routing changes made in Nginx. We then took advantage of a new feature in Nginx that allowed us to write Nginx configuration in Javascript instead of Lua, which the developers were much more comfortable with.

My goal with all these teams and pincer movements was to create Napoleonic style **Corps D'Armées**. I wanted small teams who understood the underlying strategy and their individual contexts and could engage with any day-to-day problem and stay on track. I needed that because I needed to split my attention across a number of different problems. I was helping with hiring, onboarding new engineers and helping the leadership team plan what they would do with the new capabilities we were delivering. I was also trying to strengthen the relationship with marketing (the SEO team reported in to marketing) and the data organisation.

The good relationship I built with the SEO team and the Marketing department as a whole was for two reasons. One was obvious and on the surface. One of my success criteria was improving Zoopla's SEO ranking. I needed to demonstrate that I had implemented everything the SEO team needed. This meant I needed a good relationship so we could prioritise those needs and show progress. The other reason was more manipulative. I needed the ability to:

### Kill with a borrowed knife (借刀殺人, Jiè dāo shā rén)

>Attack using the strength of another when in a situation where using one's own strength is not favourable. For example, trick an ally into attacking them or use the enemy's own strength against them. The idea is to cause damage to the enemy via a third party.

Like any organisation, particularly with a lot of technology solutions that have built up and atrophied over the years almost every decision was contentious. The method we used to style the website, how we cached content, how content was presented on pages and on what pages that content was presented on, the tags that were implemented and how they were implemented. All of these things required multiple layers of conversations with the engineers and also with the leadership team. Using the Marketing departments knives helped me shortcut a lot of those conversations. Given Zoopla's nature, as a classifieds service, the marketing department was very powerful and had some formidable leaders. If I didn't take them seriously they could make mine and the technology leadership's life very difficult but they made for powerful allies. The same went for the data department. Marketing need data in order to make decisions. Data-driven was and still is a buzzword term that loosens the pockets of investors. Having my solutions ratified by the data department also ended some conversations before they even began. If this sounds duplicitous remember that I lent my knife to the Marketing department, in the form of the SEO team and helped their burgeoning product marketing function make a splash by ensuring they knew everything going on with the new tech stack. I also leant my knife to the data team who were executing a re-platforming of their own. I had built some credibility so confirming that I thought they were making great choices (they were) helped them too.

I wrote extensively in Chapter 5 how I used the:

### Befriend a distant state and strike a neighbouring one (遠交近攻, Yuǎn jiāo jìn gōng)

>Invading nations close to oneself carries a higher chance of success. The battlefields are close to one's domain and as such is easier for one's troops to receive supplies and defend the conquered land. Make allies with nations far away from oneself, as it is unwise to invade them.

and:

### Make the host and the guest exchange roles (反客為主, Fǎn kè wéi zhǔ)

>Usurp leadership in a situation where one is normally subordinate. Infiltrate one's target. Initially, pretend to be a guest to be accepted, but develop from inside and become the owner later.

At Zoopla I very purposefully chained strategies together. While none of the technical problems were particularly challenging there were many of them, they were all interlinked and multiple departments had needs of them that were not easily balanced.

Not everything worked the way I wanted I was forced to:

### Sacrifice the plum tree to preserve the peach tree (李代桃僵, Lǐ dài táo jiāng)

>There are circumstances where short-term objectives must be sacrificed in order to gain the long-term goal. This is the scapegoat strategy where someone suffers the consequences so that the rest do not.

My plum tree was the component library and the component library team. One of the key features of the React framework is that everything is a component. Web pages are really very minor concerns in React there are merely places that describe what components will be displayed to the user. Components themselves can and should be decomposed into what are known as atoms, molecules and organisms

-------------------------------------------------- insert book reference

This approach allows for very thorough testing of the basic elements of a web page. When those elements are brought together to make complex components they don't need as much testing. This in turn means they are developed faster and their development time is quickly becomes predictable.

I could not convince Zoopla's leadership of this. I tried everything, including all my borrowed knives to no avail. Sacrificing the plum tree allowed me to preserve the peach tree which was the rest of the tech stack. We paid the price for that. Components took longer to build but it was impossible to prove that it would have been faster if we'd had more support for the component library and the component library team.

My strategic approach helped keep me and the teams focused, we had the new platform up and running very quickly. We had the most important and complex page built a few months later without the help of a product manager and with the disruption of COVID lockdown in the middle of the project.

## Marks and Spencer (M&S)

Marks and Spencer wanted a very safe operating environment to support development of their e-commerce site, loyalty and reward programmes. They also intended to grow their own in-house development capability. They started the initiative with a handful of very skilled and dedicated people who had a goal to create a proof-of-concept cloud infrastructure and web platform. The concept they were trying to prove was whether a platform could be created with sufficient guardrails to allow developers to build the products they needed to but that would enforce just enough standards and quality to minimise outages and improve productivity.

The M&S engineers were deeply suspicious of consultancies and so we needed to start by just being their supporters and sharing some advice as well as coding alongside them to demonstrate we could walk the walk as well as we talked the talk.

M&S had defined some key features of the platform they wanted. They wanted it to be a cloud native implementation. They wanted CI/CD and they wanted React and Next.js because they liked them as a development environment and they wanted an off-the-shelf experimentation capability.

I knew that what they were trying to prove was possible with all the tools they wanted to use because I had just done something similar at Zoopla with a very similar tech stack. From a technical perspective this was going to be a reasonably standard modernisation programme.

The **identifiable pattern of actions that when performed in similar conditions that will achieve predictable results.** was a React/Next.js Monorepo using ESLint, 100% code coverage and all the scanning solutions security demanded deploying into Azure Service Apps.

The interesting parts of working at M&S were how we built trust with the M&S people. We wanted a seat at the table when decisions were being made so we could be confident that the M&S team had heard a wide range of ideas before making their decision. We implemented a Decision Log that we kept in Github, we ensured there were always at least three people involved in laying out the options and choosing one. Given the size of the team at the time this gave us lots of opportunity to be included in the conversation. Even if we weren't the decision log process allowed a period for options to be added and decisions to be discussed.

