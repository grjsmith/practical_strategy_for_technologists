# Chapter 1: Introduction to strategy

Throughout my career I’ve been a part of many meetings that were trying to be defining strategies.. I now realise that none of these meetings actually defined strategies. Those groups created mission statements, vision documents and smart goals and OKRs. From time to time I would research strategy and never found anything written for product and technology businesses.  This is the book I wished I’d found when I was trying to understand what strategy is and how it might be valuable to me and my fellow engineers.

The purpose of this first chapter is to examine the definition of strategy. In addition this chapter will look at some simple strategies and examples of using them and  introduce the concept of a grand strategy.

## The definition of strategy

The dictionary definitions of strategy are unhelpful. There are several different dictionaries in use throughout the world, and generally, their definitions of strategy run along these lines:


>**strategy** /ˈstratɪdʒi/ (noun).
>
>1. a plan of action designed to achieve a long-term or overall aim.
>"time to develop a coherent economic strategy"
>
>2. the art of planning and directing overall military operations and movements in a war or battle.
>"he was a genius when it came to military strategy"

This seems to suggest that a strategy is just a plan that spans a long time period or it’s only useful in the context of war. That doesn’t seem right. If that were true why would there be sales strategies, marketing strategies and technology strategies. If strategies were just plans then why aren’t project managers writing them?

As the oldest human organisation the military has developed and used strategies for much longer than anyone else which may be why it’s so prominent in dictionary definitions. Even if you're completely new to the concept of strategy you've probably heard of a couple of military strategies for example The Pincer Movement or the Trojan horse.

In military terms The Pincer Movement is an attack where an adversary is caught between two forces and forced to deal with both simultaneously and ideally fall into chaos or retreat, either way the adversary is removed from the objective.

Everyone knows the story of the Trojan horse. A besieging force left a giant horse statue as a tribute for the city they were besieging. Later that night after the statue was brought into the city soldiers snuck out who could open the gates and lead their forces to take the city.
The pincer movement and the Trojan horse are both characterised by the fact that they can be reused in similar situations to achieve the same results.

Perhaps a better definition of a strategy might be:

**An identifiable pattern of actions that when performed in similar conditions will achieve predictable results.**

## Applying military strategies in modern business

Given the military's long history of working with strategy they are potentially a huge resource for us to draw upon when thinking about the problems we face in business.

Let’s start with the Pincer Movement. In technology our adversary is never an opposing force, it's a problem we need to overcome. Consider a problem on an e-commerce site. Customers are trying to place orders but they aren’t getting to a payment screen. The engineers would look in two or even three  places simultaneously. They would look at the application server logs looking for errors and at the data stores and or event messages to see if there are any problems persisting the transaction or any problems the next function has of trying to read that data.

By tackling the problem on two fronts the teams could whittle away at the problem piece by piece.

Considering problems as adversaries means many tried and tested strategies from military and business history become available. Let’s take a look at another example.

## Defensive Strategies

There are defensive strategies as well as aggressive strategies. Consider a multi-layered network design that increases security by decreasing the attack vector with each layer of the network.

In its simplest implementation web sites are connected to the internet but only allow a single port to access them. They in-turn connect to applications via an API layer that only allows the web servers to connect on that same SSH port. These API servers are then the only servers allowed to connect to the data sources and again only on the port specifically configured for those data sources.

This describes the classic concentric ring security model. The image on the right (Image courtesy of West Lothian Archaeological Trust, Jim Knowles, Frank Scott and John Wells) shows an aerial view of an ancient Ring fort.

<img src="images/Concentric Ring Security (1).png" alt="concentric ring security model" style=width:300px><img src="images/Multivallate_Ringfort_at_Rathrar_(Rathbarna_Enclosure_Complex),_Co_Roscommon,_Ireland.jpg" alt="aerial photo of a ringfort" style=width:300px align=right>
<br />

These are defensive strategies. When executed in the service of providing web applications to the internet it will work in any number of different situations. It can be deployed in AWS, Azure, Google Cloud Platform, in Data Centres, managed hosting services and various specialist Platform As A Service (PAAS) solutions or any combination of those hosting solutions. It will work with any programming languages, frameworks and for any data source be it SQL, NoSQL or a document data store. In the military and private security contexts this is also known as the Perimeter Security Model. This strategy was used to construct fortifications for thousands of years and is just as useful today in a technology context.

I can speak to anyone with security, network engineering or infrastructure skills and discuss perimeter security or the concentric ring model and they’ll instantly have a mental model that we can discuss in more detail. This is one of the great powers of strategy. A strategy is a pattern and humans are natural pattern matching machines.

## The importance of planning

When tackling larger problems or problems that, by their nature, require more time to solve, plans will often prove inadequate on their own. Plans are useful for solving short-term problems that are limited in scope. The reason why plans are not useful for larger or longer term initiatives is that they are easily disrupted. Hence the expression: 

>"no plan survives contact with the enemy" Helmuth von Moltke the Elder.

There's no such saying about strategy.

In technology when tackling short-term objectives with a small number of reasonably mature teams with a capable delivery management structure it is possible to create an accurate plan for about 6 weeks. Any further out than that and the potential for disruption  increases to the point where it can't be planned for. This disruption can take many forms: funding for the project can be revoked, a new company could be acquired, important members of the team can leave, essential dependencies such as infrastructure or core libraries might become unavailable or not behave as expected. Even if these dramatic events don’t occur small changes will. A good delivery manager will keep on top of these changes. They will lead mitigation attempts, replanning and re-scoping but the longer this goes on for the more likely it is that these will overwhelm the teams. Seemingly small disruptions can have a chaotic effect and end up having a much larger impact than was initially predicted.

Strategies can be useful at almost any scale and over medium or long timescales ranging from months to years. Multiple strategies can be chosen and layered to protect initiatives or the teams tackling certain problems. Strategies can provide a flexible structure within which short-term plans can be successful.

>“Plans are worthless, but planning is everything.” Dwight D. Eisenhower.

When facing a poorly defined problem the act of planning, particularly with a small group of well informed and motivated people can create the boundaries of a problem and through that process define the problem to be solved. Usually this process will also lead to an approximate definition of several surrounding problems that might otherwise disrupt the efforts of the team solving the primary problem.

Once problems are well understood, strategies can be identified. then plans, informed by those strategies, can be developed. Systems can be implemented that allow plans to be followed over short timescales and the process repeated. Scrum is an excellent method to work in this way. It won’t be successful for long on its own but supported by strategic thinking it is incredibly powerful.

Plans are essential when interacting with teams who have hard deadlines like marketing, advertising or supply chains. This is where teams without strategies struggle the most.

## Grand Strategy

Grand strategy exists to encompass the state that will be achieved once the strategies have done their jobs. In terms of nations and military strategies the grand strategy presents solutions to winning the peace once the war has been won.

In a business context a grand strategy will describe how an organisation will achieve the culture and capabilities it needs to thrive once it has dealt with the immediate problems blocking its progress.

At Zoopla we had just released our new technology stack. We had been instructed to not make any design changes to the new search page, partly because we lacked designers but also because when we started the work we didn’t have any product managers to scope out those changes. To the rest of the business, who weren’t going to look at the code to see what was different, we had spent 8 months building exactly what they had before only this time it did the same things on mobile as it did on a PC. It was very underwhelming for everyone outside the technology department.

Multiple new teams had been formed and they were in the midst of adopting the new tech stack, scoping out what their new pages would do and what they would look like when it was announced that we were going to rebrand and run a marketing campaign to promote it. I was really excited by the prospect because the whole point of the new tech stack my teams had built was that we could make these sorts of changes very easily.

The Delivery Director, one of her delivery managers, a product manager and myself came together and we crafted a grand strategy. That isn’t what we called it at the time but that’s what it was.

First of all we ran a training exercise, this was just like a military training exercise. We organised a couple of ad hoc teams who had the right skills and as a fun Christmas event we had the two teams do a fake rebrand. Design got on board and designed some hideous logos, iconography and chose some horrible fonts. We did stupid things like making spacing huge and borders visible so it was very obvious what had changed. The teams ran for one day and rebranded and redesigned as much of the site as they could.

This achieved exactly the same things as military exercises do. It gave the engineers and designers confidence that we could do the rebrand. It gave marketing and the technology leaders confidence and we found a bunch of things that didn’t work that we could add to the backlogs of our teams to get resolved before we had to do the rebrand for real. We presented the new hideous pages to the rest of the company and everyone enjoyed the results.

Having completed the exercise and got the fixes on to the backlogs the delivery manager started working with Design, Marketing, Product Marketing, Product Management and the product and technology leadership to form them into a steering committee that could review the work and make decisions but in an organised way that wouldn’t cause mixed communications and risk derailing the programme. We had seen evidence that Zoopla was going to run more of these programmes that involved multiple teams coordinating their work. The leadership didn’t necessarily agree or didn’t think  this kind of work needed different management than just in-team delivery management.  So another goal of ours was to demonstrate what programme management meant in an agile context.

The Delivery Manager got the steering committee started on some early decision-making to design a strategy for the rebrand itself.  This involved creating a prioritised list of rebrand activities. He used this to create layers of scope. So the first priority was a new logo and some basic colour changes. Another layer of scope was spacing, typography and some menu and line type elements. Finally came new fonts and more complex changes. Those of us close to the tech were very confident that all of this could be completed in the time we had but the Delivery Manager used this layered scope approach to de-risk the programme, take pressure off the teams and cause the steering committee to coalesce into a team used to working together to make decisions. This was no mean feat given these people probably spent less than an hour together every week. This last part was all part of the effort to show how programmes could be run.

The rebrand came together and launched without any hitches, it was a bit of an anticlimax. The leadership team won some kudos with their peers in other departments. We demonstrated what a programme could look like and shortly after that we started recruiting for Programme Managers. I had almost no involvement beyond the training day but I was happy that we’d demonstrated how good the new tech stack was. The product and technology organisation got a significant morale boost too.

Grand Strategies are complex, they aren’t for tackling a single objective but they are useful for getting a large and disparate group focussed on a shared set of objectives and they give those crafting them great flexibility.

## Conclusion

Strategies aren’t plans, they aren’t mission statements, visions, goals, policies or anything else. Strategies are: **An identifiable pattern of actions that when performed in similar conditions will achieve the same results each time**. As such they offer the strategist a high degree of confidence of success.

Mission statements, visions, goals, policies and plans all have their use and their place, as does strategy. Some of these things can be used in service of strategic objectives and they will be presented in that context later in the book.

If the strategist considers problems as their adversary or enemy that must be overcome then they gain access to thousands of years worth of battle-tested military strategies from every culture in the world. Study of these strategies will present solutions to a wide range of problems.
