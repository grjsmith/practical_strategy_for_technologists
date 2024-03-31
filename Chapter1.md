# Chapter 1: Introduction to strategy

Throughout my career I’ve been a part of various meetings that trying to create strategies. I was never satisfied with the experience. I now realise that none of these meetings actually defined strategies. Over the years I’ve been part of groups creating mission statements, vision documents, policies, guidelines, plans and Objective and Key Results (OKR). I have, from time to time attempted to research strategy and struggled to find anything written for product and technology businesses. All I ever found were sales, marketing and social media strategies. The goal of this book  is to be the book that I wished I’d found when doing that research.

The purpose of this first chapter is to examine the definition of strategy. This chapter will look at some simple strategies and examples of using them.

## The definition of strategy

The dictionary definitions of strategy are unhelpful. There are several different dictionaries in use throughout the world their definitions of strategy tend run along these lines:

>**strategy** /ˈstratɪdʒi/ (noun).

>

>1. a plan of action designed to achieve a long-term or overall aim.

>"time to develop a coherent economic strategy"

>

>2. the art of planning and directing overall military operations and movements in a war or battle.

>"he was a genius when it came to military strategy"

This seems to suggest that a strategy is just a plan that spans a long time period or it’s only useful in the context of war. That doesn’t seem right. If that were true why would there be sales strategies, marketing strategies and technology strategies. If strategies were just plans then why aren’t project managers writing them?

As the oldest human organisation the military has developed and used strategies for much longer than anyone else. This may be why it’s so prominent in dictionary definitions. Even if you're completely new to the concept of strategy you've probably heard of a couple of military strategies. The Pincer Movement and the Trojan horse are some of the oldest and well known strategies.

The Pincer Movement is an attack where an adversary is caught between two forces and forced to deal with both simultaneously.

Everyone knows the story of the Trojan horse. A besieging force left a giant horse statue as a tribute for the city they were besieging. Later that night after the statue was brought into the city soldiers snuck out who could open the gates and lead their forces to take the city.

The pincer movement and the Trojan horse are both easily recognised patterns of behaviour. They can also be reused in similar situations to achieve the same results.

A mosre useful definition of a strategy might be:

An identifiable pattern of actions that when performed in similar conditions will achieve predictable results.

## Applying military strategies in modern business

Given the military's long history of working with strategy they are potentially a huge resource for us to draw upon when thinking about the problems we face in business.

Starting with the Pincer Movement. In technology our adversary is never an opposing force, it's a problem we need to overcome. Consider a problem on an e-commerce site. Customers are trying to place orders but they aren’t getting to a payment screen. The engineers would look in two places at once. They would look at the application server logs for errors. They would look at the data stores and or event messages to see how far transactions got.

Considering problems as adversaries allows the strategist to pull inspiration from miltary history.

# insert trojan horse example

## Defensive Strategies

There are defensive strategies as well as aggressive strategies. Consider a multi-layered network design that increases security by decreasing the attack vector with each layer of the network.

In its simplest implementation web sites are connected to the internet but only allow a single port to access them. They in-turn connect to applications via an API layer that only allows the web servers to connect on that same SSH port. These API servers are then the only servers allowed to connect to the data sources and again only on the port specifically configured for those data sources. This describes the classic concentric ring security model.

The image on the right shows an aerial view of an ancient Ringfort. The similarities are obvious and this isn't just correlation, this is causation. The rings in a ring fort and layers in a security model serve the same purpose. They are both trying to slow down an invader. They are both trying to protect increasingly valuable assets. Image courtesy of West Lothian Archaeological Trust, Jim Knowles, Frank Scott and John Wells.

<img src="images/Concentric Ring Security (1).png" alt="concentric ring security model" style=width:300px><img src="images/Multivallate_Ringfort_at_Rathrar_(Rathbarna_Enclosure_Complex),_Co_Roscommon,_Ireland.jpg" alt="aerial photo of a ringfort" style=width:300px align=right>

<br />

These are defensive strategies. This strategy provides a secure environment for web and mobile applications. This strategy can be employed  in AWS, Azure and Google Cloud Platform. It will work in Data Centres, managed hosting services and specialist PAAS solutions.  The strategy will work in any combination of hosting solutions. This strategy will work regardless of the programming languages or frameworks being used. It will work for any data source be it SQL, NoSQL, or a document data store. In the modern military and in private security contexts this is also known as the Perimeter Security Model. This strategy was used to construct fortifications for thousands of years and is just as useful today in a technology context.

Anyone with a security, network or infrastructure background will have a mental model of this strategy. This is one of the great powers of strategy. A strategy is a pattern and humans are pattern matching machines.

## The importance of planning

Plans are less useful for larger or longer term initiatives because they are easily disrupted. Hence the expression: "no plan survives contact with the enemy" Helmuth von Moltke the Elder.

In product and technology a mature team, with a few small objectives, and a good delivery management structure can create an accurate plan covering a 6 week timescale. Any further out than that and the potential for disruption starts to impact the accuracy. This disruption can take many forms. Funding for the project can be revoked. Company or department priorties can change. Members of the team can leave. Essential dependencies can become unavailable or incompatible. Even if these events don’t occur other small changes will. A good delivery manager can keep on top of these changes. The can lead mitigation efforts. They can replan and lead rescoping efforts.  The longer this goes on for the more likely it is that these will overwhelm the team and the initiative. Several small disruptions can have an outsize effect.

Strategies can used in concert to protect initiatives and teams. Strategies can provide a flexible structure allowing short-term plans to be successful.

>“Plans are worthless, but planning is everything.” Dwight D. Eisenhower.

The act of planning, particularly with a small group of well informed and motivated people, can define the boundaries of a problem. This is a particularly useful activity when the problem is poorly defined. This process will lead to a definition of the problem. This process will often lead to the definition of several surrounding problems that present risk to solving the primary problem.

Once problems are well understood, strategies can be identified to address the problem. Then plans, informed by those strategies, can be developed. Systems can be implemented that allow plans to be followed over short timescales and the process repeated. Scrum is an excellent method to work in this way. It won’t be successful for long on its own but supported by strategic thinking it is incredibly powerful.

Plans are essential when interacting with teams who have hard deadlines like marketing, advertising or supply chains. This is where teams without strategies struggle the most.

## Grand Strategy

Grand strategy exists to encompass the state that will be achieved once the strategies have done their jobs. In terms of nations and military strategies the grand strategy presents solutions to winning the peace once the war has been won.

In a business context a grand strategy will describe how an organisation will achieve the culture and capabilities it needs to thrive once it has dealt with the immediate problems blocking its progress.

At Zoopla we had just released our new technology stack. We had been instructed to not make any design changes to the new search page, partly because we lacked designers but also because when we started the work we didn’t have any product managers to scope out those changes. To the rest of the business, who weren’t going to look at the code to see what was different, we had spent 8 months building exactly what they had before only this time it did the same things on mobile as it did on a PC. It was very underwhelming for everyone outside the technology department.

Multiple new teams had been formed and they were in the midst of adopting the new tech stack, scoping out what their new pages would do and what they would look like when it was announced that we were going to rebrand and run a marketing campaign to promote it. I was really excited by the prospect because the whole point of the new tech stack my teams had built was that we could make these sorts of changes very easily.

The Delivery Director, one of her delivery managers, a product manager and myself came together and we crafted a grand strategy. That isn’t what we called it at the time but that’s what it was.

First of all we ran a training exercise, this was just like a military training exercise. We organised a couple of ad hoc teams who had the right skills and as a fun Christmas event we had the two teams do a fake rebrand. Design got on board and designed some hideous logos, iconography and chose some horrible fonts. We did stupid things like making spacing huge and borders visible so it was very obvious what had changed. The teams ran for one day and rebranded and redesigned as much of the site as they could.

This achieved exactly the same things as military exercises do. It gave the engineers and designers confidence that we could do the rebrand. It gave marketing and the technology leaders confidence and we found a bunch of things that didn’t work that we could add to the backlogs of our teams to get resolved before we had to do the rebrand for real. We presented the new hideous pages to the rest of the company and everyone enjoyed the results.

Having completed the exercise and got the fixes on to the backlogs the delivery manager started working with Design, Marketing, Product Marketing, Product Management and the product and technology leadership to form them into a steering committee that could review the work and make decisions but in an organised way that wouldn’t cause mixed communications and risk derailing the programme. We had seen evidence that Zoopla was going to run more of these programmes that involved multiple teams coordinating their work. The leadership didn’t necessarily agree or didn’t think  this kind of work needed different management than just in-team delivery management.  So another goal of ours was to demonstrate what programme management meant in an agile context.

The Delivery Manager got the steering committee started on some early decision-making to design a strategy for the rebrand itself.  This involved creating a prioritised list of rebrand activities. He used this to create layers of scope. So the first priority was a new logo and some basic colour changes. Another layer of scope was spacing, typography and some menu and line type elements. Finally came new fonts and more complex changes. Those of us close to the tech were very confident that all of this could be completed in the time we had but the Delivery Manager used this layered scope approach to de-risk the programme, take pressure off the teams and cause the steering committee to coalesce into a team used to working together to make decisions. This was no mean feat given these people probably spent less than an hour together every week. This last part was all part of the effort to show how programmes could be run.

The rebrand came together and launched without any hitches, it was a bit of an anticlimax. The leadership team won some kudos with their peers in other departments. We demonstrated what a programme could look like and shortly after that we started recruiting for Programme Managers. I had almost no involvement beyond the training day but I was happy that we’d demonstrated how good the new tech stack was. The product and technology organisation got a significant morale boost too.

Grand Strategies are complex, they aren’t for tackling a single objective but they are useful for getting a large and disparate group focussed on a shared set of objectives and they give those crafting them great flexibility.

## Conclusion

Strategies aren’t plans, they aren’t mission statements, visions, goals, policies or anything else. Strategies are: An identifiable pattern of actions that when performed in similar conditions will achieve the same results each time. As such they offer the strategist a high degree of confidence of success.

In considering problems as adversaries to be overcome we get access to strategies proven over thousands of years from every culture in the world. Study of these strategies will present solutions to a wide range of problems.