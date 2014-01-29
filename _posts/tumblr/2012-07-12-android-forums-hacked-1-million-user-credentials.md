---
layout: post
title: 'Android Forums hacked: 1 million user credentials stolen'
date: '2012-07-12T18:02:41-07:00'
tags: 
tumblr_url: http://blog.lovellfelix.com/post/27081562378/android-forums-hacked-1-million-user-credentials
---
Phandroid’s AndroidForums.com has been hacked. The database that powers the site was compromised and more than 1 million user account details were stolen. If you use the forum, make sure to change your password asap.


I have some unfortunate news to pass along. Yesterday I was informed by our sever/developer team that the server hosting androidforums.com was compromised and the website’s database was accessed. While the breach is most likely harmless there are important and potential pitfalls, and we want to provide as much helpful information to our users as possible (without getting too technical).

The trust of our users is extremely important and several staff members worked through the afternoon, evening, night, and morning to ensure we’re doing everything possible to regain complete security.

Here are the facts:

- The exploit used has been identified and resolved. The server has been further hardened and extra “just in case” actions have been taken.. and will continue to be taken.

- All code that resides in the database and the file system has been thoroughly reviewed for malicious edits and uploads.

- No other sites in our network appear to have been accessed (we’re triple checking).

- The user table of AndroidForum’s database was (at a minimum) accessed. While we can’t prove or disprove whether or not the data was downloaded (due to the way the data was transferred), it’s completely possible.. and we’ve taken action assuming this is the case. 

- Information in the user database includes: Unique ids, usernames, emails, hashed (encoded) passwords, registration IP addresses, usergroup memberships, infraction levels, last time online, last post date, post count… as well as far less critical things like number of PMs, visitor messages, last online dates, and some vbulletin options set in your UserCP.

- Immediately following the incident, all ~100 staff were notified of a pending password change - and all passwords to were changed to random strings. Almost all are back in with new passwords. Because gaining access to a staff member account could pose the biggest threat, we first moved to secure these accounts. 

What Probably Happened

This was, in our current opinion, most likely an e-mail harvesting attempt. A spammer could theoretically attempt to bulk e-mail all AF users with the user database. Luckily, GMail and similar e-mail services offer a “spam” button that helps it to collectively identify and automatically filter potential spam.

It’s also absolutely possible that nothing of consequence happened. There is some chance they did not get enough of the database to matter, did this for fun to see if they could, or will not move forward with any plans after finding out we’re actively investigating. This is a serious offense and you can best bet we are doing just that.

What Could Happen?

We take matters like these incredibly seriously and want to make sure you’re warned of ALL the possibilities, regardless of how slim the chances. You can never be too safe, so we’re asking you to consider the possibilities and protect accordingly.

- This could be someone who is upset with us who hopes to use the information against staff

- With username, email, and IP information, a skilled hacker could pretend to be other users.

- They could blackmail us and threaten to publish the information publicly.

- Knowing your IP one can get a general idea of where you are located in the world, though most your IPs are dynamic and will change before too long anyway. 

- With a username and hashed password one could open a session with accounts on other sites that use the same credentials - if they gain file level access to that site first. 

What should you do?

Although we’re confident the threat is neutralized it is still highly recommended that you change your password here and on other sites where you use the same username/password. This can be done while logged in through your UserCP, or using the “forgot your password?” page if logged out. You can also contact me via PM orContact Form and we will help you if you need.

No website wants to make an announcement like this. I assure you we, as the Neverstill Team, could not apologize profusely enough. Websites come under attack all time time - and sometimes the bad guys make it in. Unfortunately for us, yesterday was our time. We have been attacked before but never breached, and please know we are going to continue to do everything in our power to ensure it doesn’t happen again. 

If you have any questions please let us know - we will do our best to answer them. I will leave this thread open for discussion as long as it remains productive.

-Phases, Rob, and the Neverstill Team

UPDATE: I forgot to mention. If you are using the Android Applications - they will not register the password change and may flood your email with “someone has tried to access your account” emails. Unfortunately the only advice I have for that is to uninstall/re-install the app, if you cannot change your password from within.
