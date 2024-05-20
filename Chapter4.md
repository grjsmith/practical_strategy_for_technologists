# Chapter 4: Preparing for strategy

If a strategy is: **an identifiable pattern of actions that when performed in similar conditions will achieve the same results each time**. Then the key to a successful strategy is choosing the right pattern or patterns for the results that are needed.

The conditions that must to be managed in order to improve the chances of successfully executing a strategy have been examined in an earlier chapter. This chapter will examine how the strategist can define the results their strategies need to achieve. If the strategist knows that and can create the right conditions then they can select or design their strategy with confidence.

The first step towards formulating a strategy that can be successful is to define how the world must be different afterwards. People tend to think in terms of solutions, not in terms of problems. It’s very common for someone to explain what problem they’re having by explaining the solution they’re thinking of implementing. In almost all simple cases this is a useful trait, it helps people get to conclusions with less effort and less time. It’s a problem for the strategist because it becomes a habit. It gets over applied to more complicated problems that require detailed analysis.

When we were building the AOL Broadband Management System my first goal was to define the infrastructure it would need. I wasn’t allowed to spend any money but that was OK. AOL had a lot of infrastructure available and we found some servers that had originally been assigned to the London cache but never installed so I had some nice overspecified Sun servers available to me. Not long after the project started my director came storming up to me demanding to know where we’d get a Storage Attached Network (SAN). Thoughtworks said we needed one. When I asked why they said we needed one he explained that they  needed to store some configuration files that would be shared by multiple machines. After literally a moment’s thought I said: “Just write the files to every machine”. Problem solved. Originally destined to be cache servers, all the machines had a huge amount of disk space; a few extra config files would not be a problem. Both Thoughtworks and my Director had expressed the problem to me as a solution, the need for a SAN but in fact an expensive extra piece of infrastructure that would have added a long term maintenance burden to my team was not the right solution for that problem. By expressing the problem, as a problem, the need to access configuration information from each machine allowed me to solve the problem for free.

The advantage of taking a step back and ensuring you are working with the real problem is that in doing so you will be creating your case for your solution when it comes time to present it.

The Five Whys is an excellent tool to help with this. If you find yourself, either with a solution but no well defined problem, or you have a problem you’re struggling to articulate, the Five Whys will help you get to the root cause of the problem. After each question has been answered, you have an option to stop and choose to tackle the problem exposed at that level.

At M&S a few years ago I was proposing to the CTO that he should consider creating a temporary programme organisation that could add a little oversight and perspective to a large strategic initiative I was helping with. I suggested it could help with some of the wider reaching concerns he was expressing to his leadership team about how they were choosing which teams would get newly hired  engineers. It would also help coordinate bringing new teams on to the new technology solution we were developing. The CTO thought it looked like it would work but asked me why his people weren’t doing that sort of thing already. I thought of several possible reasons why they might not have thought of this but I couldn’t decide if it was due to one single root cause or a combination of factors.

After the meeting I got my people together, the ones who worked most closely with the organisation’s management, and I repeated the CTO’s question to them. Like me they all had ideas but nothing quite landed. On the call we ran a quick 5 Whys exercise to try to get to a root cause:

**Question:** Why aren’t M&S' senior management team thinking strategically about what's right for all of their teams in the context of the whole business?
<br>
**Answer:** They spend 40 hours a week in meetings focused on day-to-day operations. They don’t have time to think strategically.
<br>
**Question:** Why do they spend so much time in meetings all day?
<br>
**Answer:** Because they can’t make clear decisions in the meetings.
<br>
**Questions:** Why can’t they make clear decisions in the meetings?
<br>
**Answer:** They don’t have all the right people and information in the meetings, so they can’t make a decision and they need more meetings.
<br>
**Question:** Why don’t they have the right people in the meetings?
<br>
**Answer:** Because the decision making authority isn’t aligned across the hierarchy, decisions that have a financial impact, such as hiring more people or changing which department someone works in requires the most senior delivery person in the department. Those people have concerns that are above team level and aren’t usually in the meetings where team level concerns are discussed.
<br>
**Question:** Why isn’t the decision making authority aligned across the hierarchy?
<br>
**Answer:** No idea but that’s the right time to go back to the CTO and discuss what we’ve learned.

The Five Whys is a simple and powerful tool that helps you work backwards from a problem to get to a root cause. As such it's often used in post-incident reviews. It is recommended that it be used in a group, not just to spread the cognitive load but also to make sure there is enough information to answer all the questions.

## Principles, behaviours, processes, training and expectations

Having got to the root of the problem that needs to be solved the strategist now needs to understand what tools they have available to help them solve the problem. The most important consideration to understand is the people.

The military has been executing strategies longer than anyone else. It’s worth comparing and contrasting the way the military and business operate and how that impacts the execution of strategy. The military focuses a lot of time and money ensuring military personnel know what to expect of each other. This is summarised as training. Before a service person is asked to join their team and do their job they are subject to around a year of training. The training doesn’t end when they join their team. Specialisations and promotions sometimes require additional training and certifications. Service personnel are taught what to expect from each other and what to expect from their managers and their leadership. They are taught how to use their equipment and given significant time to practise with that equipment in different situations. Once they are in their teams they are trained alongside other teams so they can understand what’s expected of their team by other teams. Contrast that approach with technology organisations. Some large organisations have graduate programmes but they aren’t in every company. New engineers joining a technology company are often expected to be productive immediately. Engineers, new to an organisation, might have a completely different set of skills and expectations picked up from their previous companies. Companies are aware of this and so there is a tendency to choose technologies that are in common use. This is done so that  onboarding time can be minimised. Setting up development environments to work on legacy systems can still be challenging.

At Just Eat engineers owned and managed the services they built from start to finish. In my Site Reliability Engineering (SRE) department we put almost all of our energy into building and improving the tools the software engineers used to build and manage their services. This included the Amazon Web Services (AWS) cloud infrastructure. All the infrastructure-as-code (IAC) was Cloudformation and we stored variables in a Consul store. This meant that ideally we needed to hire software engineers that knew how to work with AWS. The interviews were primarily designed to assess whether the candidate was capable with C# and .Net, the language and ecosystem they’d be using to develop their services in. Most candidates were just asked: “Do you know AWS?” almost invariably they said yes and they were hired. It was common to find that they didn’t know AWS. None of them who came to us for help had ever lied in their interview. It was just that in their last company they only used AWS through the web console, or all the infrastructure was managed by someone else and all they had to do was run a command to deploy the application. Not having worked directly with infrastructure before meant they didn’t know there was more to it. We also encountered people who had been using other tools that managed AWS on their behalf but didn’t know they were because it was never explained to them. The most common support requests we received were simply due to the software engineer not knowing how to do something with AWS natively. This shows that when asked people can think they know something without actually knowing something, through no fault of their own. They just have a different set of expectations of what knowing something means than the questioner. We have pairing exercises that we use during the interview process to ensure we have similar expectations when it comes to programming but we can’t apply that process to every aspect of a role.

Technology organisations usually consider training to be a cost or even an employee benefit as opposed to an investment. Training is usually the first thing to get cut when economic conditions get tough. This always reminds me of the old joke:

**Manager 1:** “What if we train them and they leave?”
</br>
**Manager 2:** “what if we don’t train them and they stay!?”

Universities still aren’t preparing software engineers to enter the workforce. Many graduates have never developed software in a team, they’ve never tried to extract requirements from non-technical stakeholders. They’ve never needed to resolve an incident in the dead of night. They’ve never participated in a post-mortem or needed to deploy their code to a cloud. Universities are only giving them the most basic programming skills. This means new engineers face a daunting task when joining a new organisation. Coding boot camps exist that do emphasise these aspects of life as a software engineer but these are still relatively rare.

No strategy can be successful if the people involved can’t execute basic tasks. The strategist needs to lay some groundwork before they can hope to successfully execute their strategies. This groundwork might require specific strategies but more usually take the form of Principles, behaviours, processes, training and expectation setting.

### Principles

 Principles describe a set of expectations that several teams are expected to share. In this way principals can be thought of as a contract signed by all the teams. Principles are a useful tool when choices need to be made as they can provide some guidance for choosing one solution over another. Strategies can be designed assuming the principles will be true. because the strategy and the principles can be designed to reinforce each other. A team member who acts contrary to the principals (and the strategy) can be performance managed.

One of the most famous examples of principles driving and supporting strategy is Jeff Bezos’ infamous memo:

>All teams will henceforth expose their data and functionality through service interfaces.
>
>Teams must communicate with each other through these interfaces.
>
>There will be no other form of interprocess communication allowed: no direct linking, no direct reads of another team’s data store, no shared-memory model, no back-doors whatsoever. The only communication allowed is via service interface calls over the network.
>
>It doesn’t matter what technology they use. HTTP, Corba, PubSub, custom protocols — doesn’t matter.
>
>All service interfaces, without exception, must be designed from the ground up to be externalizable. That is to say, the team must plan and design to be able to expose the interface to developers in the outside world. No exceptions.

The memo was never intended to be public, as you can probably tell by the tone, it was made public accidentally. You can read more about that story here if you’re interested: https://gist.github.com/chitchcock/1281611

While this principle was handed down rather than created by a group looking to work together to achieve the best result it did the job. It helped Amazon become the giant success it is today and led directly to the creation of the Amazon cloud.

These principles also provide a great test for software choices. Clearly following this principle Amazon wouldn’t choose to buy any solution that doesn’t offer an API.

Principals are more usually derived in an inception workshop. This style of workshop has a great way of levelling the playing field for the people in the room; CTOs can choose to collaborate on an equal footing with junior engineers and in so doing will agree a set of principles together. This is a powerful way of not only creating the principals but beginning the process of creating a mutually agreed set of appropriate behaviours.

### Behaviours

As my good friend Dave Williams likes to sayL: "You get the culture you tolerate". In order for an organisation to be able to execute a strategy it must have an environment where that’s possible. That environment has many components but by far the most important is the behaviours exhibited by the people within it. Environments that contain many ways to fail and few ways to be successful, where nothing is ever praised or where nothing is ever certain creates cautious people who won’t commit to anything. It’s impossible for people, who are protecting themselves, to commit to a strategy, in many cases, they can’t even recognise a strategy for what it is, even after they’ve been told, because to them everything is a trap and success is defined as avoiding traps. The safe thing to do in these environments is not to do anything at all.

This means that prior to the formulation of a business strategy the behaviours of the people within that environment should be managed. Changing those behaviours might require a strategy and if the goal is a significant transformation it almost certainly will. In such transformations I have a saying: “Make it easy to do the right thing and hard to do the wrong thing”. In a security and governance context that means creating processes, tools and systems that are secure by default, as opposed to needing security applied afterwards.

Changing the behaviours of people in a company requires a two pronged approach. People must be rewarded for good behaviour and punished for bad. Reward and punishment, in this context, are subtle. A reward is not a celebration or an Amazon gift card. A reward in this context is a combination of praise and listening to the people in the team and ensuring they have the  resources they need to be more successful. If it’s a product delivery team, give them some support from SRE to help improve their pipeline or observability, or give them a delivery manager to help them organise themselves better. Then celebrate the team’s accomplishments in public, not the team themselves but rather what they have achieved. Again this doesn’t require an all-hands and public thanks and a gift card. This means private praise and public recognition of the capabilities of the product. Punishment is equally subtle, if a team is struggling with decision making, point out other teams who are doing it well and suggest the struggling team learn from them. If a team's product or service is lacking capabilities, have leadership lead workshops and spend time with them to help identify where the problems are. A team receiving such attention will be keenly aware that no one else is getting such attention and should figure things out. If they can't they are the wrong people to be working on that product.

Culture flows down from the top. If the organisation's leaders are displaying toxic behaviour then the rest of the organisation will inherit that behaviour. If leaders are always interrogating their people and nothing is ever celebrated then the rest of the organisation will do their best to stay out of the firing line and not step up and be bold.

### Processes

The power of processes is vastly underestimated in product and technology organisations. Many organisations create processes without even realising the impact those processes have. While those processes achieve their goal, they have inadvertent knock-on effects. These effects can be so widespread that they aren’t even noticed. Processes are mentioned here because they can impede or assist with strategy.

An company I worked with recently had created lines of business. They devolved budget authority to those lines of business. This allowed each line of business to be accountable for its success. This is a very powerful move that many organisations are too afraid to make. Unfortunately the finance department demanded such onerous processes that they missed out on all the benefits of the strategy. The company ended up being the kind of place where every decision required five meetings with increasingly senior people. This completely negated the impact, of what could have been, a transformative strategy. This is a case of where process hinders strategy.

This doesn’t mean creating processes should be avoided. The Law of Unintended Consequences must be taken into account. The first thing to do when considering creating a processes is to ensure there is a process for changing the process. Once that’s clear, processes should be designed to be as constrained as possible. Some people love a process and will work very hard to over-apply a process. This is particularly true in organisations where there hasn’t been much clarity in the past. This means it’s important to specify the situations where a process should be used and where it shouldn’t. Processes should also be published alongside a description of the intended outcomes. This empowers the people involved to inform the process owner of any unintended consequences. Processes must always have an owner. The process owner is accountable for the results achieved by the process.

To the strategist, processes represent a hard point in the strategic landscape. They are units of execution that can be relied upon. This is another reason why they should be constrained because as much as being able to rely on them can be useful, they also remove options. If processes are too large changing them might well need a strategy.

### Training

Training in the technology industry has taken on a bizarre meaning. In the technology industry training typically means attending a three or four day course. Sitting in a sterile classroom environment, usually in a rented workspace. The training involves some classroom-style learning about generic situations with minimal context. Then, the person returns to work to go back to doing what they were doing before. Where they then forget all they learned. Very rarely is any effort made to use what was learned. The net result is that the employee is told they have been invested in. They get something to add to their CV, which hiring managers tend to ignore except in rare, specific cases.

The training that actually has an impact in Technology comes from the little rewards. From things like submitting small, easily understood changes to a complex codebase. This trains the rest of the team to work in smaller increments. When obnoxious, over-opinionated, engineers are promoted, then everyone around them is given a lesson in what success looks like. Every action taken is training for the people close to that action and those affected by it. This is another example of why behaviours are so important. Every behaviour tolerated, rewarded, or punished is training.

When formulating a strategy, it’s important to know what people are trained to do. When implementing a new strategy it's usually necessary to do some sort of training. I was helping an organisation move away from a large, complex codebase that no longer had any discernible rules. I needed to encourage people to design smaller, discrete solutions. These should be easily understood and shouldn't be magnets for features. This was a new technology strategy, supported by an architectural direction. I chose to involve myself in onboarding new engineers. I would talk them through a high-level architecture diagram of the technology. I would explain where it was difficult to make changes and where it was easy. I would describe where there was space for new solutions that didn’t need to reference old technologies and data sets. I would provide a view of what good implementations looked like. Finally, I would offer a service as a reviewer for any solutions the new engineers or their teams might consider. This was usually the first time the new engineer was introduced to the wider context of the organisation’s technology. As such it presented an opportunity to instil some key principles, values, behaviours. This worked very well. When these new engineers had questions or concerns they would come to me as well as their team lead. This allowed there to be several views on what good looked like. This gave me an opportunity to help the team lead, where it was needed. I could also back-up that team lead lending weight to their authority.

### Expectations

The best way to give someone the space to do their job but ensure it’s done to the right standard is to set expectations. Expectation management can span the entire gamut of a job. They can help ensure a job is well defined before work begins. They can help ensure the job is completed to the right quality standards. Expectation management can ensure that appropriate aftercare is provided. It can also ensure that customers and stakeholders receive the right communications.

Objectives and Key Results (OKRs) are a great tool for setting expectations. They are sometimes misused by people who think OKRs are just a fancy way of setting goals. OKRs are a great structure for setting expectations. An OKR is nothing more than defining an Objective that needs to be achieved and a Key Result that can be used as evidence that the Objective has been achieved.

A DevOps OKR might be: To improve the confidence and safety of deployments. That could be measured by an increase in the Change Rate to two deployments a day.

That OKR gives an engineer a clue about the direction they should be thinking and it tells them what success looks like. On its own, that OKR could be dangerous. The engineer could, in theory, deploy solutions with known vulnerabilities. Their solution could make unreasonable hardware demands. There is an expectation that OKRs do not exist in a vacuum. For that particular OKR to be successful, there will need to be some technology standards. These standards would define languages, frameworks, and clouds that need to be supported.

Dave Williams, CIO at Trustpilot, is the master of expectation management. No one who works for Dave is ever in any doubt about what is expected of them. Even under trying circumstances, Dave doesn't resort to micromanagement. Dave always finds a way to make his expectations clear. He does this in two ways:

Dave holds himself to higher standards of behaviour than he holds his people to.

Dave uses the coaching technique of helping someone understand a problem by questioning. So Dave leads people to understand what’s expected of them by having them question themselves until it’s clear to them what they need to achieve.

This ensures that his expectations are internalised. The person is not meeting the standards because they are forced to. They are meeting those expectations because they understand, within themselves, that they are necessary. They also see their leader living those standards. With a little practice, people tend to meet Dave’s expectations unsupervised. Without thinking about it, they tend to pass these expectations on to their own people. In operating this way, Dave fulfills several of Sun Tsu’s conditions. In embodying his expectations as he does, he establishes what Sun Tsu called the Moral Law and fulfils the role of Commander.

## Utmost Exertion of Powers

In his book, On War, General Carl von Clausewitz starts by trying to create a science of military strategy. Clauswitz attempts to break war down into its constituent parts. One of these parts he calls: Utmost exertion of powers where he says:

>“If we are to defeat the enemy, we must proportion our efforts to his powers of resistance.”

Applying that premise to technology, where our enemy is the problem we are trying to solve. We need to ensure that we have enough people with the right capabilities and resources to match the scale and complexity of the problem. If the problem is very large, it will need a large number of capable people and large budgets to tackle it. In most organisations boards are unwilling to make very long commitments of people and resources. The way forward then is to break the problem down into smaller problems or milestones. These smaller problems should be defined such that solving them is either trivial or brings significant business advantage. In this way confidence grows and morale is improved. This visible progress might convince the budget holders to make more resources and people available. Each solution also builds the organisation's knowledge. In this way the execution of the strategy can also be an inspiration for other business ideas. This reinforces the value of strategy and the strategist and might unlock more people and resources for tackling the problem.

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

## Timescales for strategy

Defining the success criteria for each of the smaller problems is as much about timescales as it is about what needs to be achieved. Success might be considered to be achieved if the next round of funding is won. Looking at timescales that short is dangerous as it’s very easy to create a business that can’t grow to the next milestone. The timescale for a successful strategy needs to be close enough that the conditions won’t substantially change or become unmanageable but far enough away that substantial change can be achieved. There is also a human factor to be considered when choosing a timescale for a strategy. Humans have limited attention spans. A strategy that is too long term will not engage people as it will seem unrealistic or even if realistic it will be detached from people’s personal timescales. If the goals are ambitious enough then a long term strategy can inspire people and keep them motivated but significant milestones or proofs that can be celebrated along the way gives people an opportunity to unwind from their efforts and then refocus and step back in to work on the next milestone and the longer term goal. These are also the right moments for the strategist to engage with their stakeholders and ensure they are still working on the right problems and review the people and resources available to the strategy.

One of the most famous long term goals was the moon landing. In the 8 years between John F Kennedy’s speech and the actual moon landing there was almost one significant strategic accomplishment each year:

**1961:** President John F. Kennedy "I believe that this nation should commit itself to achieving the goal, before this decade is out, of landing a man on the moon and returning him safely to Earth."
<br>
**1962:** John Glenn becomes the first American to orbit the Earth.
<br>
**1964:** The first flight of the "dummy" Apollo spacecraft.
<br>
**1965:** Gus Grissom and John Young take off in the first flight of a two-man Gemini capsule.
<br>
**1966:** Michael Collins and Buzz Aldrin complete the first US spacewalks.
<br>
**1967:** The first flight of a Saturn 5 rocket is successful.
<br>
**1968:** The first orbit of the moon.
<br>
**1969:** Neil Armstrong and Buzz Aldrin land on the moon.

It’s easy to look back and write off this effort but I’d encourage all readers to imagine a single project at their company that could be successfully completed over 8 years and survive 3 CEO’s!

This albeit extreme example is a great lesson in how to craft a long term strategy. The people carrying out the strategy need to feel emotionally invested in the longer term goal but they need significant milestones to celebrate, blow-off steam, catch their breath once it’s complete before then leaning back in and refocusing on the next milestone and the longer term goal.

It’s also worth reflecting that many people in NASA probably only contributed to one or two of those milestones. To them, at that time, the longer term goal was important but other life events were more important. They had families that needed them to be somewhere else or they had better job offers or they burned out and needed to change careers or take a break. They still contributed to the overall goal and still deserve their share of the glory but to them it wasn’t an 8 year mission; perhaps they only contributed for 6 months. This is another reason why a long term strategy needs milestones. There needs to be a way that people can contribute to portions of the strategy that are realistic to them and their lives.

## Strategy is based on deception

At the end of the first chapter of Sun Tzu’s Art of War he writes:

>All warfare is based on deception.
>Hence, when able to attack, we must seem unable; when using our forces, we must seem inactive; when we are near, we must make the enemy believe we are far away; when far away, we must make him believe we are near.
>Hold out baits to entice the enemy. Feign disorder, and crush him.
>If he is secure at all points, be prepared for him. If he is in superior strength, evade him.
>If your opponent is of choleric temper, seek to irritate him. Pretend to be weak, that he may grow arrogant.
>If he is taking his ease, give him no rest. If his forces are united, separate them.
>Attack him where he is unprepared, appear where you are not expected.
>These military devices, leading to victory, must not be divulged beforehand.
>Now the general who wins a battle makes many calculations in his temple ere the battle is fought. The general who loses a battle makes but few calculations beforehand. Thus do many calculations lead to victory, and few calculations to defeat: how much more no calculation at all! It is by attention to this point that I can foresee who is likely to win or lose.

Strategy requires deception too. In some cases it’s because the tactics needed to achieve the strategy can be incongruous. In some cases deception is a necessary defence against disruption. The strategist should think about disruption in the same way that Sun Tsu thinks about his enemies.

### Initial tactics might appear to contradict the strategic goals

Many strategies require some set up, particularly strategies that rely on teams being able to perform autonomously like a microservice strategy. Successfully implementing a microservice strategy requires deception. If one day a CTO announced to the organisation that they’re going to adopt a microservice strategy it would be almost guaranteed to fail. Non-technology stakeholders would complain about the hundreds of hours of work that will be required just to recreate the business value that already exists in the current applications. Each development team would craft a different approach and possibly even choose different languages, frameworks and choose different technologies to implement them leading to unreliability and increased costs. Each team would choose where they wanted to start the initiative, some choosing services that offer no value, some choosing services that have multiple tight dependencies to existing systems meaning many other teams will get dragged into their problems. Every single one of these problems offers multiple avenues for disruption from inside and outside the organisation, the chances of success approaching such a problem head-on is negligible.

Successfully implementing a microservice strategy requires deception. A successful microservice implementation can start with a single team. It can start with an opinionated CI/CD pipeline that’s optimised for a limited number of languages, frameworks and technologies. This rewards teams with an easier and more productive time if they stick to these languages, frameworks and technologies. It can start with a single team trail-blazing an approach and documenting their decision logs and lessons learned. It can start with the formation of a mission based team looking at implementing a single solution and figuring out how to integrate it with the existing technologies. It can start with a set of enabling services added to the existing technology stack to make it easier for newer approaches and technologies to work with it. It can start with an API gateway layer presenting services in a coherent way even if the back-end is a disorganised mess of different solutions. Any one of these tactics can be the first step to a successful microservice strategy but in every case the stated result is not a microservice strategy it’s some lesser, easier to imagine goal that presents less surface area for disruption.

These examples also demonstrate the incongruous nature of tactics and strategies. Quite often the tactics needed to implement a strategy seem at odds with the strategy they are trying to bring into being. If we consider that the reasons for wanting to implement a Microservice strategy are usually to allow an organisation to have many teams working on the same objective at the same time without the problems associated with many teams working on the same codebase at the same time. One might think that the right approach to implementing a Microservice strategy would be to start with many teams and a single codebase. However as discussed above that is never the right way to do it. Strategies that rely on many teams working together always rely on mature core components and infrastructure. Something that only a single well organised team can create. Microservice strategies are often considered chaotic because they offer the most benefits to an organisation that has autonomous teams free to build what their specific parts of the product need. Chaos has its upsides; these teams need no command and control leadership to tell them when to scale up and down and when to focus on reliability or when to focus on features. These teams are quick and responsive if they have the  right capabilities and the right signals. Getting those capabilities and signals relies on good infrastructure, observability and a culture of learning and adapting. None of those come from chaos. So in order to benefit from chaos at some point in the future there needs to be an initial investment in order.

The first step on the journey to defining a strategy is to recognise the ultimate goal that needs to be achieved and then understanding the conditions that are already present. Once the conditions are well understood the strategist needs to determine if any of those conditions presents a risk to the strategy and hence needs to be changed. If conditions need to be changed a strategy will be required to achieve that lesser goal before the focus can be switched to the main strategy. That doesn’t mean these things have to be done one after the other but it might mean that one is on the critical path to the other meaning one has to finish before the other can finish. This layering of objectives is useful because it helps break down a complex problem into smaller simpler problems. Smaller, simpler problems can each be solved by smaller simpler strategies that each provide less opportunities for disruption but also provide more emergent opportunities.

Emergent opportunities is another reason why a level of deception is essential to implementing strategy. Long term goals can usually be achieved in a number of ways. We’ll go into more detail on this later when we discuss two-way doors, however for now recognise that in a large enough time scale there are numerous opportunities for disruption but there are also numerous opportunities for unforeseen successes that can themselves provide other ways to achieve the long term goal.

Going back to Zoopla again, I discussed how, at Zoopla there was a legacy tech stack that I had no confidence in. I was forced to expend engineering effort to attempt to see if it could be made safer and more predictable. I didn’t think it could be but I had to try. That presented me with two opportunities. If the attempt failed, as I predicted, I could double-down on my strategy of moving fast by building new solutions rather than attempt to refactor old ones using the failure as an example of why my strategy was the correct one. If the attempt was successful I would have a much easier time phasing out the legacy technology using GraphQL as the API for the data it created and managed because implementing those changes would be safer and quicker. Either way my goal of building small, modular components with modern languages and frameworks would be achieved.

## Conclusion

If there’s a problem that's difficult to define, work backwards through the problem using tools like the 5 whys to identify a root cause.

Once the problem has been identified, consider all the conditions in the organisation that affect the chances of a successful resolution. Identify if any of these conditions need to change in order to allow the successful resolution of the main problem. If any of the conditions need to change repeat the process for defining the problem. When considering how to change the conditions present in an organisation remember that there are many different tools available that can help, namely: Principles, behaviours, processes, training and expectations.

Once this is done, consider the timescales required to solve these problems to identify if a single, simple strategy is required or whether it will be necessary to run multiple strategies in series or even overlapping strategies in parallel.

With the timescales in mind consider other avenues of disruption such as powerful stakeholders or chaotic team members and how they can be brought on-side or use deception to manage the potential avenues for disruption. Consider the human timescales and present the strategy in easy to digest packages. What matters is that the results are achieved, not that everyone knows how clever the strategist is.
