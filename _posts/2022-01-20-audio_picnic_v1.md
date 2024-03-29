---
layout     : post
title      : "Audio Picnic v1"
date       : 2022-01-20
categories : distributed synthesis
---

![beautiful souls](/etc/images/audio_picnic_v1_wide.jpg)

on Sunday, Jan 16, we had a picnic - this was very lovely!  many thanks to the beautiful souls who attended.

##	footage

{% include youtube_player.html id="gg9udLivhFA" %}
*footage by [Lauren Abineri](https://linktr.ee/laurenabineri)*

{% include vertical_player.html id="fU5gW7LWle8" %}
*footage by [jankbowie](https://www.instagram.com/jankbowie/)*

##	discussion

within a few minutes, four issues became apparent:

0.	getting connected
0.	staying connected
0.	REPL overload
0.	amplitude


###	getting connected

not everyone was able to connect frictionlessly. all phones were able to connect eventually, but some phones did not support qr codes, and others would search the ip address as a string in a search engine rather than passing it to a web browser as a URL.

###	staying connected

after joining the instrument, many participants reported that, without user interaction, the phone would sleep its screen.  when this happened, the result became unpredictable:
-	some of the phones stayed connected and active, continuing to make sound,
-	others stopped making sound altogether,
-	while others still continued to make sound, but became unresponsive to websocket communications.

![a websocket](https://socket.io/images/bidirectional-communication.png)
*from [socket.io](https://socket.io/docs/v4/)*

frustration at not being able to instruct their phone easily to stay awake, caused some people to give up on participation with the instrument, and instead resume other picnic related activities.  others persisted, continually unlocking their phones, refreshing the page, and rejoining.

two corrolaries of participants constantly rejoining:

0.	save / load function was significantly impaired, as states were saved localy in the webpage, which were lost upon refresh.
0.	the REPL was inundated with messages regarding new users joining (see below)

although most phones have settings that can be tweaked to stop the phone from sleeping, the best solution would one that stopped phones from sleeping from inside the webpage, which would shield users from having to confront the clumsiness of their relationship with their phones.

###	REPL overload

about a week earlier, on Saturday, Jan 8, I had played a show at [Ancient World](https://www.instagram.com/p/CYc2Z-wvcve/), where I decided to try my hand at live-coding.  it was a rewarding challenge - I will most likely keep live-coding as a central workflow for my solo electronic music project, assembly, with a view to doing more live-streaming, and more involvement with [ALGORAVE](hhttps://algorave.com/about/) & [TOPLAP](https://toplap.org/about/).  inspired by my experience working with [Tidal Cycles](https://tidalcycles.org/), I decided to build a live-coding interface for the DX∑.  

creating a custom REPL was [fairly straightforward](https://nodejs.org/en/knowledge/REPL/how-to-create-a-custom-repl/).  you can see the REPL being used in the videos below, to both accept input and display information:

<br />

{% include youtube_player.html id="SQQTjOQhR8c" %}

<br />

{% include youtube_player.html id="RWI_kNpGOlI" %}

<br />

{% include youtube_player.html id="YREAv5AwLXI" %}

<br />

during the picnic, however, a considerable limitation of the REPL approach became apparent fairly quickly.  the main problem being that data output by the REPL appears at the command line, ie. in the same place you input text commands.  each time information is printed to the command line, the input text you may or may not be half way through typing, is interrupted.

it seems the neatest solution to this would be to build a DX∑ Atom package, allowing users to evaluate blocks of code directly in the text editor, similar to the [Tidal Cycles plugin for Atom](https://atom.io/packages/tidalcycles).

###	loudness

much of the feedback from participants pertained to perceived loudness - there are two sides to this: physical amplitude / cultural infrastructure (ie. "expectation management").  there is a lot to talk about here so I will dedicate a separate blog post to this.


##	other notes

the text messaging worked really well! I will post a more compreshensive discussion about this, including some notable performers who do similar things, and what such an affordance might mean for the DX∑.

![next time](/etc/images/audio_picnic_v1_next_time.png)
