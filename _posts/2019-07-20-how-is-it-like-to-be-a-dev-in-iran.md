---
date: "2019-07-20 21:11:35 +0430"
title: "How is it like to be a dev in Iran"
categories: ["Iran", "Sanctions", "Coding"]
tags: ["iran", "sanctions", "censorship", "vpn", "tor", "fod", "privoxy", "named", "shecan"]
---

It is going to cover _cersorship_ and _sanctions_.

# Censorship

Censorship comes along with traces of governments ALWAYS!

In many contries allover the world, governments tend to block their citizens to
access some certain domains/ips across the internet. Some say "It's there to
keep culture and moral healthy!". They block pornographies and so. Even in US
we can find certain domains which are blocked and cannot be accessed like those
which contain CP or wild anti-humanism contents.

But in Iran (and most other countries) that's not the case!

They block many things. We cannot visit medias like BBC, FoxNews, VOA,
social-medias like Twitter, Facebook, messangers like Telegram, WeChat, Kik,
SnapChat, services like YouTube, you may not believe, but even some subdomains
of sourceforge!

**Why?** Because it is how the totalitarian government can live. Though they
sell VPNs and proxies, they spy on their people and they eliminate unwanted
elements of the society way easily. You may never find out what happened to your
friend who you just visited few days ago!

The filtering/cyber censorship, is a really profitable industry! For both, the
government AND non-governmental companies, as they get paid much more than a
typical IT company here!

Sometimes you see they place heavy filtering on some services, e.g Telegram,
to promote their own service! Sometimes they say fancy things about a service
like "It is Israelian!". I mean, so what? Haven't you used _Israelian_ weapons
during war vs. Iraq (1980-1988)? It wasn't a thing then, but now it is!

Sometimes they break SSL/TLS! I recently saw similar thing, [Kazakhstan
intercepting HTTPS Traffic][reddit-kazakhstan], officially MITM their citizens!

**Ok, what is affecting me, as a dev?** You know, their systems are not perfect.
Sometimes you come up with losing access to some must-have services, like
GitHub! Why? Because the filtering program has droped the connections to GitHub
because of accident/misconfigs! Sometimes you come up with totally broken SSL
handshakes! Sometimes SSL handshakes can take long forever and break at the end!
Sometimes CloudFlare resists to serve due to broken TCP packets!

It is pain in the ass when you are going to learn something new; no YouTube,
no Reddit, no Medium, painfull surfing the web and so on.

I don't talk about low quality internet access, like 200kB/s on home wifi!

# Sanctions

If you follow world news, you have definitely heard about sanctions against Iran
because of Iran's nuclear programs. Though it is not just limited to physics and
nuclear things, many companies have obeyed US sanctions against Iran.

No body really care about what would happen to the people. People worth nothing.
That's what they believe. Both Iran's government AND international institutes,
you say UN.

People are dying due to absence of medicines. People are starving.
The economy system is falling apart and the politicians and their children are
all abroad! None of them have any sense about what is going on the streets.

**What happens to us, IT men?** *Sanctions!*

**What are we missing?** _FOSS!_ We are missing _Free Open Source Softwares!_
You see?

[![Sanctions of Docker][sanc-docker-img]][sanc-docker]

Few months ago, Slack team, decided to join the sanctions. They simply deleted
every single user who they found out is Iranian! With no real prior notices!
Many people has lost their data on Slack and no one was going to do anything!
They had some Iranian users who was living abroad for many years and hasn't even
visited Iran for a long time, but their account got deleted along with others!
There were lots of peolpe complaining about it on
[T][sanc-slack-1][w][sanc-slack-2][i][sanc-slack-3][t][sanc-slack-4][t][sanc-slack-5][e][sanc-slack-6][r][sanc-slack-7].
[A][sanc-slack-8][n][sanc-slack-9][d][sanc-slack-10]
[e][sanc-slack-11][v][sanc-slack-12][e][sanc-slack-13][n][sanc-slack-14]
[m][sanc-slack-15][o][sanc-slack-16][r][sanc-slack-17][e][sanc-slack-18].
(I guess you [got the idea][sanc-slack-more].)

We cannot have MasterCard/VisaCard easily, thanks to economic banking sanctions.
Thus, we cannot create AWS account, we cannot buy anything on amazon/ebay, we
cannot have google store console, we cannot use (almost) any enterprise service.

[Android dev][android-dev] returns HTTP 403, [Docker docs][docker-docs] returns
HTTP 403, [bintray][bintray] returns HTTP 403, [Schema.org][schema-org] returns
HTTP 403 and so on. ([There is a long list available][fod-domains])

# Dev experience

You may have no sense of what I am talking about.
Imagine you are supposed to build something with a new technology you know
nothing about for your company. The first step is to find the technology
documentations and try to figure out how to make it work.

After googling the name of it, you find many related links including links to
the official documentations. You click on the link and suddenly an annoying ugly
stupid page pops out which has a big text on it "You are sanctioned by the US
and we cannot serve you".

You get back to the google results and try to find something else. You see
YouTube and medium links there but you know they are censored or unavailable for
where you live and you cannot use them either.

A link to a SO question takes your attention and you click on it. The question
is about something likely advanced in that technology and you have no idea what
are they talking about! You have no choice to get to google results, page 2.
On page 2 to page 100,000 there is no related links!

You go to your boss and tell him/her "This technology is not working here. Find
something else or cancel the project". Tomarrow you are looking for a new
position somewhere else!

# How do we survive?

We have to bypass both, sanctions and cersorship.

## HTTP proxies

Proxies are one of the (currently almost) working solutions.

It is not easy to find a proper proxy, it is not safe to use any proxy, and
proxies don't cover everything.

The domain list mentioned above is from a personal community funded proxy server
which only accepts the domains listed in that file and denies any other domain.
It is not an easy task for everyone to config their system to use that proxy for
those certain domains. And they don't cover _all_ domains, the list is getting
longer whenever someone finds some domains not covered and notices that to the
server owner. Another limit is that, this proxy does NOT cover cernsored
services.

## DNS proxies

There is a [DNS proxy][shecan] running by [Sharif university of
technology][sharif-ut] which can bypass sanctions only. But since it is
recommended by the government, it doesn't sound like a safe option! In the front
page, they have tutorials for users to set their DNS server on the OS to point
to the proxy servers, means the proxy server is going to resolve all your DNS
queries! Personally, I don't like a third party (which is recommended by the
government), to spy on all my DNS queries. I won't change my DNS server from
`1.1.1.1` to theirs!

## Public VPNs

Not a safe, but a working solution.

Free and paid VPNs are mostly driven by the government. They do spy on every
single request and investigate any suspicious thing they recognize. Obviously
compromising safety and privacy.

Any other non-governmental VPN gets banned by the government and you need to
look for new working VPN 2-3 times a week!

## Private VPNs

Safe and working but an expensive solution.

There are some private VPNs out there you can use, or you can even run your own,
they are completely safe and privacy friendly, but they're also expensive! Not
all people can buy/serve a private VPN.

## TOR project

The most reliable but not the best solution.

TOR is the unbannable privacy promising solution out there, which bypass
obviously both, sanctions AND censorship. But there is a big problem with it,
not all servers like to get traffik from TOR. For instance, CloudFlare annoys
when you are accessing its servers through TOR. Google makes you solve lots of
reCaptchas. And some servers simply don't serve anything due to odd TCP traffik
of TOR.

Besides, Iran's government has tried to limit connecting to TOR, though they can
never block TOR completety (unless they block foreign servers entirely!), but
they prevents you to connect to the TOR network directly. There comes obfs
bridges! However you need to get to bridge.torproject.org somehow first.

## How do I survive

I use a mix of all the above!

I have configed [bind/named][bind9] to proxy few certain domain queries through
[shecan][shecan] and [privoxy][privoxy] to tunnel all supported domains by
[FOD][fod] through FOD, and others through TOR.

I also use GitHub gists to save and spread TOR bridges among trusted people.

----

I just wanted to write about how difficult can it be to do all the things people
do daily without even thinking about it! I bet you cannot imagine internet
without YouTube. You never experienced losing your data all of a sudden with no
prior notice! You cannot believe how is it painfull to survive heavy censorship
and sanctions. You have no idea how is it like to wait for a VPN connection for
more than 10 minutes, and then get rejected!

The painfull fact is "All this is happening just because we are living in Iran,
where no one cares about the people. Not even the people!"

_Note:_ Please fix my typos and grammar mistakes. Thanks for reading.


[android-dev]: https://developer.android.com
[bind9]: https://bind9.net
[bintray]: https://bintray.com
[docker-docs]: https://doc.docker.com
[fod]: https://github.com/freedomofdevelopers/fod
[fod-domains]: https://raw.githubusercontent.com/freedomofdevelopers/fod/master/domains
[privoxy]: https://privoxy.org
[reddit-kazakhstan]: https://www.reddit.com/r/privacy/comments/cfglcu/update_kazakhstan_intercepting_https_traffic/
[sanc-docker]: https://virgool.io/DockerMe/%DA%AF%D8%B1%DB%8C%D8%B2-%D8%A7%D8%B2-%D8%AA%D8%AD%D8%B1%DB%8C%D9%85-%D8%AF%D8%A7%DA%A9%D8%B1-%D8%A8%D8%A7-%DA%86%D9%86%D8%AF-%D8%B1%D9%88%D8%B4-z6czoxibqnyk
[sanc-docker-img]: /assets/2019-07-20-how-is-it-like-to-be-a-dev-in-iran/sanc-docker.png
[sanc-slack-1]: https://twitter.com/imaN_Khoshabi/status/1075648863732752384
[sanc-slack-2]: https://twitter.com/blockchaindildo/status/1075834524649619460
[sanc-slack-3]: https://twitter.com/MaziR1989/status/1075660298835714048
[sanc-slack-4]: https://twitter.com/GamerGeekNews/status/1075849114972086272
[sanc-slack-5]: https://twitter.com/verge/status/1075976412224475141
[sanc-slack-6]: https://twitter.com/jabdi/status/1076146349719150595
[sanc-slack-7]: https://twitter.com/lrz/status/1075852522814926850
[sanc-slack-8]: https://twitter.com/tha_rami/status/1076924288639340545
[sanc-slack-9]: https://twitter.com/ponisha/status/1075642349575913472
[sanc-slack-10]: https://twitter.com/ahamidyousefi/status/1075620454801555462
[sanc-slack-11]: https://twitter.com/MattBinder/status/1075860343249879040
[sanc-slack-12]: https://twitter.com/kimaboe/status/1075891755705348097
[sanc-slack-13]: https://twitter.com/jonahedwards/status/1075802686614790144
[sanc-slack-14]: https://twitter.com/mahdi_slh/status/1075658656048402432
[sanc-slack-15]: https://twitter.com/TechForThePpl/status/1076186278725603328
[sanc-slack-16]: https://twitter.com/thehill/status/1075825437417312258
[sanc-slack-17]: https://twitter.com/kfvahedi/status/1076073199333449728
[sanc-slack-18]: https://twitter.com/__dc0d__/status/1076524955129524224
[sanc-slack-more]: https://twitter.com/search?q=slack%20iran%20since%3A2018-12-18%20until%3A2019-01-01&src=typd
[schema-org]: https://schema.org
[sharif-ut]: http://www.en.sharif.edu/
[shecan]: https://shecan.ir
