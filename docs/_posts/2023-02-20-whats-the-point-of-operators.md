---
title: "What's the point of a telco?"
tags: [ telecom, business ]
layout: post
---

One night last year, a man and his colleagues stood outside in the cold and filmed 
a [short selfie video](https://youtu.be/48I00K4nJJk 'Zelenskyy's video after Russian attack'). 
The effect was electrifying. _We are here. We're going to fight._

That message was carried by a telco operator. 
When you post, or stream video, from your phone, it sets up a channel to carry the data across 
the ether to the nearest cell tower, which in turn sends it to a piece of software,
rather grandly called a packet core. Cell towers, packet cores, and all the infrastructure needed 
to get your data to the Internet are run by telco operators. Now that we live in a world where a 
tweets and videos rally a populace to fight, it's worth restating: 
this network stuff is _important_.

It's also strangely difficult to make money at. Let's look at the 5-year stock performance for a few bellwethers:

| Operator       | Stock | Feb 2018  | Feb 2023 |
| :-------       | :---- | -------:  | ------:  |
| Verizon        | VZ    | $ 50.15   | $ 40.22  |
| AT&T           | T     | $ 29.06   | $ 19.44  |
| Vodafone Group | VOD   | £ 201.80  | £ 92.08  |
| Comcast        | CMCSA | $ 39.79   | $ 39.12  |

Oof.  

Faced with this, operators must ask themselves: what is our purpose? Will people pay for what we 
are good at, and, if they won't, what should we do? There are a couple of ways that this plays out.

1. We have the best network. People will pay a premium for that, surely.

   The message is unambiguous to both the customer base and to the employees who actually have to implement it.
   An operator who takes this path is on the hook to support continual
   expansion and capacity improvements to keep the network humming along. Somebody somewhere at this operator
   is going to spend many hours poring over network telemetry and JD Power 
   [surveys](https://www.jdpower.com/business/press-releases/2023-us-wireless-network-quality-performance-study-volume-1).
   It's also very expensive to pull off. It doesn't help that operators already carry lots of debt, and 
   interest rates are rising, so it's difficult
   to spend their way to happiness. On the bright side, there is a lot of scope for innovation _if_ the operator
   can overcome their traditional aversion to risk: use of AI for network monitoring, deep automation of the network,
   and other modernizations could transform how operators run their networks (but note the cautionary tale of NFV,
   discussed elsewhere).

2. Network, blah. Let's get hold of content, and charge for that.

   There's charging for access to content, and there's owning content. The cable operators know how to do the former,
   because they've been ~~holding sports fans hostage~~managing rightsholders for years. When you own the set-top box, 
   you can negotiate the toll that even OTT providers must pay to be featured in front of the viewers' eyeballs. 
   Of course, if you are smart, you'll play nice, or else your customers will all buy Rokus and relegate you to 
   being the cheap pipe again. In any case, gatekeeping won't work forever: the device manufacturers (TVs, phones, etc.) 
   all have their own financial incentives to take control of the user experience, and Google/Apple make it 
   nice and easy for them.

   Or you could take a deep breath and buy content. I can think of only one operator that has pulled this off,
   Comcast (NBC Universal, 2011), and you could argue that they already knew what they were doing since they
   owned several TV channels and media properties already. The others...eh, not so much. 
   AT&T/TimeWarner (2018) is now a business school [case study](https://rbr.business.rutgers.edu/sites/default/files/documents/rbr-060309.pdf) in failure 
   and the best that analysts could find to say about Verizon/AOL/Yahoo was "at least you only burned $4B" 
   ([CNBC report](https://www.cnbc.com/2018/12/11/verizon-made-the-right-decision-not-to-be-big-on-media.html)). 
   But all you armchair quarterbacks need to sober up: leadership made tough calls with imperfect data.
   
3. Why do the content people get all the money? We should be charging them rent for using our pipes.

   This is the repeal-Net-Neutrality argument in the US, and in Europe, 
   the [Fair Share](https://www.vodafone.com/news/corporate-and-financial/european-digital-infrastructure) one. 
   The Internet hive-mind is profoundly opposed to this, but the request does comes from a place of genuine pain, 
   as opposed to merely rent-seeking. Mobile data traffic on AT&T increased by a factor of 1,000 in just seven years 
   to 2014. None of that was AT&T's doing: they just got crushed by the combination of phones that could handle video
   and Netflix being more than happy to oblige. It's anybody's guess whether we have reached "peak data", but, assuming
   not, then networks are going to continue to be capacity constrained, and operators are going to continue to ask 
   their governments and regulators for relief. In a supreme irony, operators have such an unfortunate reputation for 
   taking government funds and not delivering on their promises that this path may end up being closed to them for 
   political reasons. 
   
4. Consumers are fickle gods. Let's sell more to businesses.

   Internet service. Private 5G networks. Office 365 seats. Security features. Operators could sell these and other products. But here's the
   unpleasant secret about operators: the most lucrative products either have terrible margin or high customer acquisition costs for them.
   An operator can sell a ten thousand 365 seats...but most of that money goes to Microsoft. They can sell Internet circuits
   ("DIA", in the lingo) with their eyes closed...but it takes 60 days at best before the customer is generating money, because
   the address has to be checked in a giant IT system to see if fiber passes the building, someone has to order a box for the customer, the customer
   needs to successfully install the box (or the operator has to do a truck roll), ...and DIA is the *easy* case that, the one that
   operator sales people love to sell. Try getting them to sell private 5G or hosted voice PBX services and they will nod and smile
   and mentally calculate how much quicker their commission check arrives if they just carry on selling Internet. 
   
6. Shareholders above all. Squeeze every penny out of the customers that stay, and jettison the rest

   This is the easy button, up to a point. Did your bill go up, for no obvious reason? Congratulations, your operator
   is in this bucket. Cell service is remarkably sticky (churn rates are under 2%, and 2% would be considered worryingly high).
   What about the jettisoning part? If your operator serves fixed (landline) customers, they would love love *love* to be able to move these
   customers over to cell service or junk them completely. Unfortunately regulators like the US FCC take a dim view of that, and it doesn't help
   that the places with a lot of legacy landlines also tend to be in rural places that don't have good cell coverage. We won't see
   any movement here until a more agreeable regulatory and legislative environment takes shape. It's been possible to deliver voice over Internet and over cell service
   for getting on 25 years and yet here we are, so I don't think much is going to happen here. Ironically the smaller telco operators,
   who are closer to the communities that they serve than the national operators, might be in the vanguard here.

So there you have it. If that all seems a little gloomy, it's not - more a recognition that despite the billboards, Super Bowl ads, analyst briefings, 
and all the other assorted noise, an operator is a utility, and the market should treat it as such. It is high time that operators stopped 
trying to convince the world that they are just like the cool kids in the Valley, and regained their self-respect as key providers of an essential infrastructure.
