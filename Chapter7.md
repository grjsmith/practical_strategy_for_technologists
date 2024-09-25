# Chapter 7: 20th Century tools

In the last two chapters we examined some of tactics espoused by the most influential strategic political and military thinkers from the past.

This chapter aims to introduce some modern 20th and 21st century tools that can be useful when designing a tactical approach.

## Conway's Law and the inverse Conway manoeuver

This sounds like something out of Star Trek but it’s the name given to a statement made by a real software engineer named Melvin Conway. In 1967 Conway wrote: Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure (https://en.wikipedia.org/wiki/Conway%27s_law).

Dubbed Conway’s law this observation has been tested and reinterpreted many times. There’s a commonly accepted extension to the law that for a long-lived piece of software its architecture comes to resemble every iteration of the organization that created it.

A very simplistic interpretation of this tells us that if we have a web team and a backend team and a database team our software architecture will likely have a separate web service, backend service and some databases. Regardless of what we want the software to do.

More specifically if that database team are all Oracle experts you’re likely to have Oracle databases whether that’s the best solution or not.

It’s important to remember though, Conway never said that system architecture will reflect the organization structure. In simple cases it probably will but Conway said the system design will be a copy of the organization's communication structure. This has much broader implications than just the org chart.

A common debate in the industry at the moment is whether websites should be built in a monorepo or with multiple repositories. The debate has several technical angles, but technology is not the major outcome of this decision. In a monorepo all the code for the site is merged into one code repository. No matter how many teams are working on it they merge all their code together. This brings several technical advantages. It’s simple to build shared components just once and have every component, page and site have access to them. Standards can be implemented in one place and be universally applied. End to end tests can be executed in the build pipeline and test every page and interaction required regardless of which team built it.

All of these advantages become more difficult to achieve when building a site across multiple repositories. A common pattern is for each page to be in its own repository. There are usually smaller, simpler pages that don’t undergo as much change and they might be grouped together. When each page or a group of pages each have their own repository they can’t easily share components with each other. There are some approaches to help with this but they all require additional technology to build them and they all require maintenance. If an end-to-end test is required it needs to be built outside of the flow of building each page, it’s an additional overhead with additional costs and a maintenance burden. Standards have to be applied to each repository, again this requires a solution either copying and pasting standards into each repo and trying to keep them all up-to-date or building some technical solution to apply those standards across all the repos.

The cost of a monorepo is that engineers wanting to make changes to the site need to merge their code with all the rest of the code. While they are trying to do this all the other engineers are trying to merge their code too. Only one version of the codebase can be authoritative at one time so only one merge can happen at once. This creates what’s called a merge queue and means some engineers will need to rebase their local version of the code and try merging again. In an organization with lots of engineers this can lead to frustrating delays.

There is a simple non-technical solution to this problem. The engineers can all get in a chat channel and announce when they want to merge and discuss the order they want to merge in to ensure urgent changes are made first and high profile changes get a little extra attention.

If you’re not an engineer this might sound like a great solution and I think you’d be right. Software engineers usually hate the idea of this. This is often considered to be friction. Having to talk to each other gets in the way of the engineering workflow. This is an example of Conway’s law in action. If an organization values its engineers talking to each other and taking a shared responsibility for the site and helping each other they might choose to mandate a monorepo solution because one shared communication channel for all the engineers, mirrors one shared codebase that all the engineers work on and take accountability for. This is what we built at Zoopla, for precisely these reasons, we wanted a culture of sharing, collaboration and mutual support.

The Inverse Conway manoeuver was created by Jonny LeRoy and Matt Simons in a 2010 article in the Cutter IT journal. The Inverse Conway manoeuver describes a process whereby an organization is designed or reorganized  specifically to build and support a particular software architecture.

Just Eat circa 2016 were a great example of this, as with many successful technology organizations Just Eat had built a software monolith but unlike many other technology companies Just Eat actually managed to decompose their monolith. Just Eat formed their teams around the major components they wanted in their platform. There was a Search team, a Menu team, a Restaurant team etc. and each team built what they needed to in order to achieve the KPIs they agreed to meet and the features they agreed to provide. The advantage of this approach is that there were a whole host of problems that could be left up to the teams to resolve that didn’t require any centralized decision making.

The downside of this approach is that no one team was accountable for the quality of the platform as a whole. Resolving that problem involved creating several new teams who could identify where a problem needed resolution and were empowered to get the relevant team to resolve that problem. There was the service management team who, amongst other things, helped teams understand how their cloud costs were changing and helped run initiatives to reduce costs. There was an operations centre team who actively monitored the service and the platform during peak hours and highlighted anomalies that needed to be investigated. They, later, took on a function of helping check that new services entering production were ready for production loads. There were several Site Reliability Engineering teams that developed tools for the teams to use to manage their deployments, observability and security.

Conway's Law and the Inverse Conway Manoeuver can both be tested backwards and forwards. It is possible to draw a system architecture and compare it to the organizations communication structure and flows and see where they match and where they don't. Likewise, once an organization's communication patterns are understood a software architecture can be designed. This provides the tactician with a great opportunity to test their ideas. If the architecture required doesn't match the communications patterns then the tactician knows that the architecture will not stay as it is for long. Human communications are much more resistent to change than software.

## The OODA Loop

The OODA Loop was created by Colonel John Boyd, a US Air Force fighter pilot. Colonel Boyd recognized that rapid decision making was essential in aerial combat and larger, longer running military operations. The OODA loop is a decision making framework that has come to be a staple in legal, political and military strategy circles.

The success of any large undertaking requires rapid, good quality decisions. This ensures momentum is gained and retained. It ensures that opportunities can be taken advantage of and that risks are managed before they develop a momentum that can pose a significant threat.

The OODA loop defines good decision making as a loop. Each action taken creates new situations which, in turn, require actions to be taken or may cause adversaries to take action which, in turn, necessitate further actions.

One complete loop requires an observation, orientation of that observation in a wider context, a decision about what to do about the observed situation and an action taken.

The idea behind the OODA loop is that if a full cycle of the loop can be traversed faster than the situation observed can evolve then the situation can be mitigated and resolved through good decision making. Proponents of the OODA loop maintain that if two full cycles of the loop can be traversed before the situation being observed can evolve then the situation will resolve itself because it won’t have the opportunity to cause any significant impact.

### Observation

Making good observations can be an extremely complicated and expensive activity in its own right. In technology we often need to buy observability tools, and we certainly need to spend a significant amount of time configuring tools and configuring our applications to be able to provide these tools with the right data so we can observe the behavior of our applications. We also need to provide the costs for running the applications to the finance organization so it can be determined whether the application is profitable.

This is just for simple technical solutions. It’s even more complicated to observe teams to determine what they are doing and how well they are doing it.

One of the principals of the agile development movement was to break work down into smaller deliverables so that they can be scoped, tackled and delivered in a few weeks. Delivered in this case means demonstrating what was learned and what was built to the stakeholders so they can confirm the team is on the right track or provide feedback to allow the team to correct their course, so the products eventually created meet stakeholder expectations.

The logic behind this principle seems to have been lost. Engineering teams seem to do sprints for their own sake or adopt Kanban so they don’t feel pressured to work to a fixed timescale. Technology leaders ask for ways to measure productivity and velocity when the ultimate measure of this is to judge what a team has learned and achieved over a period of time. Team demos where they show their stakeholders what they have scoped and built and learned are the ultimate measure of productivity. If a team is deemed to be under-performing, based on stakeholder expectations the stakeholders should review the demo and talk to the team to determine what friction they’re experiencing and help to remove that friction or reset their expectations.

If we do all of this right we can know that our applications are functioning,  how well they are performing for the customer and we can know whether our teams are functioning and what friction they are experiencing.

The next question is how well our products are meeting our customers' needs. That’s where user research, product management and product design come in.

If those functions are established and have the people, skills and resources they need then combined with the technical and functional data we can observe our applications and their performance.

As can be seen above, simply making observations is expensive, difficult and time consuming. Orienting those observations in a wider context is uncertain, speculative and, very likely, contentious.

### Orientation

Observation is difficult and expensive and we have direct access to the people, processes and technologies that we need information about. We seldom have direct access to trusted information about the environment our organizations are operating in. We don't know the state and plans or our competitors. Separating facts from marketing about the latest, relevant developments in the industry is a challenge. The real needs of our customers, shareholders and investors are difficult to separate from what they say they want. The state of third party systems we’re dependant on such CRMs, ERPs, and the companies that produce them is a complex mesh of disinformation. The state of our customer's devices that they run our applications on is another unknown, particularly as there are so many possible variations of operating system, browser and app versions.

Orientation requires a continual process of observation and speculation about the operating environment, industry, politics, local and global economy and technology so there is a background of information that can be used to orient a specific observation.

### Decide

If an observation, oriented in context, requires action a decision must be taken. There can be a reasonable degree of certainty about the observations. There is much less certainty around the orientation so decisions are never certain to produce the desired outcome. This means every decision carries risk. If an organization has not taken care to create a system that empowers good decision making then a decision will require meeting after meeting. In an extreme case those meetings continue until the options diminish to one and then a decision is forced on the organization. Many organizations accept this as decision making when actually decisions are not being taken at all.

There are many ways to facilitate good decision making. There can be a structural approach where the organization structure is associated with levels of authority and accountability. This creates a benign dictatorship where decisions sit with an individual. This doesn’t preclude the leaders of these organizations establishing their own decision making systems, including committees, consultancy or anything else but it does force accountability for the outcomes of decisions they take. There are systemic solutions where decision-making processes are agreed upon in advance and then accountability for the outcome of decisions is shared between those accountable for the decision-making systems and those responsible for executing the processes. A common example of a systemic approach to decision making is a hiring panel or a scoring matrix for selecting suppliers.

### Action

Deciding to take an action doesn’t resolve the situation being observed. Taking action isn’t a point in time, it's a process in its own right. In technology taking action will likely mean creating or optimizing some software, reconfiguring a system or restructuring some data or even building a team to tackle some or all of those actions. This is why it’s important to have accurate observations, a good background of information with which to orient those observations and a rapid and robust approach to decision making. Actually taking action will be expensive and time consuming and will no doubt require more detailed decision making so it’s important to make the right decisions because the wrong decisions will cost the organization three times. Once in the time taken to make the decision in the first place, a second time to undo whatever mistaken actions were made and a third time to traverse the loop again.

I mentioned earlier that at the DWP the initiative to bring a centralized approach to DevOps and Public Cloud faced two groups of adversaries. The first and most obvious group of adversaries were the teams trying to bring services to citizens and I’ve described how their adversarial nature was born from past experience and a desire to do the right thing and not be held up by unnecessary bureaucracy. The second and less obvious adversary was the CTO. The threat he posed to us was distraction. As his calendar allowed he would come into the department to check up on us and ensure we were making good progress towards his grand strategy. Unfortunately alongside this diligence came a passion for technology and a lack of awareness for how powerful his voice was. While receiving the demos and getting excited for the progress he would ask if we had plans to implement this technology or that technology and our leadership felt compelled to tell him we would and our teams would be distracted by those requests.

My solution to this problem was the OODA loop. I didn’t have the authority or the opportunity to work with the CTO directly, the DWP was very hierarchical so I couldn’t counsel him or manage his enthusiasm. What I could do was implement a framework for observation, orientation, decision making and action. We expanded our relationships, we learned what technologies were being discussed, we oriented those observations against the backdrop of our next priorities and our capabilities. We made sure that we took action to have some useful demonstrable capability that would allow us to conclude any conversation about additional scope.

The next time the CTO came by to check on us and asked if we had plans to be able to deploy Docker containers. We had already spoken to the team in Pensions who were speculating about Docker and the Universal Credit team that had spiked it and we had an alpha version ready to present. We were able to repeat this successfully several times.

It can be argued that the OODA loop isn’t a tactic; that it’s a tool for decision making. Many organizations are so poor at decision making that, for them, implementing an OODA loop is a first tactic they need to implement because without that no other tactics could be executed.

OODA loops can be tested just as easily as an organizations existing OODA loop can be identified. The advantage of testing the OODA loop is that it's helpful to face the organization with the decisions it's made about decision making. For example if the CEO needs to sign off on every spend over 50,000 and the organization needs to do that 10x a year then it's easy to see that with a normal CEO calendar it will require a herculean effort to chase down that sign-off. That can then lead to a productive conversation about whether the sign-off amount should changed, whether sign-off authority should be devolved, whether an improved sign-off process is required or even whether that is an appropriate amount of friction given the current state of the business.

## Two way doors

Strategies allow for a great deal of flexibility. Within a strategy it can be possible to adapt to new information potentially changing the tactics while leaving the strategy intact and still relevant.

A great example of this adaptability is the concept of two way doors. A two way door describes a decision that can be made that can be changed later without having to undo or redo a lot of work.

A great example of a two way door in technology is whether to build a monolith or a microservice architecture when building a new piece of software. The mistake many people make when thinking about this is considering only the most extreme examples of these two architectures. They imagine a monolith that has been modified and adapted, under pressure, for years. They imagine a mess of unpredictable dependencies that are impractical to test. Failing that, they imagine hundreds of serverless functions and containers orchestrated in undocumented ways with one or two functions in each so that it’s impossible to track a single transaction through the system.

It is perfectly possible to design and build a monolithic application that has clearly segregated functions, that is well tested and easy to change. Likewise it's possible to build a microservice architecture that is riddled with un-managed dependencies and lacks tests.

Two way doors is a great pattern to use to architect a system to have the right level of scalability and accountability.

For best results use domain driven design to break a big problem into smaller problems that are appropriately isolated from one another.

## Combining tactics

Combining DDD and the inverse Conway manoeuver helps the tactician identify exactly what problems need to be solved and provides an organizational structure that can solve those problems. In addition it creates the first draft of a high-level system architecture diagram that can be tested by engineers.

Adding a decision making framework that ensures a rapid OODA loop provides a way to quickly respond to the difficulties that will arise as the environment changes or hidden problems are uncovered.

## Operating models

The end goal of all of this work can be an operating model. Operating models are a one page description of how the people, processes and technologies work together to deliver the products to customers, generate data and insights and how all of it is governed.

Target operating models need to take 6 things into account:

<img src="images/Target_operating_model_TOM_small.png" alt="target operating model diagram showing functions, people, tech, service delivery, insight and governance">

Operating models are a useful communication tool but they are also useful because they allow leadership teams to talk about how value is generated without having to get into the detail of individuals and their teams.

The organizations essential functions, how many people and what skills they might have, the technology needed, how services will be delivered and to what standards, the data needed to inform future decision making and the necessary governance can all be discussed safely.

Once an operating model exists it can then be tested with as many real-world cases as necessary to give the leadership confidence that it will provide the required results.

In larger organizations budget processes can create pressure that has lead to duplicate functions in silos. Operating models will clearly identify that duplication. The decision can then be made to determine what to do about that. If it's felt that a single centralized solution might be preferable an operating model can be created and tested to determine what impact that might have on productivity, communications and the org chart.

The most important function of an operating models is testing. The implications of any proposed changes can be tested against the operating model to determine what might improve and what might get more difficult.

Once an operating model has been created then an organizational structure can be designed. Organizational structures can also be tested in a similar way and from organizational structures can flow career frameworks and job specifications and that very quickly leads to execution.

## Conclusion

In this chapter we have examined a handful of tools that the tactician can use to inform an organization about the changes it might need to make in order to deliver a strategy.

More importantly each tool can act as a test of the previous ideas facilitating a useful fast feedback loop for even the most ambitious ideas.