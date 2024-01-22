---
layout: post
title : "What's the point of a telco?"
date  : 2023-02-20 19:00:20 -0500
tags  : [ "telco", "business" ]
---

One night last year, a man and his colleagues stood outside in the cold and filmed 
a [short selfie video](https://youtu.be/48I00K4nJJk 'Zelenskyy's video after Russian attack'). 
The effect was electrifying. _We are here. We're going to fight._

That message, from Ukrainian President Volodymyr Zelenskyy, was carried by a telco operator. 
When you post, or stream video, from your phone, it sets up a channel to carry the data across 
the ether to the nearest cell tower, which in turn sends it to a piece of software,
rather grandly called a packet core. Cell towers, packet cores, and all the infrastructure needed 
to get your data to the Internet are run by telco operators. Now that we live in a world where a 
tweet can move markets and a video can rally a country to fight, it's worth restating: 
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
5. Shareholders above all. Squeeze every penny out of the customers that stay, and jettison the rest

