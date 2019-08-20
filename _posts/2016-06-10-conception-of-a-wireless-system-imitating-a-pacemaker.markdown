---
layout: post
title: Conception of a Wireless System imitating a Pacemaker
date: 2016-06-10 13:32:20 +0300
description: A wireless system conception project made in my preparatory school (TIPE)# Add post description (optional)
img: conception-of-a-wireless-system-imitating-a-pacemaker.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Conception, Preparatory School, Arduino, R&D]
---
In my second year of preparatory school, I handled all over the year a personal project of my choice. I worked 3 hours per week in a laboratory and more hours in my part time.

You can access my oral presentation here:

[Download the oral presentation]({{site.baseurl}}/assets/download/Bourgeois%20Gaspard%20-%20Conception%20of%20a%20Wireless%20System%20-%20Presentation.pdf)

# Introduction
Electromagnetic communications are everywhere, in phones, gps, magnetic cards. They are now gradually integrating the medical field, with for example the monitoring of wireless pacemakers. I'm interested about those technologies of data exchange. That's why I decided to reproduce an industrial device for remote communication at my scale.

# To structure my project
In order to start my project on solid basis, the 22th of December 2015, I visited a company specialised on pacemaker, called LivaNova (92). I met Renzo DAL MOLIN, the Director of Advanced Research in Livanova, he made me visit his company, and gave a lot of advice on how to imagine my system. He proposed to do a binary exchange thanks to Arduino tension. I really appreciated his help.
Then I went to the famous engineering school called Supelec in order to meet Anthony KOLAR, Teacher-Researcher at Centrale-Supélec, specialized in the design of integrated systems with high constraints applications in medical systems. Antony is brilliant and exactly the person I needed on my project. We worked together an afternoon in order to conceive the basis of my electronic system, explained after.

![Livanova Visit]({{site.baseurl}}/assets/img/conception-of-a-wireless-system-imitating-a-pacemaker/visit_livanova.png)
<center>Livanova Visit</center>
# My personal work
My work was organised around 3 parts :
- to conceive a wireless system on my own with the school materials I had.
I conceived a system, transforming a binary tension (5V/0V) to a magnetic signal. It represented my central. And then I conceived another system, reading that magnetic signal and converting it to a binary tension interpreted after by a computer. It represented the pacemaker. All of it constituted a wireless system communicating through wireless magnetic waves.

- to create an optimised protocol of communication between both devices
I took a number and converted it into a binary signal with an Arduino. Then I changed the length of the signal and the number of repetitions of the sequence, I analysed the good interpretation of the signal by another Arduino and also the time it took to transmit the number. I added a checksum in the binary signal to improve the communication.
[See the Arduino Code on GitHub](https://github.com/Gaspard-Bourgeois/arduinos-communication)

- to quantify the influence of the environment on the device range.
I put an equivalent system in different environments, including one imitating the pacemaker's one.

# Pictures of my work


![Electronic System]({{site.baseurl}}/assets/img/conception-of-a-wireless-system-imitating-a-pacemaker/electronic_system2.png)
<center>Me in front of the system sending a square signal</center>

![Electronic System]({{site.baseurl}}/assets/img/conception-of-a-wireless-system-imitating-a-pacemaker/electronic_system3.svg){:width="100%"}
<center>Plans of the system</center>

![Electronic System 2]({{site.baseurl}}/assets/img/conception-of-a-wireless-system-imitating-a-pacemaker/electronic_system.png)
<center>The wireless system</center>

![Blood Environment Simulation]({{site.baseurl}}/assets/img/conception-of-a-wireless-system-imitating-a-pacemaker/wireless_system_environment.png)
<center>Measure the impact of the body on the signal range</center>
