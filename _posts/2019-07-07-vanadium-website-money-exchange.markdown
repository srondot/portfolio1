---
layout: post
title: Vanadium - Online Payment Plateform
date: 2019-07-07 22:13:20 +0300
description:
img: vanadium-website-platform-exchange.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Website, ENSAM]
---

During my first and second year in ENSAM, I joined the informatics students' union, a team of 3 students in charge of maintaining the wifi infrastructure and making some informatics projects. At that time, former students have made an offline website called Vanadium to manage all the payments inside the promotions, those payments include money exchange between all students and other students' union. The website was written mainly in both PHP Oriented Object and Javascript, transactions were saved on a local server accessed through SQL queries. At this time, the platform was used to save all the account balances in one place, the fiduciary money was handled by the leading students' union, creating and deleting money on the platform. We engaged with our promotion to put this useful platform online.

The website is only accessible by members of ENSAM with an account at [http://myvanadium.com](http://myvanadium.com). That's why I will present some pictures of the website in this page only. The task done by our team is presented, followed by a quick overview of the website for a better understanding.

# Define the needs

With the leading students' union, we planned several tasks to completely transform this platform, including:
* Migrate the platform online
* Enable some secured banking card top up on the platform
* Notify regularly by email members in bankrupt
* Get some statistics on expenses
* Improve the global design

# Organize and schedule tasks

Main goal was to have the platform working with card payment methods online before our second year in school. In fact, the platform was stopped on holidays only. We fixed to weeks during holidays to achieve it together. All the other tasks were to be done all along the year.

# Holiday work

Tasks done between first and second-year holidays in ENSAM by the informant's students' union.

## Migrate the platform online

We subscribed to an online host server and we bought a domain name server. We migrated both files and database. We performed several tests to ensure the integrity of data. We optimized the size of pictures to accelerate navigation.

## Enable the secured banking

Thanks to a partnership between school and Lydia, we could pay through Lydia payment platform. They were really few information on the procedure to follow in the web. We took contact with an informatics employee of Lydia to make our solution of payment secured.

# Second-year work

Task done by the informatics union on Vanadium all along our second year in ENSAM.

## Notify members by email

We defined a list of automatic messages for different profile cases. Some of them aimed at preventing bankrupt, some other at giving information about the account status. To perform regular tasks on a server, it is common to use CRON, unfortunately our server didn't allow it.
The idea was to perform the task on page loads. During every connection, hidden to them members check whether or not they are some emails left to send. Mails are sent after the page load to keep unchanged the user experience.

## Enhance statistics on expense

We wanted students to access the total money spent on the site, to have an evolution of expenses view, and to know how expenses were divided between each students' union.
An overview of the page in use is accessible [down there](#statistics).

## Improve the global design

We completely reshape the design of the website, from the background to the fonts in use. Our main objective was to enhance the user experience.

# Overview of the website

## Authentication page

![vanadium-authentification]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\authentication.png)

This page secure the access at the platform to members only.

## Main page

![vanadium-main]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\main.png)

The main page is divided in blocks containing, editable information, a ranking of last 2 weeks consumers, money balance in the platform, the one of your organization and the calculated one of your promotion.

## Historic

![vanadium-historic]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\historic.png)

Here you get a detailed overview of every past expenses, including data on dates, beneficiary organization, expense designation and amount . You can search through pages or thanks to a filter text box. The Ajax command aimed at filtering on key press directly.

## Money transfer

![vanadium-transfer]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\transfer.png)

Here you can send some money to others or ask to receive some. We match the member searched using Ajax prediction on typing, thanks to what you can't fail paying back.

## Statistics

![vanadium-statistics]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\statistics.png)

Some statistics on your expenses already introduced.

## Top-up your balance

![vanadium-online-payment]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\online_payment.png)

You can fill your account using your banking card on this page. The text box is used to generate a link needed to start a transaction on Lydia's website. We authenticate every user starting a transaction with a unique code sent and returned encrypted by Lydia. Those precautions are really important to secure our website from Cross-Site Scripting [(see more about it on Wikipedia)](https://fr.wikipedia.org/wiki/Cross-site_scripting).

![vanadium-online-payment-done]({{site.baseurl}}\assets\img\vanadium-website-platform-exchange\online_payment_done.png)
Once the payment done, we update our database with the appropriate value.
