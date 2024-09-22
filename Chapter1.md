# Chapter 1: Strategy, Tactics and Planning

## Strategy

The word strategy is over-used and often misused to the point where it's almost become meaningless. The dictionary definition of strategy isn't very helpful in helping us understand what a strategy is. There are several different dictionaries in use throughout the world their definitions of strategy tend run along these lines:

>**strategy** /ˈstratɪdʒi/ (noun).
>
> a plan of action designed to achieve a long-term or overall aim. "time to develop a coherent economic strategy"
>
> the art of planning and directing overall military operations and movements in a war or battle.
>"he was a genius when it came to military strategy"

Richard Rumelt, author of Good Strategy/Bad Strategy, in an interview with Mckinsey once described Strategy as:

>Strategy is problem-solving. It is how you overcome the obstacles that stand between where you are and what you want to achieve.

(source: https://www.mckinsey.com/capabilities/strategy-and-corporate-finance/our-insights/why-bad-strategy-is-a-social-contagion)

That's as good a definition as any for us to work with. A strategy is _how_ an organization overcomes the obstacles that stand in the way of their success.

Strategies are usually unique to an organization, their environment, the prevailing economic conditions and what they are trying to achieve. As such there are few reusable strategies. Some notable examples of strategies include:

- Southwest airlines' Greyhound for the skies strategy
- Apple's ecosystem strategy
- AOL's so easy we're number one

Southwest Airlines disrupted domestic air travel in the US by deliberately offering what their competition didn't. They flew point-to-point to smaller locations and alternative airports in larger cities. They offered price-conscious travelers an alternative to their cars and busses.

Apple's technology is based on well-respected open standards software and hardware and yet Apple products only work well with Apple software and other Apple devices. This is a concerted strategy to up-sell and cross-sell things customers already have so they can use those things with their apple products. This strategy has been wildly successful for Apple making it one of the most valuable companies in the world.

America Online was just another internet service provider in 1999 but a focus on offering a premium service catering specifically for non-technical people propelled it to being the biggest internet service provider in the world during the early 2000's.

These strategies are all unique to the industry, the company that created them and the time in which they were operating. Their competitors were forced to adapt either with their own strategies or by improving their operational efficiency.

When a large organization wants to change itself, it's capabilities or make some significant impact on the world it will either create a strategy or attempt to optimize it's operational efficiency.

What happens next is what we'll examine in this book. Once an organization has a strategy, they have defined how they want to achieve success. What happens next?

As suggested by the title of this chapter the answer isn't planning. Planning is what we do once we know what we need our teams to achieve. There is an essential step between formulating a strategy and building a plan and executing it. That step is identifying, defining and designing tactics.

## Tactics

Strategies are, by their nature, unique to a company, industry and even the time-period they are operating in. Tactics are not unique. **Tactics are patterns of activities that people perform in order to achieve a strategic objective**. Tactics are a way of describing a complex pattern of activities in a simple way. 

Let's examine some simple tactics everyone has heard of: the Pincer movement and the Trojan horse. The Pincer Movement is an attack where an adversary is caught between two forces and forced to deal with both simultaneously.

Everyone knows the story of the Trojan horse. A besieging force left a giant horse statue as a tribute for the city they were besieging. Later that night after the statue was brought into the city, soldiers snuck out and opened the gates allowing their forces to take the city.

The pincer movement and the Trojan horse are both easily recognized patterns of activities. They can also be reused in similar situations to achieve the same results.

In technology our adversary is never an opposing force, it's a problem we need to overcome. Consider a problem on an e-commerce site. Customers are trying to place orders but they aren’t getting to a payment screen. Engineers trying to identify the problem will look in two places at once. They will look at the application server logs for errors. They will also graph metrics from the data stores and event messages to see how far transactions were getting before they failed. In this scenario the engineers would split their forces to attack the problem from two sides simultaneously. They perform a Pincer movement on the problem.

The term "Trojan Horse" has come to mean any tactic that allows someone to gain access through false pretenses. A malicious piece of software that masquerades as something innocent is known as a Trojan.

Considering problems as adversaries allows a tactician to pull inspiration from throughout military history.

## Defensive tactics

There are defensive tactics as well as aggressive ones. Consider a multi-layered network design that increases security by decreasing the attack vector with each layer of the network.

In its simplest implementation web sites are connected to the internet but only allow connections over a single port to access them. They in-turn connect to applications via an API layer that only allows the web servers to connect on a specific port. This API gateway requires authentication and connects to the backend servers which are the only servers allowed to connect to the data sources and again only on the port specifically configured for those data sources. This describes the classic concentric ring security model.

The image on the right shows an aerial view of an ancient Ring fort. The similarities are obvious and this isn't just correlation, this is causation. The rings in a ring fort and the layers in a security model serve the same purpose. They are both trying to slow down an invader. They are both trying to protect increasingly valuable assets.


<img src="images/Concentric Ring Security (1).png" alt="concentric ring security model" style=width:300px><img src="images/Multivallate_Ringfort_at_Rathrar_(Rathbarna_Enclosure_Complex),_Co_Roscommon,_Ireland.jpg" alt="aerial photo of a ring fort" style=width:300px align=right>

<br />
Image courtesy of West Lothian Archaeological Trust, Jim Knowles, Frank Scott and John Wells.
<br />
<br />

These are defensive tactics. This approach will work in AWS, Azure and Google Cloud Platform. It will work in Data Centres, managed hosting facilities and specialist Platform-As-A-Service (PAAS) solutions. This tactic will work regardless of the programming languages or the frameworks being used. It will work for any data source be it SQL, NoSQL, or a document data store.

In military and security contexts this is also known as the Perimeter Security Model. This strategy has been used to construct fortifications for thousands of years and is just as useful today in a modern technology business. Anyone with a security, network or infrastructure background will already have a mental model of the concentric ring model. This is one of the great powers of tactics. A tactic is a pattern and humans are pattern matching machines. Just saying to an engineer that we're going to be using a concentric ring model can shortcut hours of conversation.

This is the power of tactics. They are memes, they are little stories that stick in people's heads. No matter how a persons brain works they will be able to conjure a mental model of a tactic. 

From these examples we can consider that **tactics are patterns of behavior that when used in similar situations can achieve repeatable results.**

Unfortunately tactics aren't taught to aspiring leaders. As we mature and grow in our professions we are taught to focus on details and planning. Later we start to learn about strategy. Many leaders will have a favorite strategy book and they might recommend their team read the book, as a part of bringing the team together around a strategic approach. We completely skip over tactics. In nearly 30 years working for technology organizations I have ever heard anyone discuss tactics. I have heard people discuss strategy, when they meant tactics. I have made this mistake myself many times. It was only when I talked to ex-military people did I begin to realize that the military deals almost exclusively with tactics. Strategy is something created by the most senior people, that most military people don't interact with on a daily basis. The rest of the officers are trained on tactical implementation, as a tool, to implement strategy with their teams.

If you've ever been part of a team and unsure how your team is contributing to the organization's strategy then you are not alone. Very few organizations understand the link between strategy, tactics and planning well enough to explain them to their people or use them to create alignment and a shared sense of purpose.

## The importance of planning

Plans are most useful for team level short term initiatives because they are so easily disrupted. Hence the expression:
> "no plan survives contact with the enemy"

Helmuth von Moltke the Elder.

A mature team, with a few small objectives, and good delivery management, can create an accurate plan covering a 6 week timescale. Any further out than that and the potential for disruption starts to impact the accuracy. This disruption can take many forms. Funding for the project can be revoked. Company or department priorities can change. Members of the team can leave. Essential dependencies can become unavailable or incompatible. Even if these events don’t occur other small changes will. A good delivery manager or delivery focused product or engineering manager can keep on top of these changes. They can lead mitigation efforts. They can re-plan and lead re-scoping efforts. The longer this goes on for the more likely it is that these will overwhelm the team and the initiative. Several small disruptions can have an outsize effect. This is particularly true in organizations with un-managed dependencies, when any one team's action or inaction can disrupt any number of other teams.

Strategies and tactics can be used in concert to protect initiatives and teams. They can provide a flexible structure allowing short-term, team-level plans to be coordinated and prioritized together. This can lead to a more successful outcome than plans can on their own. Strategies provide a larger context that allows a team to test whether what they are working on is the right thing. Tactics provide a narrative or meme that's easy for everyone in the team and department to remember so they can talk to each other about what they're trying to achieve. This is particularly helpful when teams need to talk to each other about different aspects of the work. If one team seems to have have different priorities teams can use the tactics as a framework for a conversation about why one team seems to be working on something else.

> “Plans are worthless, but planning is everything.”

Dwight D. Eisenhower.

The act of planning, particularly with a small group of well informed and motivated people, can help to define the boundaries of a problem. This is particularly useful in product and technology departments where most problems are poorly defined. This process will lead to a good definition of the problem and the risks.

The mistake a lot of organizations make is to take these plans and attempt to execute them. What should happen, at this point is that the plans should be reviewed by the leadership team. They should look for unnecessary dependencies, or for opportunities to reduce risk across all the teams. This might involve using a platform-as-a-service offering, or outsourcing some mundane but essential work or just finding problems the teams couldn't see because of their closer perspective. Once that is done the planning exercise should be done again with a view to starting execution. The problem with attempting to launch an initiative based on the first planning round is that the people in the teams struggle to step outside of their team perspectives. This isn't a problem to be solved, this is what leadership teams are for. Too often leadership teams haven't spent the time to learn how to work together, as a team, and so pulling them together to review how team-level plans fit together is an enormous undertaking.

- Once problems are well defined, tactics can be identified that can be used to solve them.
- The plans, informed by those tactics, can then be developed by the teams.
- Systems and processes can be developed that increase the probability that plans are executed successfully.

Plans are essential when interacting with teams who have hard deadlines like marketing, legal, advertising or supply chains. This is where teams without strategies, systems and processes struggle the most. To organizations like this planning seems like guess work at best and an opportunity to fail at worst.

### A Side note on Grand Strategy

Strategies are for solving problems. Grand Strategies are for creating organizations that can handle problems.

Grand strategy exists to encompass the state that will be achieved once the strategies have worked. In terms of nations and military strategies the grand strategy presents solutions to winning the peace once the war has been won. In a business context a grand strategy describes how an organization will achieve the culture and capabilities it needs to thrive.

In the summer of 2020 We had just released a new web technology stack at Zoopla. We had been instructed to not make any design changes to the new search page. There were a lot of reasons for this. The design and product function wasn't in place yet. The technology leadership wanted to compare like for like with the old and new tech stacks. To the rest of the business, who weren’t going to look at the code, we had spent 8 months building exactly what they had before. There were some SEO improvements  but it was underwhelming for everyone outside the technology department. 

I needed to prove that Zoopla could now do things that it couldn't do before. The challenge came in the form of a redesign, rebrand, and associated marketing campaign.

Zoopla hadn't been able to do a redesign for years. It was too difficult to make changes confidently across the old tech stacks.

We were confident that the tech stack would it's job. The new problem was that Zoopla had no systems or processes to run large, cross-team and cross-department initiatives. We needed a Grand Strategy to show Zoopla how it could easily shift between multiple product-led teams working independently to a large cross-team and cross-department programme where the teams were focused on a collective effort.

The first thing we did was run a training exercise, this was just like a military training exercise. We organized a couple of ad hoc teams who had the right skills and as a fun Christmas event we had the two teams do a fake rebrand. Design got on board and designed some hideous logos, iconography and chose some horrible fonts. We did stupid things like making the spacing huge and borders visible so it was very obvious what had changed. The teams ran for one day and rebranded and redesigned as much of the site as they could.

This achieved exactly the same things as military exercises do. It gave the engineers, designers and the leadership confidence that it was possible to rebrand. It also gave us the opportunity to fix a few of things that didn’t work quite right. We presented the new hideous pages to the rest of the company and everyone enjoyed the results.

With the exercise complete and the necessary fixes added to the backlogs it was time to prepare for the real thing. We pulled together a steering committee comprised of marketing, product and technology leaders. This committee would review the work and make decisions in an organized way that wouldn’t cause mixed communications and risk derailing the programme. We had seen evidence that Zoopla was going to run more of these programmes that involved multiple teams coordinating their work. The leadership didn’t necessarily agree or didn’t think  this kind of work needed different management than just in-team delivery management.  So another goal of ours was to demonstrate what programme management meant in an agile context.

The Delivery Manager got the steering committee started on some early decision-making to design a strategy for the rebrand itself.  This involved creating a prioritized list of rebrand activities. He used this to create layers of scope. So the first priority was a new logo and some basic color changes. Another layer of scope was spacing, typography and some menu elements. Finally came new fonts and more complex changes. Those of us close to the tech were confident that this could be completed in time. but the Delivery Manager used this layered scope approach to de-risk the programme. It took pressure off the teams and gave the opportunity for the steering committee to form into a team. This was no mean feat given these people probably spent less than an hour together every week. This last part was all part of the effort to show how formal programmes could be beneficial.

The rebrand came together and launched without any hitches, it was a bit of an anticlimax. The leadership team won some kudos with their peers in other departments. We demonstrated what programme management could look like in an agile environment and shortly after that we started recruiting for Programme Managers. I had almost no involvement beyond the training day. My lack of involvement meant that we had successfully  demonstrated that the new tech stack had done it's job.

Grand Strategies are complex but once the a strategy has been delivered they are the next stage of maturity for an organization.

## Conclusion

Strategies aren’t plans, they aren’t mission statements, visions, goals, policies or anything else.

>Strategy is problem-solving. It is how you overcome the obstacles that stand between where you are and what you want to achieve.

Tactics are how teams can engage with the strategy and plan confidently. ** Tactics are patterns of behavior that when used in similar situations can achieve repeatable results**

In considering problems as adversaries to be overcome tacticians get access to tactics proven over thousands of years from every culture in the world. Study of these tactics will provide ready-made solutions to a wide range of problems.