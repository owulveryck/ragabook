*“Here’s one I made earlier”* is the staple diet of TV programmes when faced with the possibility that something might go wrong. Demonstrations are always a risky business. In the case of this book, doubly so. I want to let you loose on a scenario but alas I’m not even there to correct things if it all goes pear shaped. To manipulate the odds slightly in my favour of a beneficial result then before we get to the scenario (chapters 12 and 13), I’m going to cover some aspects of mapping in a little more detail. This is somewhat naughty because these ideas being fresh in your mind are likely to create a bias which is exactly what I’m hoping for. I’m signposting the answer before we’ve even got there. It’s the closest I could get to “Here’s one I made earlier” without writing down the answer first .  

However, to make the exercise still challenging then I’ve taking the liberty of hiding the clues throughout this chapter which is interspersed with lots of useful but not directly relevant concepts in a smorgasbord of the slightly useful. The concepts we will examine are on the opportunity of change, the trouble with contracts, common lies we tell ourselves and how to master strategy.

# Opportunity of change

Activities, practices, data and knowledge all evolve and co-evolve in a process which is not always smooth or continuous. In chapter 10, we covered the peace, war and wonder cycle and how previous giants in a peaceful product phase of competition can be overtaken by new entrants in the “war”. Those new entrants are likely to settle down to become the titans of that industry. The most interesting aspect of this cycle is in the change (**point 1** in figure 133) between the two states of peace and war and it’s here we will focus.  

Whilst the act (e.g. computing) may be well understood, this transition (e.g. computing shifting from products such as servers to utility services such as cloud) causes a great deal of confusion because the nature of the act is changing — we’re moving from a world of constant feature differentiation to a world of volume operations of good enough. This change is compounded by co-evolved practices (such as DevOps), our inertia to it, the surprising speed at which it occurs and vested interests usually spreading all manner of fear, uncertainty and doubt.  

<figure>
<img src="1__MdC3AnOSo8OQp39V8LE5Q.jpeg" alt="Figure 133 - A time of change" />
<figcaption>A time of change</figcaption>
</figure>

Behind the confusion, what is fundamentally occurring is the rise of new standards, the de facto optimisation of a market and a shift towards commodity. This doesn’t mean that alternatives aren’t available, we often have a battle over standards e.g. AC vs DC in the “electricity wars” or VHS vs Betamax for video recording standards. It’s however marketplace adoption and network effects that will choose the winner and consign others to the niche of history. It’s important to understand that in the early stages then everything is up for grabs.

## Alternatives in Cloud Computing

When Amazon launched EC2 (its utility compute environment) in 2006, I made a number of calls to executives in traditional hardware companies and offered to help them set up a competing service using our Borg technology — a suite of tools that we had used to provide on demand virtual machines within my own company . I was confident we could easily emulate the APIs of Amazon and though we were behind the game in some areas, we were ahead in others. Overwhelmingly there was no interest and the couple (i.e. two) meetings I managed to arrange always ended up with the same result — “how will this help us sell more servers?”  

I’d like to say that by 2008 the attitude had changed but it hadn’t. In late 2008, in the first of many such trips, I flew to the US, met a number of executives, told them their entire hardware business would be lost, showed them how by creating a market of AWS clones and creating a price war they could exploit a constraint that Amazon would have in building data centres and use this to fragment the market by pushing demand beyond supply. I explained why they wouldn’t do this due to existing inertia and why they would lose the war. The lack of interest was beyond palpable, it was dismissive. Amazon was not considered a threat but a minnow and only a “madman” would think otherwise. To paraphrase what I was told, these companies would be “doing something in the future in that market, creating their own standards and taking this industry away from Amazon if it ever became serious” which they assured me it wouldn’t. In all but actual words the message was clearly “go away little boy and let the grown ups deal with this in a responsible manner”. The air was always thick with endless prognostications of their own future greatness along with the old trope of “how will your stuff sell more servers?”  

The truth be told, I did feel like the naughty boy pointing at the Emperor and going “he’s got no clothes on”. It was like staring generals in the face and telling them that ordering troops to continue walking north over a cliff wasn’t a good idea and getting a gentle pat on the head or a pinch on the cheeks with the kindly guffaw of “walking north is what we do!”  

The problem with evolution in business is the threat is much larger than most realise due to the punctuated equilibrium and the rapid speed of change. You can either create a large ecosystem fast which means a very focused effort around creating a marketplace based upon some form of open standards or you can co-opt and eventually aim to own the standard. What you cannot afford to do is dilly dally, rest on your laurels or try to create another differentiated product solution to compete against evolution. Unfortunately, this is exactly what happened. The companies that have lost the cloud war had all the advantage — they had the finances, the skills, the talent, the reach, the brand and everything you could possibly want to win it. They were like generals in charge of massive modern armies going up against a David armed with a sling and a spud gun. Fortunately for David, the generals all ordered their troops to walk north, over the cliff and to their doom.  

The cloud war in infrastructure was lost not due to some magical engineering capability of Amazon but instead due to executive failure of past giants. Every single one of them could have won the war with ease. When they finally did act it was too late, with too little investment and often in the wrong direction because of a pre-occupation on what they wanted (“selling servers”) and not what their users needed. But users also had inertia to this change and in a somewhat tragic act of desperation this was seized upon. Past giants had found their Kodak moment.

## The Kodak moment of cloud

When Kodak had finally overcome its own inertia to the shift to digital images, it solved the conflict with its traditional fulfilment business by promoting the idea of the digital photo printer. They would bring fulfilment of photo printing into this digital world! It tanked because users just started sharing images and bypassed the whole point of the traditional photo. In the cloud world, this same tragic mistake has been created with the private cloud. We will bring you all the benefits of volume operations with commodity components through a public provider but using enterprise like hardware customised to your needs and running in your own data centre! In other words, they planned to bring “selling servers” into this utility world.  

Certainly private cloud has some merit for dealing with inertia (i.e. often unjustified security concerns) but this is a transitional play at best. It’s short lived and it’s not the end game. Alas even today, in 2017, there are people arguing that the future is a hybrid mix of public and private cloud. It’s not, it never has been. The future has always been a hybrid of multiple public clouds. But why multiple public clouds? The first concern is resilience which is solved through those co-evolved practice such as distributed systems and design for failure. Now, multiple public clouds doesn’t necessarily mean multiple public cloud providers. You could use multiple Amazon regions or availability zones and that is a hybrid model. The decision to use multiple providers is a trade between the risk of a single provider failure, the cost of switching between multiple providers and any bargaining power it might provide.  

Within the Amazon ecosystem then the cost of switching between regions is low, your bargaining power is relatively weak but you can mitigate risks by designing across many zones. For many, this is more than adequate. When you need to go that extra mile and combine multiple public providers then you’re incurring an increased cost of switching not only through any movement of data but also any change in the syntactic or semantic compatibility of APIs. Syntactic compatibility simply means the APIs have the same structure and form. Semantic means they operate in the same way. Without this compatibility then your management tools which work with one might not work with another and that incurs a cost of transition.  

To reduce this cost then either you want multiple public providers with are interoperable or management tools which cover both. But management tools can only cover both by offering the lowest common denominator i.e. the common factors between both. Unless you have a way of ensuring interoperability then switching incurs an additional cost beyond the movement of data through either transition costs or some loss of useful functionality. But switching is still desirable in terms of bargaining power and ensuring competitive pricing in a market. These are the trade offs that you need to consider. Well, in practice, you don’t. There is no interoperable and competitive market between multiple providers. There is instead one continent (Amazon), some substantial islands and then a lot of small atolls most of which are sinking fast into the sea. But it didn’t have to be this way, nor will it necessarily stay this way.  

If I go back to the Zimki plan (figure 134) then along with creating an ecosystem models around a serverless platform, we also intended to create a marketplace of platform providers and we hoped for a marketplace of infrastructure providers. It’s worth making a distinction here. You have a consumer ecosystem (as in companies or individuals that use your component), a supplier ecosystem (as in companies or individuals that provide components for you to use) and a marketplace (of consumers and suppliers around a component). These are not the same.  

<figure>
<img src="1_XLv85r9HLI3ObrXQgS1bRw.jpeg" alt="Figure 134 - Marketplace or ecosystem or both?" />
<figcaption>Marketplace or ecosystem or both?</figcaption>
</figure>

In the case above, we aimed to build a consumer ecosystem around our platform as a service i.e. we hoped many others would consume our component enabling us to run that “innovate-leverage-commoditise” model and to sense future change. We also aimed to provide a marketplace of providers (i.e. to enable others to set up as platform players) in order to overcome concerns over lock-in to a single provider. To achieve this we had announced the open sourcing of Zimki along with testing services to enable others to become Zimki providers.  

However, in our value chain, we also consumed components of infrastructure from others and hence it was advantageous to us (for reasons of pricing competition) that our ecosystem of suppliers consisted of a competitive marketplace with interoperability and easy switching between them. We intended to achieve this by open sourcing Borg (our infrastructure play) which would co-opt the APIs of any major utility provider if it appeared. Hence my early phone calls to those executives offering to provide them with an Amazon competitor.  

Open sourcing a technology not only enables that component to evolve quickly but it can help in creating an interoperable marketplace with switching between providers especially when combined with testing services. The last part is crucial, as there is always the danger than providers will try to differentiate with features in a commodity market creating what’s known as a collective prisoner dilemma — everyone weakening their own position and that of others through self interest. Unfortunately, whilst this was my plan in 2005, the entire project had been killed off in 2007 for not being “the future”. By the time the hardware executives finally woke up and started to play an open source game around OpenStack in 2010, they invested far too little and far too late. They failed to co-opt (arguing for differentiation) and failed to prevent a collective prisoner dilemma forming.  

It’s water under the bridge but if the competitors had reacted more timely, put in enough investment, focused on co-opting APIs, created a price war to force up demand beyond supply due to Amazon’s constraint then we might have seen a vibrant marketplace of many providers. Instead, we’ve seen not only industrialisation of computing infrastructure to utilities but also centralisation towards Amazon. This is another point to highlight in this sorry tale. Industrialisation does not necessarily mean centralisation. What it means is standardisation to a de facto. The question of whether something centralises or decentralises is influenced by other factors beyond evolution including executive gameplay.  

The reason why Amazon dominates the market is it has played the game well whilst most competitor executives have failed despite all their advantage. Equally, this is not a permanent state of affairs. A better set of players may emerge (e.g. from China) and cause the market to decentralise. The game however becomes much harder once a standard becomes established and the victors of the war have emerged. The time to change the players and to play the game well is in the overlap between the states of peace and war during the change from product to utility. If you miss this then to change the game again requires a bloody battle of attrition to unseat a titan, a game of last man standing and often political intrigue. It is unlikely that those who so spectacularly lost this battle will have the skill to win such a war of attrition.  

For infrastructure, this shift from peace to war has long passed and the victors have emerged. For the “serverless” platform world, we’re in the midst of this change at the moment. The war has been raging but it will soon be over. By 2020, we should probably know who the winners and losers will be.  

Opportunity on a map can be found in several places. From the genesis of the novel or the provision of unmet needs or differentiation of a product or the time of transition from one state (e.g. peace) to another (e.g. war) — see figure 135.  

<figure>
<img src="1_2Hkl4WkQUVotoCmRIW5H6Q.jpeg" alt="Figure 135 - Opportunity and change" />
<figcaption>Opportunity and change</figcaption>
</figure>

The maps won’t tell you what path you should take but they are a guide to help you discuss and decide.

# The trouble with contracts

Contracts like plans are often the bane of my life. It’s not that they don’t have a use, they do in terms of setting expectations. Unfortunately, for some reason that I have yet to fathom, people tend to invoke mystical properties around contracts. They tend to believe that the contract or plan represents a reality that is foretold — *“If it’s in the contract then it must happen as it is written”*. This is quickly followed by disappointment and disputes when it doesn’t. But surely, that’s the point of the contract — *“we want to know what is being delivered!”*  

To explain why that principle is the problem then I’m going to use an example for a communication platform for a large organisation with a distributed workforce that often worked on events. This organisation had a detailed plan for the communication platform, an exhaustive specification (hundreds of pages) and a division of the system into lots for contracting. It all seemed very sensible. However, as is my usual style, when I first met the team then I asked the question — *“What is the user need?”*  

The responses were somewhat elusive and wispy. It was felt that the answers were in the pages of the specification but they were not to hand. No-one had put them together. So, we spent a few hours and mapped the system out (see figure 136). The basic user needs were device to device communication (e.g. “I need to tell Joe to pick up a box”), point to multiple points (e.g. “I need to tell all my team to come to Sheffield”), emergency function (e.g. “We need more staff at this event”), scheduling (e.g. “I need to know where to go next”) to various applications, video recording and even simple use as a telephone.  

<figure>
<img src="1_C-siQui7bm0P24Ew0KKMiQ.jpeg" alt="Figure 136 - Communication Platform" />
<figcaption>Communication Platform</figcaption>
</figure>

To make the system manageable, the organisation had broken it down into what it considered to be sensible contracts based broadly upon financial value and other characteristics. However, when I overlaid those contract “lots” onto the map then there was an obvious problem. One lot known as “C” was very broad including items which were industrialised and others which were highly specialised, often custom made (see figure 137).  

<figure>
<img src="1_g3W9y9g9WbrBlGt5cgcAxQ.jpeg" alt="Figure 137 - Trouble with outsourcing" />
<figcaption>Trouble with outsourcing</figcaption>
</figure>

Why is this a problem? Let us assume we apply an outsourcing contract to Lot “C” for delivery against some specification. Obviously we want to know what’s being delivered hence we put effort into writing the specification. We have some form of competitive tender process which many potential suppliers bid for.  

We hope the suppliers will naturally try to be competitive in their bids. However, in order to do so then the suppliers need to manage their own risks. One of the risks is the change of specification. For example, if you asked me to bid for providing 10 tons of gold and I won the lot with a competitive price, then it would be for delivering 10 tons of gold and not 10 tons of platinum or 10 tons of diamonds. If you change the specification then I’m going to charge you.  

In any system governed by such contracts and specification then there will be a change control process as it’s only reasonable that if we change our mind then we incur the cost of this. These change control processes tend to be burdensome and expensive because they’re designed for minimising change and for delivering against the specification. Even a simple change can incur rewrites of the specification, analysis of impacts and many other steps that add up to considerable costs.  

But look again at the map above and in particular Lot “C”. Some of the components are industrialised which means they are unlikely to change and are suited to this contract approach. We can specify what we want here. However, some of the components are nearer the uncharted space. We don’t know what we want here, no-one does. These components will change and we will incur that change control cost. The problem is we’re applying a principle of *“we want to know what is being delivered”* to components that we cannot possibly know what is going to be delivered. The one thing we can guarantee with those custom built activities are they will change. We are doomed to invoke the expensive change control cost process at the point the contract is signed. The cost will spiral and dispute will happen.  

Let me be crystal clear. We can anticipate dispute even though we haven’t yet started. I can also tell you that some fool of a Took will decide that the solution to this problem for future projects is “better specification”. This will not only increase the costs in trying to describe the unknown but repeats the same mistake of change control costs by trying to define the unknown. Unfortunately, without mapping the environment and overlaying the contract structure then you won’t be able to find this problem until you hit it i.e. after the contracts are signed. Specification documents and business process diagrams don’t provide you with the situational awareness you need for sensible contracting.  

In 2008, I would commonly see this problem. Outsourcing had already got a bad name but in truth the problem isn’t outsourcing, it isn’t even contracts, it’s the way we apply such approaches across very broad systems containing both industrialised and often novel components. There’s a far better way to deal with such systems.

## FIRE

One case worthy of praise in business, is the truly marvellous work of Lieutenant Colonel Dan Ward. If you’ve never read FIRE or the Simplicity Cycle then stop what you’re doing (i.e. reading this) and go read them. I first came across FIRE (fast, inexpensive, restrained and elegant) when it was called FIST (fast, inexpensive, simple and tiny) and was used in military circles. The rename is more about a reboot to make it applicable to the wider marketplace. I happen to prefer the old term (probably my own inertia for having used it) because it’s just a bit more punchy.  

**Fast** means build things quickly i.e. short time scales. It’s a constraint on time and reduces the risks of change which comes with long schedules. **Inexpensive** is more than a constraint on budget, it’s a mindset of thrift and re-use. Simple is a constraint on complexity but also a mindset for the pleasing **elegance** of simplicity. It’s less about adding on more but taking stuff away. Whereas the A10 Warthog is an example of elegant simplicity in ground attack aircraft, the F35 is the polar opposite. Tiny means small, as in constrained or **restrained** as in small budgets, short schedules, small documents, small teams and small components. It’s again about mindset, a love of the detail and of self control. It’s about saying “Do we really want to add short take off and vertical landing to our bombing run, ground attack, air-to-air combat and reconnaissance aircraft?”  

**Fast** + **Inexpensive** + **Restrained** + **Elegant** = FIRE  

Taking these FIRE principles, I’ve applied them to our map of a communication platform form above which I’ve broken down into small discrete areas avoiding any broad systems i.e. no mixing of industrialised with the uncharted. Each of these areas should be managed using small budgets, short schedules — see figure 138.  

<figure>
<img src="1_9kirvgc_iiRNWuyn5ch9rQ.jpeg" alt="Figure 138 - FIRE" />
<figcaption>FIRE</figcaption>
</figure>

With such a map we can now apply the use of appropriate methods and techniques. For the more industrialised components we can look to re-use market standards or outsourcing arrangements under detailed specification or even utility providers such as cloud services. For the more novel we can build in-house or have contracts based upon time and material basis (see figure 139).  

<figure>
<img src="1_RkCpC8nysMaZtwL8ytuAXw.jpeg" alt="Figure 139 - Using standard components and appropriate methods" />
<figcaption>Using standard components and appropriate methods</figcaption>
</figure>

It’s worth noting that with novel items then you will tend to try and build these in-house. There are alternatives. You could outsource them under a time and material basis to a group that specialises in the experimentation required but this is a different type of arrangement from outsourcing under a specification or volume operations. You might even outsource the novel to the market i.e. just let the market get on with discovering what is there and take a back seat until the component becomes more evolved. Procrastination can be a useful tool if consciously used as such and with a good understanding of the landscape.  

We can also use the map to organise ourselves with small teams, distributing power away from some central planning office and giving autonomy and control to those on the “ground”, at the “coal face” who can make decisions more quickly, with a greater understanding of detail (see figure 140).  

<figure>
<img src="1_RkCpC8nysMaZtwL8ytuAXw.jpeg" alt="Figure 140 - Distribute power" />
<figcaption>Distribute power</figcaption>
</figure>

Using appropriate methods, tighter control on schedules and budgets with empowered people — what’s not to like? Actually, there’s often huge resistance to this.

## It’s all too difficult

Despite all the horrors caused and the endless stream of disasters, there is one commonly cited advantage of the all encompassing contract that seems to trump everything. The advantage is that it makes it simple to manage. The unpleasant old phrase of “one throat to choke” comes to mind. In practice, it provides someone else to blame when things go wrong or as change control costs spiral (as they would in the original contract structure).  

Of course, the vendor will blame you for not knowing what you wanted thus leading to the endless calls for better specification which only exacerbates the problem, We inevitably fall for this in business because of the fear of taking the risk, of managing what we need to manage, of embracing the complexity and uncertainty that exists. We fool ourselves (despite all the evidence) into believing that we can outsource this risk through massive, one size fits all contracts using detailed specification. To compound this, given enough time we even outsource the skills we need to effectively negotiate “reasonable” terms (if such a thing exists) for these contracts. These problems are acute in business but generally swept under the carpet. They are more visibly exposed in Government contracts with Government IT and “horrendous, costly failure” being synonymous in some quarters.  

The normal reaction to breaking down a complicated (and possibly complex) system is that it makes it difficult to manage. It exposes many areas to consider, many teams and many interfaces (see figure 141). The reality is those areas and interfaces existed beforehand and the use of a large (and broad) contracts is just a way of trying to make it someone else’s responsibility to manage. We are often willing participants in a game where to avoid managing the environment then we accept excessive cost overruns, inappropriate methods, loss of strategic control and ultimately greater risk whilst claiming the approach reduces risk. Outsourcing is a global practice that is often disparaged in the popular press due to these associations.  

<figure>
<img src="1_0fxmo1M-daM3TaL0PMOZJw.jpeg" alt="Figure 141 - Exposing interfaces" />
<figcaption>Exposing interfaces</figcaption>
</figure>

I need to emphasise that the problems are not with outsourcing per se but instead with what is being outsourced. The concept of outsourcing is based upon a premise that no organisation is entirely self-sufficient nor does any have unlimited resources and some work can be conducted by others at a lower cost. This is entirely reasonable. The organisational focus should not be on the pursuit of capabilities that third parties have the skills and technology to better deliver and can provide economies of scale. Every tea shop does not need to be a power generator, a tea plantation, a dairy herd and a kettle manufacturer. This practice occurs safely in more mature industries; the machine manufacturer doesn’t have to make its own nuts and bolts and can instead buy those from a supplier.  

Alas IT is not such an industry. A recent study that examined 5,4000 projects concluded that over 66% of large sized (in excess of $15M) software projects “massively blow their budgets” and 17% went so bad that they threatened the very existence of the company. The larger the project, the higher the rate of failure. Let us focus on those points. In an attempt to avoid managing what we should manage then under a banner of reducing risk we put the existence of entire companies at stake in 1 out of 6 cases and go disastrously wrong in 4 out 6. If this is **management** then to quote Inigo Montoya from The Princess Bride — *“You keep using that word, I do not think it means what you think it means”*.  

In comparison, the approach of SOCOM (special operations command) in the US Military is towards smaller projects, short acquisition cycles and re-use. As Dan Ward points out, 88% of SOCOM projects fit the FIRE principles with over 60% of those projects staying within cost and schedule estimates with the remaining 40% experiencing only “modest” overruns. The problems are not outsourcing as a concept but the size and breadth of the projects under such contracts. It is far more effective to think small — as in small teams, small contracts and small areas of focus.  

But there’s more to the game than this. It also offers up opportunities. Within the communication platform there is a requirement for an application store (see **point 1**, figure 142). It’s not uncommon even in 2017 with the abundance of well established application stores such as Google Play for companies to still believe that they need to build their own. Often such actions can be taken over concerns of control or because some pre-existing effort is under way or in production. These are all forms of inertia. But how do you deal with such inertia and any pre-existing systems? How can you turn this into an opportunity?  

<figure>
<img src="1_GV9QPiKKyChL6XLkVREmLA.jpeg" alt="Figure 142 - Dealing with legacy" />
<figcaption>Dealing with legacy</figcaption>
</figure>

In 2008, one of the big inertia barriers to adopting cloud services was legacy environments. These systems depended upon different architectural principles and were not suited to adoption of cloud infrastructure. Many companies decided that what they needed was a cloud service which acted like their “enterprise” environment. The reality is that such environments are a trade off between the cost of re-architecting versus the benefit of standardised commodity components. Whilst not a long term future, the appearance of vendors offering such enterprise clouds does provide an opportunity for exploitation. To explain this, I’ll outline three basic ways of dealing with legacy :-

## Disposing of liability

The first and most obvious approach is to simply recognise that a change is occurring, that you have inertia caused by past systems and you need to invest in re-architecting for the change. All technology investment is toxic over time and you need to continuously refactor to remove this. In many cases such refactoring is not done on a continual basis which stores up problems for the future by creating a large (toxic) landscape which then needs to evolve. To avoid huge scale projects (known in the industry as “Death Stars”) which attempt to resolve this mess (with the usual catastrophic results) then such change is best done in a piecemeal fashion using small components over time. You dispose of the liability bit by bit, often using techniques such as the strangler pattern. Even a relatively new company such as Netflix took seven years to remove its legacy and become data centre zero (all cloud). Unfortunately many will wait and fail to continually invest in refactoring. They leave the liability to grow until it becomes obvious that they have to change at which point they will scramble to build a “Death Star” along with many other companies who have done the same. This creates an inevitable shortage of skills which piles on the misery and cost. So, start early and dispose of it bit by bit.

## Sweat and dump

A variation of the approach is to deliberately sweat the legacy (i.e. minimise investment) whilst you build the new world. In the case of cloud, this is where enterprise cloud services might have some benefit. By shifting a legacy environment to an “enterprise cloud” provider with minimal architectural changes then you move any responsibility for capex investment to the provider. You sweat the legacy whilst preparing a new environment with components that you have built or use from third parties. What you want is for the “enterprise cloud” service to provide utility based charging with no long term contract. Despite the empty words you might have given the provider regarding long term future, when you are ready you unceremoniously start dumping the legacy. By such an approach you’re shifting future capex investment to the provider and reducing this cost for yourself. This method is unlikely to make you friends with the provider so plan accordingly.

## Pig in a poke

By far the best approach is to convince someone to pay you for your legacy. Just because you are aware that the environment is changing does not mean everyone else is aware. You’ll need a bit of misdirection here such as generating a future story for the legacy. In the case of the communication platform above, you might convince another company that enterprise application stores are the future. If you have a pre-existing home grown application store then you can sell it to them including some of the underlying environment (from infrastructure to staff) as a “future business” whilst ensuring you have access ideally on a utility basis hence providing a revenue stream for the buyer and making the deal seem “sweeter”. During this time you work on your replacement (e.g. shifting to Google Play) before dumping your use of the legacy store. This can be a surprisingly effective way to monetise legacy. This will definitely not win you friends with the people you sell it to but then caveat emptor!  

When you think about contracts, then look to break them down into small components, don’t be afraid to manage the risk and also think about how you can even turn your legacy into an opportunity with a bit of sleight of hand.

# It’ll save me money and other lies we tell ourselves.

There are many lies we tell ourselves in business:- the environment changes slowly, we can predict the uncertain, we can outsource our own risk, management can be made simple, the key to success is implementing this culture or that innovation or this principle or that method. If anything, I hope that mapping is teaching you that there are no single methods or simple answers but you can still manage this.  

These maps help you to describe an environment that consists of multiple evolving components. They contain simple components that have the perception of being well known, well defined and common such as the nut and bolt or the plug. They also contain chaotic components that are uncertain and we do not yet understand such as the genesis of the new. The environment itself can be complicated with many components and at the same time complex in that you have to dynamically respond to changes both caused by climatic patterns and other competitors actions. These terms of simple, chaotic, complex and complicated have quite precise meanings and I’d recommend the reader spending some time becoming familiar with the work of Dave Snowden and the Cynefin framework.  

Despite all of this, we try to grab for simple truths. In 2008, this was commonplace in the world of cloud computing mainly due to the confusion that existed. I thought I’d use a few “simple truths” that turn out not to be either simple or true to illustrate some climatic patterns that are worth knowing about.

## Efficiency will reduce our budgets

One of the most common ideas was that cloud computing would reduce IT budget expenditure. It’s a notion that if cloud computing is more efficient then then we will spend less on IT. Sounds simple, sounds obvious and yet it is so wrong.  

I gave a talk at <IT@Cork> (in 2008) on how this assumption ignored creation of new industries, componentisation and price elasticity effects. By increasing efficiency and the reducing cost of providing infrastructure then a large number of activities which might have been economically unfeasible become feasible. Furthermore, the self-service nature of cloud not only increases agility by enabling faster provision it also enables user innovation through provision of standardised components (the componentisation effect). Building a house is faster with bricks than a clay pit. This in turn can encourage the creation of new industries in the same manner that the commoditisation of electronic switching — from the innovation of the Flemming valve to complex products containing thousands of switches — led to digital calculators and computers. As these industries evolved they drove further demand for electronic switching.  

The effect of these forces is that whilst infrastructure provision may become more efficient, the overall demand for infrastructure will outstrip these gains precisely because infrastructure has become a more efficient and standardised component. We end up using vastly more of a more efficient resource. This effect is not new. It was noted by Willam Stanley Jevons in the 1850s, when he “observed that England’s consumption of coal soared after James Watt introduced his coal-fired steam engine, which greatly improved the efficiency of Thomas Newcomen’s earlier design”  

In figure 143 I’ve outlined the main effects. First (**point 1**) you have an activity that has evolved from genesis through to product and is finally becoming more industrialised e.g. a commodity or a utility. This will allow for more efficient provision of the act through volume operations.  

However, the more industrialised component can enable greater use of the component as previously uneconomical acts become viable (**point 2**). There can be a long tail of things we’d like to do and unmet needs which are enabled by the efficiency of provision. The final aspect (**point 3**) is consumption of the component will increase as new industries that it enabled start to evolve.  

<figure>
<img src="1_YPv3dP0Op-q2m4UM4jajdw.jpeg" alt="Figure 143 - Jevons paradox" />
<figcaption>Jevons paradox</figcaption>
</figure>

But can’t I just ignore this? We’re talking market effects here? Won’t it reduce my budget because all I care about is what I produce and not what new fangled industry is created or what unmet needs can now be met?  

If you look at computing then I can buy a million times more resource for the same money than I could twenty years ago. This doesn’t mean IT budgets have reduced a million fold in that time, instead we’ve ended up doing more stuff. Don’t confuse efficiency with reduced IT spend.

## Cloud will be green

Another common talking point in 2008 was whether cloud computing would be green. There was a lot to this from the substitution of physical goods for digital to the levels of inefficiency in the existing industry to the material waste in unused capacity to the means of energy provision. There was undoubtably a lot of waste and potential for improvement hence an argument could be made for Cloud being green. However, there’s something more long term to be thought about here.  

When we consider a value chain, we’re constantly industrialising components and building new systems on top of them. Machinery on top of the nut and bolt. Intelligent software agents on top of databases on top of computing on top of electricity. We are constantly creating higher order systems built upon more industrialised and ordered components. We are building towers of order out of the chaos. As with other biological systems, we are decreasing local entropy and that requires energy. We might be far from efficiently using energy today but regardless our underlying demand and consumption of power will increase (see figure 144). In order for progress to be green then inevitably we need to turn to the means of energy production.  

<figure>
<img src="1_0QC0y16ovSOAY2cDwfaqjg.jpeg" alt="Figure 144 - Feel the power" />
<figcaption>Feel the power</figcaption>
</figure>

## We can deal with it later.

Whenever we see a shift from products to more industrialised forms such as utilities, then most large companies (with the exception of the enlightened) will tend to ignore the change. This is due to inertia caused by pre-existing practice, assets and markets. The most telling signs are often overlooked until it is too late. One of these signs is the flow of financial capital. We tend to see a marked movement of capital away from the existing industries (the past) and towards both the more industrialised forms and the new activities built upon it.  

If I take figure 143 from above and overlay onto it this flow of capital along with the peace, war and wonder cycle then we can get a sense of what is happening. At the same time that an act is become more efficiently provided through industrialised forms with its demand increasing due to a long tail of unmet needs and the creation of new industry then financial capital is flowing away from past product vendors towards the new vendors and new companies serving those new markets. Now add in the co-evolution of new practice caused by the evolving act, the new forms of organisation that arise, the speed of change caused by a punctuated equilibrium, the inevitability of change (i.e. the Red Queen) and the inaction of past giants caused by inertia then what you have is destruction of the past at the same time as the future is being created. The combination of competition with basic climatic patterns such as inertia and co-evolution creates this constant pulse of new consumer needs, new vendors, new methods of production, new markets and new forms of organisation. This heart-beat was described by Joseph Schumpeter as “creative destruction” (see figure 145) and by the time it becomes obvious, it’s usually too late to react.  

<figure>
<img src="1_kjxswmy53A0j-_v8AG_0bA.jpeg" alt="Figure 145 - Creative destruction" />
<figcaption>Creative destruction</figcaption>
</figure>

But hang on! If we know about the cycle, if we can use weak signals to anticipate it, if we understand the different forms of inertia then surely we can prepare and adapt when it occurs? Why on earth would any company be disadvantaged or eliminated by it? The problem is blindness and this leads to the next lie we tell ourselves.

## Execution matters more than strategy

One thing I had become aware of in my journey around companies was that few seemed to have examples of maps. They had things they called maps but these diagrams lacked those essential characteristics e.g. visual, context specific, position relative to an anchor and movement. When I pointed this out, I’d often get a lot of pushback especially on the aspect of movement. This still happens today, so it’s worth emphasising.  

Movement isn’t simply about drawing a line on a picture it’s about the consistency of meaning of such a line. Position, anchor and movement are essential for navigation. Take a look at figure 146. It’s a farm (that’s the context), it’s visual, it has position of fields relative to an anchor (in this case the compass) and you can draw movement on it. You’d probably agree that you can give this map to someone else and they could quite happily find the barley field with it.  

<figure>
<img src="1_Ls468awzqH49IDszYl6bNg.jpeg" alt="Figure 146 - A map of a farm" />
<figcaption>A map of a farm</figcaption>
</figure>

I’ve taken the same map, kept the same number of fields plus their shape and relative areas but removed any concept of position and the anchor. I’ve just placed the fields in order of what type they are — fruit, livestock and crop. I’ve also added a movement line to it. The question is, could you hand this “map” (figure 147) to someone else and expect them to find the barley field?  

<figure>
<img src="1_TYQIm0rQtowVuy6BajZNOQ.jpeg" alt="Figure 147 - A “map” of a farm" />
<figcaption>A “map” of a farm</figcaption>
</figure>

It should be obvious that the answer is no. Movement and its consistency — you can follow this path to go from A to B — are not only essential qualities of a map but they also turn out to be essential for map making. Explorers can’t explore by just sitting still, something has to move (whether it’s them, a drone or a satellite is immaterial). Action is a necessity for exploration.  

These navigational qualities enable us to learn about the environment whether through a visual form or a equivalent internalised mental model. Take for example the tube map. The stations might not be in exactly the right geographical position but it is nevertheless a useful map. It has position of stations (anchored by the tube network itself) and consistent movement between them. If I’m at Bond Street there are multiple routes for me to get to Cannon Street but there is consistency. If I’m travelling anticlockwise on the circle line, then I know I will travel through South Kensington, Sloane Square, Victoria, St James’ Park and Westminster on my journey (**point 3**, figure 148). If there was no consistency then the circle line might take me via Victoria, St James’ Park and Westminster one day and Victoria, Edgeware Road and Mornington Crescent the next. I wouldn’t know where I would end up and it would be impossible to navigate.  

<figure>
<img src="1_jB8TWp3_BVK9wJ5ynRDg8g.jpeg" alt="Figure 148 - A tube map" />
<figcaption>A tube map</figcaption>
</figure>

Of course, the tube map doesn’t have to look like the above. You could build your own variety by simply travelling on the trains and recording the stations but as long as you can consistently describe movement then it is a map you can share with others. Now, tube maps are currently a vogue in the business world with various companies creating them to describe complex environments. For example, in figure 149 we have a “tube map” of the digital world. The maps lacks context being simply a grouping of technology and digital concepts. It has position of components but it is not clear what anchor is used. Lastly, according to the “map” then to go from Online Ad Networks to Agency Holding Companies you need to travel through social advertising then email marketing then digital agencies then management consultants then campaign management then media metrics then media agencies to reach the destination. Is this true? On what basis is that movement consistent and justified? I suspect it’s not. This is not a map, it’s a diagram of loosely connected concepts and questionable relationships.  

<figure>
<img src="1_DAB6uF4ll3ereKcG_ob9UA.jpeg" alt="Figure 149 - A tube “map” of the digital world" />
<figcaption>A tube “map” of the digital world</figcaption>
</figure>

So, why does this matter and what has this got to do with execution? Without maps then situational awareness will be poor. In 2008, I was still firmly under the illusion that people were just keeping their maps secret from me but doubts were growing. I started to have this notion that some companies might actually be blind to change and if people couldn’t see the environment they were operating in then how could they prepare for predictable forms of change? By the time such changes would become obvious, their pace and any inherent inertia would make them unsurmountable and even fatal. However, in discussion with others I was often told that this didn’t matter, that strategy was fairly meaningless compared to the real key which was execution. I also had doubts about this because firing a gun rapidly doesn’t help you if you don’t know where to fire it.  

In 2010, Professor Roger L. Martin challenged this notion head on in the Execution Trap. If you haven’t read it, go do so. Martin’s argument was there was no distinction between execution and strategy, they were part of the same thing. By pure chance, in 2012 under an LEF research project then I had the opportunity to test this.  

Every company told me they had strategy but I was acutely aware that there existed different levels of situational awareness. I had been interviewing 160+ Silicon Valley companies looking for examples of open gameplay whether open source, open data or open standards. I plotted these companies against their level of strategic play based upon situational awareness (i.e. using their understanding of own and competitors value chains and how they were evolving) versus their propensity to take action (in this case to use an open approach to change a market). The result is shown in figure 150.  

<figure>
<img src="1_fi_wQGoQaDbn9XmhLT1E8w.jpeg" alt="Figure 150 - Awareness vs Action" />
<figcaption>Awareness vs Action</figcaption>
</figure>

Leading Edge Forum 2012 study on situational awareness versus action  

The bigger the bubbles, the more companies at that point. This was Silicon Valley, supposedly the top end of competition and even here there were companies building strategic play based upon low levels of situational awareness and in some cases near blindness to their environment. Quite a few not only didn’t understand evolution, they didn’t know their value chains or even what their users needed.  
Now, if execution rules then the companies on the right hand side of this graph with a high tendency towards taking action should probably on average perform better. Of course, if strategic play based upon situational awareness was important then the companies at the top of the graph should perform better. Out of curiosity, I decided to examine market cap changes of those companies over the last 7 years. The results are shown in figure 151.  

<figure>
<img src="1_GTPhHpsolMRfBGdnGTkHNQ.jpeg" alt="Figure 151 - Market Capitalisation impact" />
<figcaption>Market Capitalisation impact</figcaption>
</figure>

Leading Edge Forum 2012 study on situational awareness versus action  

I can’t repeat what my first response was but let us just say that I was very surprised. What the data strongly suggests is those companies with high levels of strategic play based upon situational awareness and a propensity towards action perform better than those who don’t. Just having a focus on action is not enough.  

In the case of companies having low levels of situational awareness (i.e. those in the bottom half) then action (and how well you execute on it) does matter. Those with poor situational awareness and low propensity for action performed negatively whilst those with poor awareness but a high tendency towards action were more neutral. In other words, if you’re blind to the environment then it’s better to shoot faster and with more impact just in case you do actually hit something. Hence if you’re competing against others with poor situational awareness then I can see how an argument that “execution matters more than strategy” can occur.  

However, if you have poor situational awareness and are competing against someone with high situational awareness then you might have a much higher propensity towards action and better execution of such but they will still tend to outperform you. I find myself strongly in agreement with Professor Martin that strategy and execution are part of the same thing but also I’ll add that situational awareness is a key part of this. This study however was in Silicon Valley and the levels of situational awareness tended to deteriorate outside that cauldron of creativity. It had taken me several years to discover some weak evidence to back up my initial suspicions that corporate blindness (i.e. very low levels of situational awareness) was a problem. But how common place is this?

## How common is corporate blindness?

In 2014, I was messing around with modelling agents in a competitive market and looking at various impacts on company longevity. This was partially out of curiosity, a desire to learn and general play. I wasn’t expecting to find anything. I created a simulation with 1,000 agents (companies) competing against each other with each company having a starting age of 45 years. I added some variables for disruption through product vs product substitution, overlaid a peace, war and wonder cycle including new entrants and disruption of past players. I then added steps for acceleration of evolution due to industrialisation of communication mechanisms. I ran a multitude of scenarios and noticed patterns starting to emerge. One of the most interesting is shown in figure 152  

<figure>
<img src="1_Bmlsk_KnSIjROeItAvedDQ.jpeg" alt="Figure 152 - Agent modelling of competition" />
<figcaption>Agent modelling of competition</figcaption>
</figure>

What’s happening in the above is a constant undulation in average company age of the top 400 in the simulation. The system is constantly attempting to return to a higher average age but the constant wars and disruption by new entrants (on top of the normal product to product substitution) keeps this in check. However, the acceleration of evolution (due to industrialisation of the means of communication) is causing a shift downwards to a lower age and a new stable plateau around which age will oscillate. What’s interesting about this pattern is it reasonably closely mimics Richard N. Foster’s examination of average company age in the S&P 500 despite being a random agent model with set rules and parameters i.e. automatons in a variation of Conway’s Game of Life.  

Why is that interesting? Well, the agents are automatons that are blind to the environment. The pattern is highly influenced by the ability of the agents to adapt i.e. if we assume high levels of situational awareness and the ability of companies to evolve then this pattern doesn’t happen and a completely different pattern of dominance emerges. This, combined with my own experiences of industry and previous experiments on situational awareness versus action was enough to give me some confidence in what I started to suspect in 2008. Large parts of industry are blind to the environment they are competing in.

## We’re not blind, we have principles!

A common counter to this idea that companies were playing blind was that it didn’t matter. If we could find the ideal algorithms, rules or principles then we could create that sustaining organisation. You can think of this as a variation of Conway’s Game of Life but with the conceit that all we need to do is to find the right code and the problem with my simulation is I just had the wrong principles. To challenge this, I’ll use a bit of WoW.  

I’ve often found World of Warcraft (a massive multiplayer online role playing game known as WoW) to be a useful vehicle for explaining and exploring basic concepts of strategy and this is no exception. In this example, I want you to imagine two teams of players — the Horde and the Alliance — preparing to fight for the first time in a battleground called Warsong Gulch.  

Both teams have a short time to prepare before the battle commences. The winner is the team that captures the opponent’s flag three times. Let us assume neither team has been to Warsong Gulch before or has experience of fighting in battlegrounds. Just for reference, when your character is killed in the battleground it resurrects a few moments later in your team’s graveyard. One team (the Alliance) outlines its strategy for how it’s going to win the battle. It consists of what they describe as five principles that they’ve all agreed upon. These are :-  

**Focus** : Capture the flag and win the game!  

**Doctrine** :

-   Do this with great people! We’re going to be the best fighters, wizards and healers.

-   Be prepared to take risks and fail fast! We’re not going to just play it safe.

-   A supportive culture! We’re going to help each other when asked.

-   Open to challenge and asking the hard questions.

The team is enthusiastic and ready to go. Facing off against them is the team of Horde players. They’ve also spent their time preparing but the result is somewhat different. This team understands the importance of maps and uses them for strategic play. They have a map of Warsong Gulch and have developed a “strategy” which consists of :-  

**Focus** : Capture the flag and win the game!  

**Doctrine** :

-   Perform your role the best you can (Develop mastery).

-   Act as a single unit (a cell) i.e. fight and move together.

**Context specific play** :

-   To begin with team will act as one cell in an initial all out attack. The group will quickly move through central tunnel towards the enemy base, taking out opposing players that interfere. Always take out opposing healers first, then wizards and then fighters.

-   Once their flag is captured by our fighter, the group will work to take out opposing players and setup camp in the opponents graveyard — see map (figure 153) — killing off their players as they are resurrected and before they create any form of group. Taunting Alliance players is encouraged.

-   Once their graveyard is contained, the cell will split into two cells. A small offensive group consisting of a couple of wizards will take out opposing stragglers and the larger cell (including our flag carrying fighter) will continue to camp out in the opposing team’s graveyard killing all players that resurrect. Once opposing players are contained in the graveyard the cell will reform and our fighter will keep running the flag. If the plan fails then the group will reform around our flag carrier.

<figure>
<img src="1_hI_HiEEL4UwPoZV5TUhR3g.jpeg" alt="Figure 153 - The map of the play" />
<figcaption>The map of the play</figcaption>
</figure>

Annotated in game Map of Warsong Gluch, World of Warcraft  

Now, the Horde team has focus, principles and some form of context specific strategy based upon an understanding of the environment. It might not work but then the Horde players can use their maps to refine their gameplay with time. I can almost guarantee that when the battle kicks off, the first questions from the Alliance players will be “Should we attack or defend?” and “Where do we need to go?”  

Arguments within the Alliance team will quickly happen and before they know it the Horde will be upon them. The next cries you’ll hear from the Alliance members will be “Help!” and “Why is no-one helping me, I need help here!” and “Where are you?” followed by endless bickering that this or that player isn’t good enough to be part of the team combined with lots of shouts for “What is going on?” or “Where is everyone?” or “Should I grab their flag?”. In all likelihood, the Alliance team will be quickly broken into a panicked rabble. I know, I’ve been on that team and watched the mayhem.  

The point I want to emphasise is that principles are fine and yes strategy has to adapt to the game but don’t confuse the two. A set of principles does not make a strategy. Though it’s certainly better to have a set of principles than to have no principles and no strategy. This is equally applicable in business.  

There is however another aspect to consider. Within World of Warcraft there are many teams of Horde and Alliance players. Imagine that the Alliance players not only have no map, they’re not even aware of the concept of a map. All they can do is try some principles and share them from one team to another as “Secrets of success”. Imagine the Horde players understand the concept of maps, use them and share between them. Pretty soon, every Horde team will be winning using a wide variety of strategic plays. The Alliance doesn’t stand a chance until every player in the Alliance has built some mental model of the world (an internal map). Of course, every new player that joins the Alliance reduces this shared understanding. The best the Alliance can do is to tell the new player to “apply the principles and follow Morgana the Wizard. Just do what she does” in the hope the new player will build up some mental map.  

Principles aren’t going to save you against vastly higher levels of situational awareness. Now ask yourself, what do we do in business? Are we using maps for context specific gameplay, learning and communication or is our strategy more akin to copying “secrets of success” and “following others” i.e. we should be like Amazon, Netflix or AirBnB? Are we playing the game like the Alliance or the Horde? As tempting as it is, there is no secret formula and no magic secret to success.  

Conway’s Game of Life consisted of automaton that did not learn from the environment. We are not that. Awareness of the environment will always create an advantage over others and yes, I’m afraid the very nature of competition (even cooperative competition) is about creating an advantage. If anything, understanding the landscape better than competitors is the one area of continual sustained advantage because the landscape of business is always shifting.

## Focus on core!

Another common counter that was raised was the importance of core, having a goal and clearly defined purpose. At the same time that people were talking about the “goal”, Silicon Valley was raving about the “pivot”. In short, you should have a goal unless you pivot to another goal. Go figure!  

The problem of course is that strategy is not a long linear path but a constantly iterative process. The actions you or others take can change that game. All you can hope to do is to set a direction and adapt along the way or as Deng Xiaoping would say *“cross the river by feeling the stones”*. Core is at best transitory, it doesn’t matter whether you’re a software company or a legal firm.  

Let us take the example of a legal firm. You only need to travel back to the 1980s to find a world where will writing was a rather bespoke activity and legal firms made not inconsiderable sums from such practices. There was a constraint in terms of lawyers i.e. you needed a lawyer to write your will. Of course, industrialisation happened, Wills became more of commodity automated through standard templates and online services. Despite the gnashing of teeth and inertia created by past success (**point** 1, figure 154) the industry had to adapt. I’ve taken a liberty and simplified the components such as templates & computing to automation. What I want you to note is that the constraint between lawyers and wills was broken. Fortunately there was a wide variety of other contract structures which users demanded.  

<figure>
<img src="1__bretg8HGLpCMHhys6hFaQ.jpeg" alt="Figure 154 - Change to Wills" />
<figcaption>Change to Wills</figcaption>
</figure>

Alas, despite recent experience of this change, the industry is once again facing industrialisation of general contract writing through the use of AI systems. Naturally, there is the usual inertia to such changes —\_ it’s a relationship business, they won’t be good enough\_ — but since we’ve gone through this cycle in that industry within living memory it’s hopeful that more will adapt successfully this time. I suspect not (see figure 155). Once again the constraint of lawyers but this time to contracts will be broken.  

<figure>
<img src="1_JqBnjUrSYXo8RCJg2LDyWA.jpeg" alt="Figure 155 - Change to Contracts" />
<figcaption>Change to Contracts</figcaption>
</figure>

The point of this is that if your vision had been to provide personal will and contract writing services based upon access to lawyers, then what worked in the 1980s will by 2030 be mainly irrelevant or at best a niche market. There’s nothing you can do about this because you’re not solely in control, there are other players in the market and just because you don’t want it to become a commodity doesn’t stop someone else exploiting it as such.  

These sorts of changes can also hit you from multiple directions including from lower down the value chain via reducing barriers to entry into your market. The newspaper industry has suffered a recent example of this with the printing press. Back in the 1980s, if you wanted to be a journalist then you had to work for a newspaper which owned or had access to a distribution network and printing presses. These capital intensive assets were a constraint that acted as a barrier to entry. They were also a mechanism of control over journalists — there was a limited number of newspapers you could work for.  

Industrialisation of the means of mass communication through the internet was first considered a potential boon for media industries. However, it broke the constraint which has meant a flood of new entrants came into the market. Also any journalist can now set up their own online paper. This liberation changed the main reason why you’d work for a newspaper. It was no longer because they control the means of distribution but instead because of social capital — its network, brand, reputation — and access to other services. The media industry had to adapt or in some cases fail.  

But even the act of collecting, curating and writing news is now under pressure from AI with its more widespread use in business and sport reporting. The National Society of Newspaper Columnists, founded in 1977, has a core focus to promote professionalism and camaraderie among columnists and other writers but how does that mission fit into a world of computer generated copy? It’s the same with automotive industry where a core focus on the human driving experience might be relevant for the past but irrelevant or niche in a future of self driving cars. Of all the terms I come across then focus on core is probably the most destructive for the longevity of a company. To overcome it, you simply to have to accept the truth that there is no core other than a transient focus.

# Mastering strategy as simply as I can

We’ve covered a lot of ground in these chapters, so I thought in this final sections I’d recap some of the basics on how to *master* strategy. You’ll need this for the scenario. I’ve italicised *master* because I don’t really have a clue how to do that. I’m still learning and I’ve been using maps for over a decade. For now, all I can say is that strategy seems to be a journey of constant learning and the more I learn, the more I realise how little I know. If anyone does actually become a master then I’d be pleased to read about how they did it. There maybe a faster way to master strategy than a seemingly endless journey of learning. There might even be a 2x2 that’ll explain everything but so far, I haven’t found it. Hence in the absence of some marvellous solution, I’ll give you some basic steps.

## Step 1 — The cycle

Understand that strategy is a continuous cycle. You don’t have all the information you need, you don’t know all the patterns and there are many aspects of life that are uncertain. Fortunately not all is uncertain. Start with a direction (i.e. a why of purpose, as in “I wish to win this game of chess”) but be prepared to adapt as the game unfolds (i.e. the why of movement, as in “should I move this chess piece or that one?”). Your first step on the journey is to understand the cycle of strategy — figure 156. Lots of people can help you here from John Boyd (OODA loops) to Sun Tzu (art of war).  

<figure>
<img src="1_GmZy2zqOWgyI6LMxD5IIrQ.jpeg" alt="Figure 156 - the strategy cycle" />
<figcaption>The strategy cycle</figcaption>
</figure>

## Step 2 — Learn the landscape

Your next step is to observe the game i.e. to look at the landscape — figure 157. This is essential for you to be able to learn about the game, to communicate with others and to anticipate change. To observe the landscape you must have a map of its context. Any map must have the basic characteristics of : being visual, context specific (i.e. to the game at hand including the pieces involved), position of pieces relative to some anchor (in geographical maps this is the compass, in chess it is the board itself) and movement (i.e. how things can change, the constraint of possibilities). In business, extremely few companies have maps and so don’t worry too much about where others are going or grand proclamations that they might make.  

<figure>
<img src="1_dSUtviaj5TbcmK4JdYgPVw.jpeg" alt="Figure 157 - Build a map" />
<figcaption>Build a map</figcaption>
</figure>

## Step 3 — Learn and use climatic patterns

Once you have a map, then you can start to learn the next part of the strategy cycle i.e. climatic patterns. In business maps, these are the common economic patterns that effect all players and can be considered the rules of the game. Use those patterns to try and anticipate where the market is heading. The more you play, the more rules you’ll discover. It’s really important that before you start trying to organise and structure yourself (i.e. apply doctrine) that you look at where the market is going and not where it has been. No-one ever wins by building the perfect structure for the past. We’ve covered a pretty extensive number of the basic economic patterns but as I reminder, I’ll list them adding a few more flourishes where needed.

## Climatic Patterns

*Everything evolves through supply and demand competition*  

If the conditions exist that a person or groups of people will strive to gain some form of advantage or control over others due to a constraint (i.e. a limitation of a resource or time or money or people) then we have competition. If competition exists then the components effected will evolve until they become industrialised. This impacts everything from activities (what we do), practices (how we do something), data (how we measure something) to knowledge (how we understand something). The map is never static but dynamic. It’s also important to understand that if competition exists then you will be in conflict with others. Sometimes the best way of resolving this is through coopetition (i.e. cooperative competition) and building alliances. In other cases, depending upon the context, then you have to fight even to the point of a game of last man standing. In any significant landscape then you’re likely to find yourself building alliances on one part of the map whilst at the same time fighting other companies in another and withdrawing from a third. However as the components on your map evolve then your former allies can become foes and vice versa. Microsoft and open source used to be mortal enemies, they’re now often found to be best buddies. To manage such a dynamic and fluid environment then you’re going to need to be able to observe it.  

*Evolution consists of multiple waves of diffusion with many chasms.*  

Evolution consists of many instances of the same act e.g. a phone, a better phone and an even better phone. Every instance of an evolving act will diffuse through its applicable market. Those markets will change as the act evolves i.e. the market for the first custom built phones is not the same as market for more industrialised phones. The process of evolution can include sustaining, incremental and discontinuous change e.g. product to product improvements or product to product substitution. This path is not smooth, it is not linear, it has many branches and dead ends (e.g. phones that failed). Furthermore the actions of individual players are unpredictable. Hence you can know the direction (e.g. phones will industrialise over time) but not the steps and the exact path taken (this phone will be more successful than that phone) until you have walked it.  

*You cannot measure evolution over time or adoption.*  

The only consistent mechanism I’ve found for measuring evolution is ubiquity and certainty i.e. how well understood, complete and / or fit something is for the environment.  

*The less evolved something is then the more uncertain it is*  

By definition, the novel and new are more uncertain than industrialised components such as commodities and utilities. The uncharted space consists of the unknown i.e. “Ere be dragons”.  

*No choice over evolution*  

In a competing ecosystem then the pressure for adoption of a successful change increases as more adopt the change. This is known as the “Red Queen” effect i.e. you have to continuously adapt in order to keep still (in terms of relative position to others). The one thing that standing still will guarantee is that you will be overtaken. The Red Queen has a secondary effect which is by adaptation then competitors limit the growth of a single company and prevent a run away process.  

*Commoditisation does not equal Centralisation*  

Don’t confuse evolution to a commodity with centralisation. They are governed by different factors and an industrialised component can easily yo-yo between centralised and decentralised forms. Competitor gameplay is one of those factors which determine whether we’re going to start with a more centralised or decentralised world.  

*Characteristics change as components evolve*  

The characteristics of a component in the uncharted space are not the same as the characteristics of the same component when it becomes industrialised. In any large system then you’re likely to have components at different ends of the evolution scale. This leads to the Salaman & Storey Innovation paradox of 2002 i.e. the need to innovate requires polar opposite capabilities to the need to be efficient. However, a word to the wise, a company has to manage both the extremes along with the evolution between them. It’s really important to remember that there is a transition from uncharted to industrialised. Don’t organise by the extremes alone.  

*No single method fits all*  

Because of this changing characteristics there is no one size fits all methods or technique applicable across an entire landscape. You have to learn to use many approaches and so avoid the tyranny of any single one. However, expect tribes to form and endless pointless debates such as agile versus six sigma or outsourcing vs insourcing.  

*Components can co-evolve*  

All components can evolve whether activities, practices, data or knowledge but they can also co-evolve. This is commonly seen with the co-evolution of practice (how we do something) with the evolution of an activity (what we do) especially as we shift from products to more industrialised forms. What causes this is the change of characteristics of the activity. DevOps is one such example of co-evolution.  

*Efficiency enables innovation*  

Genesis begets evolution begets genesis. The industrialisation of one component enables novel higher order systems to emerge through componentisation effects. But it also enables new features for existing products to appear or even the evolution of other components. The industrialisation of mass communication to a standardised utility such as the internet enabled the industrialisation of computing to a utility. I use the word innovation to describe all those changes from the genesis of a new act, feature differentiation of an existing act or a change of business model (e.g. shift from product to utility). The evolution of one component and its efficient provision enables innovation of others.  

*Higher order systems create new sources of value*  

It is the genesis of new components, enabling new user needs that creates future sources of differential value. I specifically state “*enabling*” because in many cases the users are unaware of the future needs they might have.  

*Future value is inversely proportional to the certainty we have over it.*  

Genesis of a component is inherently uncertain but it is also the point at which a component has its highest future value. You have to gamble with the novel but there’s also the potential for huge rewards. As the component evolves, its potential for differential value declines as it becomes more ubiquitous in its applicable market. This also means that any component that has not reached ubiquity must retain some uncertainty and some element of risk. The only conditions where a well understood, almost risk free component exists that is not ubiquitous and is of high value is when there is some form of restriction on competition e.g. a constraint through patents or monopoly. Care must also be taken not to confuse the terms common as in “everyone has one” with ubiquity to its applicable market. Many components have resource constraints (e.g. gold) or the market need is specific (e.g. wigs for barristers and judges).  

*Efficiency does not mean a reduced spend*  

Whilst evolution does result in more efficient provision of a component this should be not be confused with a reduction of spending on it. In many cases there is a long tail of unmet demand that efficiency will enable or previously uneconomical acts that become feasible or even the creation of new industries that result in greater demand. This is known as Jevon’s paradox.  

*Evolution to higher order systems results in increasing energy consumption*  

The constant evolution of components and creation of higher order systems that then evolve means we are always moving to a more ordered environment by reducing local entropy. This requires the constant input of greater amounts of energy though in some cases this can be hidden due to efficiency gains from previous wasteful consumption.  

*Capital flows to new areas of value*  

The lines on the map represent flows of capital whether it’s between two existing components or a component and its future more evolved self. Financial capital will seek the area of most consistent return. Hence in the evolution from product to a utility then capital will tend to move away from the pre-existing product forms and towards the more industrialised component and the new industries built upon it  

*Evolution of communication can increase the speed of evolution overall*  

Evolution consists of many diffusion curves. If a means of communication evolves to a more industrialised form — whether printing press, postage stamp, telephone, the internet — then the speed of diffusion curves can increase. This in turn can accelerate the rate at which future components evolve. Care should be taken here, not to confuse faster evolution with us becoming more innovative as a people. Certainly we have greater opportunity to build new things but don’t assume we’re getting smarter.  

*Change is not always linear*  

There can often be a perception that change is gradual because one instance of a component (e.g. a product) is replaced by another in the same stage of evolution (i.e. a more feature complete product). This illusion of smooth and gradual change lulls us into a false sense of security that all change is such.  

*Shifts from product to utility tend to demonstrate a punctuated equilibrium*  

The shift across a boundary e.g. from custom to product or from product to commodity tend to visibly exhibit rapid exponential change and a shift from the past. This is known as a punctuated equilibrium.  

*Success breeds inertia*  

Any past success with a component will tend to create resistance to changing that component. There are many different forms of inertia.  

*Inertia increases the more successful the past model is*  

The more success we have had with a component then the more resistance and bias we have against it changing.  

*Inertia can kill an organisation*  

Contrary to popular belief, it’s not a lack of innovation that harmed companies such as Blockbuster and Kodak but instead inertia to change created by past success. Both these companies helped develop the future industries but suffered at the hands of their past business models.  

*Creative Destruction*  

The combination of inertia, a punctuated equilibrium, the red queen and co-evolution of practice means that as we shift across a boundary e.g. product to utility then we tend to get rapid destruction of the past (from business models to practice) along with creation of the new (industry and practices). This was described as creative destruction by Joseph Schumpeter.  

*Competitors actions will change the game*  

Climatic patterns are ones that depend upon aggregated market effects e.g. evolution through supply & demand competition. This means that you cannot stop them without preventing competition in the market and the existence of competitors will cause them to happen.  

*Most competitors have poor situational awareness*  

Competitor actions are an important part of anticipation. In general however this is not something that you can directly control or even anticipate beyond aggregated effects. Fortunately in today’s climate then most competitors act as blind players in which case you do not need to dwell too much on their actions. When you make a move, they are unlikely to understand why or counter you. In the near future, given the potential interest in business algorithms, they maybe even become anticipatable blind automatons following coded secrets of success. In much the same way that Dan Mirvish noted that when Anne Hathaway was in the news, Warren Buffett’s Berkshire Hathaway’s shares went up due to suspected sentiment analysis run by robotic trading platforms. This could make the game even easier.  

*Not everything is random*  

Not everything is uncertain within the map. There are various aspects which can be anticipated though the level of predictability is not uniform. In some cases you can say what will happen due to aggregated market effects (e.g. this act will evolve) but not precisely when the next iteration of a more evolved product will appear (e.g. it depends upon actors action). In other cases you can anticipate both the what and the when.  

*Economy has cycles*  

The economy demonstrates cycles such as the peace, war and wonder cycle. We start with the wonder of a new, uncommon and poorly understood thing. As we learn more then the applicable market grows and products are produced. New giants form and dominate a rather peaceful time of sustaining competition. There is some disruption (i.e. product to product substitution) and the competition is still fierce but the giants generally weather these storms. Then the act evolves to more industrialised forms, new entrants become the new titans, past giants tend to fall being stuck behind inertia barriers created from their own success. This is the time of war where competition becomes life threatening for those past giants. New industries built on the industrialised components form and a new state of wonder is born.  

*Two different forms of disruption*  

There is more than one form of disruption such as the unpredictable product to product substitution to the more predictable product to utility substitution. The latter can be anticipated through weak signals.  

*A “war” (point of industrialisation) causes organisations to evolve*  

The industrialisation of an act will tend to cause co-evolution of practice and changes to how organisations operate. If the component is significant then this can lead to a new form of organisation.  

You need to apply these patterns to your map to start to learn how things could change. You then need to allow others to challenge your assumptions and the scenarios you create — another key part of learning — until you’ve got a map you all agree with or at least understand e.g. figure 158  

<figure>
<img src="1_IoTh2h9SPdXz20EtWGe5-w.jpeg" alt="Figure 158 - Anticipating change" />
<figcaption>Anticipating change</figcaption>
</figure>

## Step 4 — Learn and use doctrine

Now you have an idea of your landscape and how it can change, you’ll want to start doing stuff about it. However, there are two classes of choice ; those which are universally applicable and those which are context specific. The universally applicable choices are a set of principles which we all should apply. These are your doctrine.  

At the time of writing, this is my list of basic doctrine — hence Wardley’s Doctrine (I really am that unimaginative). This is based upon my observations over many maps with many organisations and contains universal principles that I consider to be reasonably sound. Many of these we have already covered

## Wardley’s Doctrine

*Be transparent*  

Have a bias towards openness within your organisation. If you want to effectively learn about the landscape then you need to share your maps with others and allow them to add their wisdom and their challenge to the process. Building maps in secret in your organisations is a surefire way of having a future meeting where somebody points out the blindingly obvious thing you have missed.  

*Focus on high situational awareness*  

There is a reasonably strong correlation between awareness and performance, so focus on this. Try to understand the landscape that you are competing in and understand any proposals in terms of this. Look before you leap.  

*Use a common language*  

A necessity for effective collaboration is a common language. Maps allow many people with different aptitudes (e.g. marketing, operations, finance and IT) to work together in order to create a common understanding. Collaboration without a common language is just noise before failure.  

*Challenge assumptions*  

Maps allow for assumptions to be visually exposed. You should encourage challenge to any map with a focus on creating a better map and a better understanding. Don’t be afraid of challenge, there is no place for ego if you want to learn.  

*Know your users*  

When mapping a landscape then know who your users are e.g. customers, shareholders, regulators and staff.  

*Focus on user needs*  

An essential part of mapping is the anchor of user needs. Ideally you want to create an environment where your needs are achieved by meeting the needs of your users. Be mindful that these needs will evolve due to competition and in the uncharted space they are uncertain. Also, be aware that users may have different and competing needs and be prepared to balance the conflict  

*Think fast, inexpensive, elegant and restrained (FIRE)*  

Break large systems down into small components, use and re-use inexpensive components where possible, constrain budgets and time, build as simply and as elegantly as possible.  

*Be pragmatic*  

There will always be edge cases or a way to make something more perfect but if what you’re building could use a component that already exists then try to avoid the urge to re-invent it. If you’re a taxi company then investing your funds into making that perfect tyre will not help your business. Always challenge when you depart from using something that already exists. The old adage of “It doesn’t matter if the cat is black or white as long as it catches mice” is relevant here.  

*Remove bias and duplication*  

Use multiple maps to help you remove duplication and bias within an organisation. You will often find in any large organisation that there are people custom building what is a commodity or rebuilding something that exists elsewhere. Remember, that they’re not doing this because they’re daft but because of pre-existing inertia or the lack of any effective communication mechanism i.e. they simply don’t know it exists elsewhere. Be warned, the level of duplication within most organisations vastly exceeds any expectations that they might have and you’re often treading on the toes of someone’s pet project. Large distributed companies often talk about duplication in the single digits e.g. we have six enterprise content management systems. They tend to react in horror when it is “discovered” that they have hundreds or even “thousands”. People can get very defensive in this space and want to shut you down.  

*Use appropriate methods and tools*  

Try to avoid the tyranny of one. Understand that there is no magic solution and that you have to use multiple methods (e.g. agile or lean or six sigma) as appropriate. In any large system, multiple methods may be used at the same time. Be mindful of ego here, tribes can form with almost religious fervour about the righteousness of their method. Have fortitude, you’ll often find you’re arguing against all these tribes at the same time.  

*Focus on the outcome not a contract*  

Try to focus on the outcome and what you’re trying to achieve. Realise that different types of contract will be needed e.g. outsourced or time and material based or worth based development. Along with a focus on outcomes, try and keep contracts constrained in terms of time and budget.  

*Use standards where appropriate*  

If something is industrialised and if standards exist then try to use them. There’s always a temptation to build a better standard but avoid this or building abstraction layers on top of other “standards” unless you have an extremely compelling reason to do so. If you need a toaster, buy a toaster and don’t try building one from scratch.  

*Optimise flow*  

Within a map there will be many flows of capital — whether information, risk, social or financial. Try to optimise this and remove bottlenecks.  

*Effectiveness over efficiency*  

Whilst optimising flow is important, be careful not to waste valuable time making the ineffective more efficient. Understand the landscape and how it is changing before you attempt to optimise flow.  

*Manage inertia*  

At some point you will face inertia to change e.g. existing practice, political capital or previous investment. Try and understand the root cause. Ideally use a map to anticipate this before you encounter it and hence have prepared solutions & counter arguments. If possible, use the maps to enable people to discover their own inertia.  

*Manage failure*  

In any system there is risk. Use the maps where possible to help you understand failure modes, what can go wrong and what will be impacted if a component fails. Try where possible to mitigate risks by distributing systems, by designing for failure and by the constant introduction of failure (use of chaos engines such as Netflix’s chaos monkey). Avoid known failure modes such as building large scale (death star) like efforts.  

*Think small*  

Know the details, use small teams and break large landscapes into small contracts. Don’t be chased away by fears of complexity of management.  

*Distribute power and decision making*  

Have a bias towards distributing power from the centre including yourself. Put power in the hands of those who are closest to the choices that need to be made.  

*Provide purpose, mastery & autonomy*  

Provide people with purpose (including a moral imperative and a scope) for action. Enable them to build mastery in their chosen area and give them the freedom (& autonomy) to act.  

*Think aptitude and attitude*  

Understand that people not only have aptitudes (e.g. finance, engineering, operations and marketing) but different attitudes (pioneer, settler and town planner). The mindsets are different.  

*There is no one culture*  

Understand that a company which plans for longevity needs to cope with not only the discovery of uncharted components but the use of the industrialised and the transition between these two extremes. You will need different attitudes. You will therefore create many cultures in your organisation e.g. pioneers, settlers and town planners have different cultures. This is not a negative and don’t try to grind everyone into a single bland culture. It will not make them happy.  

*Seek the best*  

Try to find and grow the best people with the best aptitude and attitude for their roles. Invest in keeping them. Don’t force them into becoming something they’re not. It’s perfectly reasonable for a truly gifted systems tester who excels in a town planning world of massively complicated and automated systems to be paid more than the project manager. What you want to avoid is taking exceptional people out of their role and putting them into something they are not suited to simply because they think that is the only way to progress. Leadership, management and engineering are all aptitudes, they are all valuable and they have to work in concert. If the hierarchy of your organisation uniformly reflects your pay scales then you’re likely to be draining talent from where it should be and putting it into roles that it is not suited for. This is often done for arguments of “responsibility” or “managing bigger teams” (which also causes people to try and accumulate empires) or “spreading experience” or “career path” but there are alternative ways of achieving this. Taking a gifted engineer and turning them into a mediocre project manager is not wise. This is probably one of the most difficult areas as ego is quickly encountered.  

*Design for constant evolution*  

Create an organisational system which copes with the constant ebb and flow in the landscape. Ideally, changes should flow through your organisation without the need for constant restructuring. A cell based structure using a system of theft with pioneers, settlers and town planners is one such system.  

*Use a systematic mechanism of learning*  

The purpose of mapping is not just to create a map and a shared understanding but also to learn climatic patterns, doctrine and context specific play. Maps provide a systematic way of doing this as long as you collate, review and learn from them. Have a bias towards such learning and the use of data.  

*A bias towards action*  

This is best explained through the word’s or Rimmer’s Study Habit (an episode from Red Dwarf).  

*“The first weeks of study, he would always devote to the construction of a revision timetable. Weeks of patient effort would be spent planning, designing and creating a revision schedule which, when finished, were minor works of art.*  

*Every hour of every day was subdivided into different study periods, each labelled in his lovely, tiny copperplate hand; then painted over in watercolours, a different colour for each subject, the colours gradually becoming bolder and more urgent shades as the exam time approached. The effect was as if a myriad tiny rainbows had splintered and sprinkled across the poster-sized sheet of creamwove card.*  

*The only problem was this: because the timetables often took seven or eight weeks, and sometimes more, to complete, by the time Rimmer had finished them the exam was almost on him. He’d then have to cram three months of astronavigation revision into a single week. Gripped by an almost deranging panic, he’d then decide to sacrifice the first two days of that final week to the making of another timetable. This time for someone who had to pack three months of revision into five days”*  

Do not attempt to create the perfect map. Have a bias towards action because the landscape will change and you will discover more through action. You learn by playing the game.  

*Listen to your ecosystems*  

There are many different forms of ecosystems and ways to exploit them. You can build powerful sensing engines (e.g. the ILC model) for future change, sources of co-operation with others, defensive and offensive alliances. But ecosystems need management, they need tending as a gardener tends a garden — sometimes you allow them to grow wild, sometime you harvest, sometimes you help direct or constrain them. These are particular skills that you can develop but most important is the principle — listen to them.  

*A bias towards the new*  

Whatever you do will evolve. So have a bias towards the new, be curious and take appropriate risks. Be willing to experiment.  

*Be the owner*  

Take responsibility for your environment, your actions within it and how you play the game. You could outsource this to a third party in the way a chess player could outsource their gameplay to another but you won’t learn and it is still you that loses.  

*Strategy is iterative not linear*  

Understand that strategy is iterative. You need to adapt in fast cycles according to the changing environment. The best you can hope for is a direction, a constant process of learning and improvement of your gameplay along the way.  

*Do better with less*  

Have a bias towards continual improvement.  

*Set exceptional standards*  

Don’t settle for as good as or slightly better than competitors. Always strive for the very best that can be achieved.  

*Strategy is complex*  

There will be uncertainty, emerging patterns and surprises along the way. That’s the very nature of competition due to the involvement of other actors. Embrace this, don’t fall for the temptation that you can plan the future. What matters is not the plan but the preparation and your ability to adapt.  

*Commit to the direction, be adaptive along the path*  

Once you’ve set a direction commit to it. There will often be hurdles and obstacles but don’t just simply abandon a direction because a single step is challenging. Try to find paths around the obstacles. If you’re building a system and a common component is not as expected then that can often prove a market opportunity.  

*Move fast*  

The speed at which you move around the cycle is important. There is little point implementing FIRE like principles in developing a system if it takes you a year to make decision to act. An imperfect plan executed today is better than a perfect plan executed tomorrow.  

*There is no core*  

Everything is transient, whatever you think is core to your company won’t be at some point in the future. The only things that are truly static are dead.  

*Exploit the landscape*  

Use the landscape to your advantage, there are often powerful force multipliers. You might decide not to take advantage of a competitor or a change in the market but that should be a conscious choice.  

*Think big*  

Whilst the actions you take, the way that you organise and the focus on detail requires you to think small when it comes to inspiring others, providing direction and moral imperative then think big. Your purpose is not to defend the narrow pass of Thermopylae but instead to defeat the Persian army and save the Greek states.  

*Be humble*  

Listen to others, be selfless, have fortitude and be humble. Inspire others by who you are and what you do. There are many ways to manipulate the landscape e.g. with marketing by persuading others that what is a commodity is somehow different or that a product is unique to them. But these manipulations come with a cost not just externally but internally. We can start to believe our own hype, our own infallibility and our “right” to the market. Avoid this arrogance at all costs.  

As with climatic patterns, the more you play the game then the more forms of doctrine you’ll discover. It’s important to learn these continuously, so get used to using maps as a retrospective. Look for what has changed and always ask why? Of course, knowing about doctrine is not enough — you’ll want to apply it. Don’t pick and choose, apply them all. When it comes to applying doctrine then there are three basic cases

-   the map solves doctrine for you (e.g. having a common language)

-   you can use many maps to apply doctrine (e.g. use of multiple maps of different lines of business to reduce duplication and bias)

-   you can apply doctrine directly to a map (e.g. cell based structures, cultural forms such as pioneer — settler — town planner) as shown in figure 159.

<figure>
<img src="1_krb6I8pe7JTRT0FE3udW8g.jpeg" alt="Figure 159 - Apply doctrine" />
<figcaption>Apply doctrine</figcaption>
</figure>

## Step 5 — Learn and use gameplay

The other class of choice is context specific. You will learn there exists many approaches that you can deploy in order to influence the map. These approaches depend upon the map and the position of pieces within it i.e. they are not universal and you have to learn when and where to use them. To get you started, some basic from of gameplay (often called stratagems) are :-

## Gameplay

*Open approaches*  

Whether source or data or practice, the act of making something open reduces barriers to adoption, encourages collaboration and accelerates the evolution of the component.  

*IPR*  

Intellectual property rights (IPR) can be used to slow evolution by limiting competition even to the point of ring fencing a component making it difficult for others to evolve it further.  

*Fear, uncertainty and doubt*  

Often used to slow evolution by exploiting inertia to change within customers and forcing new entrants to divert energy away from the components and into countering the accusations.  

*Exploiting constraint*  

An existing constraint can be exploited to fragment a single player by increasing demand beyond their ability to supply (e.g. by creating a price war).  

*Sweat and Dump*  

A mechanism of disposing of legacy liability onto a third party by exploiting their own inertia to change.  

*Pig in a poke*  

A mechanism of dressing up a liability as some form of future business before divesting to a third party.  

*Two factor markets*  

A mechanism of bringing providers and consumers together and exploiting network effects and aggregated data.  
*Sensing Engines (ILC)*  

A mechanism of being the first mover to industrialise a component, allowing others (the ecosystem) to build new industries upon it and then using consumption data to determine future candidates for industrialisation.  

As with climatic patterns and doctrine, then the more you play the game then the more context specific patterns you will discover. With your understanding of the landscape, an ability to anticipate change based upon climatic patterns and a knowledge of context specific play that you can use to manipulate the map then you should be able to determine where you could attack and how you can use gameplay to increase your odds of success. At the very least, you should be able to create a common understanding of where you’re going and why you’re taking certain approaches within the company — see figure 160.  

<figure>
<img src="1_v4AelceAffaJ3PAwKb5VCg.jpeg" alt="Figure 160 - Applying gameplay" />
<figcaption>Applying gameplay</figcaption>
</figure>

You then decide to act. You loop around the cycle and repeat this whole exercise. Don’t hesitate with action, make your plans and roll the dice. It’s worth remembering that one of your actions maybe to change direction of the company itself, to alter your very purpose. You might start of as a paper mill but you might become a telecommunications company. Get used to it, there is no “core” to a company beyond short term immediate focus.

# A few things to remember

## On biology

Terms like evolution, co-evolution, adaptation, red queen, competition, adaptive renewal systems, cell based structures, ecosystem, flow and awareness might make you think I’m talking about some form of biological system. That’s because I am. A business is a living thing not some physical machine. The more classical view of the machine has advantages in management thinking as it implies it’s simple and can be managed just by pulling the right levers or adding the right algorithm. This works fine if you’re in competition with others who think the same way but don’t assume everyone does.  

Biological systems are highly resilient to change in total. Individual members or species might be taken out by some disease or some catastrophic event but the system of life itself adapts and evolves through mutations in the entire population or exaptation (re-use of components for another purpose). A classical machine has a far more limited scope of resilience, no matter how well designed or scenarios considered and it does not evolve with its environment in the same manner. CS Holling distinguished between these two types of resilience as engineering versus ecological. Whereas engineering resilience is primarily about the efficiency of function, ecological resilience is focused on the existence of function.  

A **fragile** system is one with low engineering and ecological resilience. It has very limited constraints of physical operation and it cannot adapt or cope with change well. It breaks easily and ceases to function.  

A **robust** system is one with high engineering but low ecological resilience. It has a broader range of physical constraints that it can cope with but again it cannot adapt to unexpected events. Many classical systems are designed to maintain the efficiency of function given a set of broad constraints or defined changes e.g. loss of a single engine in an aircraft.  

A **fluid** system is one with low engineering resilience but high ecological resilience. Though elements of the system can be considered fragile (operating within limited constraints or occupying a niche), the system itself adapts rapidly to changing circumstances i.e. the efficiency of function might decline rapidly due to a change but the function continues to exist. Many biological ecosystems can be considered fluid and the process of change is known as evolution e.g. adaptation of a species to some new predator or environmental catastrophe.  

A **resilient** system is one with high engineering and ecological resilience. Not only is the system capable of coping with a wide variety of physical extremes, the entire system rapidly adapts to a changing environment in order to exist. Nature in its entirety can be considered resilient and it has become so through the process of evolution. Nature consists of many biological ecosystems occupying niches and any change in physical conditions enables one biological ecosystem to invade the space of another. The efficiency and survival of life is preserved bar the most catastrophic of shocks.  

This last point is critical. It is evolution through competition and a changing environment that has made Nature itself resilient. Evolution is driven by competition and far from the gradual and peaceful concept that abounds in literature, it involves the entire annihilation of species and individual biological ecosystems in a violent orgy of death throughout history. Species have evolved mechanisms to survive this orgy of death. Your body builds muscle because of constant exercise but burns that same muscle during starvation — it’s all part of our bodies energy management that has evolved to cope with change. Even death itself is a necessity to evolution and self replication with constrained resources.  

However, a consequence of this orgy has been diversity and whether it is diversity between or within species, this is a critical element of ecological resilience. Lack of diversity is often a major weakness of classical engineering systems through systemic failure. If you want to create a system that is capable of adapting to constant change, is resilient to the unknown and has the best shot at longevity as a whole then nature is a past master at this. Learn from life itself.

## On maps

Maps are about awareness. You should always remember :-  

1.  The map is constantly changing. These are living documents. With practice it should take a few hours to map a business from scratch and these have to adapt as you discover more. This is relatively simple if they become embedded as a means of communication.  

2.  Maps are a means of learning about the environment and communicating this. It’s an iterative process and it will take you years to become good at it. The really important lesson about maps is not how accurate or perfect they are but how you use them to continuously learn. Maps are not the “truth” but a guide which an entire army can collaborate and communicate around.  

3.  All models are wrong, some are merely useful. Someone will produce a more useful method of mapping, a better list of doctrine, a more insightful set of patterns. As there is no such thing as the “right” map, then feel free to alter the map in a way which makes it more useful to you.  

4.  If you’re feeling that this is a lot to take in, well it is. Strategy is not a simple topic despite our attempts to dress it up as such.  

You are now ready. Well, you might have been ready long ago but I wanted to give myself the best chance, so it’s more I am now ready. Forward friends and let us now play the game with a scenario in the next chapter.
