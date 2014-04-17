---
layout: post
title: Hackers crack more than 60% of breached LinkedIn passwords
date: '2012-06-07T18:07:00-07:00'
tags:
- Linkedin
- Hack
- social media
tumblr_url: http://blog.lovellfelix.com/post/24639600648/hackers-crack-more-than-60-of-breached-linkedin
---
More than 60% of the unique hashed passwords that were accessed by hackers from a LinkedIn password database and posted online this week have already been cracked, according to security firm Sophos.
It’s very likely the remaining passwords have also been cracked, said security researcher Chester Wisniewski late Wednesday.
In all, a total of 6.5 million hashed password believed to belong to LinkedIn members was posted on a Russian hacker forum earlier this week. The crooks posted the data in an effort to get help in cracking the passwords.
Sophos said it identified about 5.8 million hashed passwords as unique. 
Based on an analysis of the 118MB password dump, Wisniewski said close to 3.5 million of the unique passwords had been cracked and made available in plain text by late last night. It’s only a matter of time before the remaining passwords are similarly cracked using automated password guessing tools, he added.
The speed at which so many hashed passwords were cracked underscores the weakness of the passwords protection scheme used by LinkedIn, Wisniewski said.
The breached LinkedIn member passwords were all hashed, or masked, using a hashing protocol known as SHA-1.
Though SHA-1 offers a degree of protection against password cracking attempts, the protocol is by no means foolproof.
Therefore, many organizations theses day use a process known as salting — where a random string of characters are appended to a password before it is hashed— to make password cracking much harder. The process ensures that even if two passwords are identical, their hashes will be unique.
Salting is considered something of a best practice for protecting passwords, especially those used by employees of large companies.
That LinkedIn apparently chose to protect passwords using just SHA-1 is disappointing, Wisniewski said. “They chose a moderate security method. For an organization as large as LinkedIn, I would expect better,” he said.
The worst policy for companies is to store passwords in clear text, experts say.
Storing them in hashed form with no salting is nearly as bad, considering the availability of SHA-1 hash cracking tools, Wisniewski said. Tables that contain pre-computed hashes for billions of passwords are easily available. Almost anyone can use these tables to decrypt almost any SHA-1 hash and recover it in plain text in in a matter of minutes.
In response to widespread reports about the breach, LinkedIn yesterday admitted that “some” of its passwords might have been compromised. So far, the company has not indicated how the breach occurred or how many passwords may have been compromised.
In a carefully worded blog post LinkedIn director Wednesday Vicente Silveira said that the company had disabled all the compromised passwords and was instructing affected members how to access their accounts to reset their passwords.
In an apparent response to the focus on the unsalted hashing issue, Silveira noted that LinkedIn recently added enhanced security measures for salting and hashing its password databases. Silveira’s post does not indicate when LinkedIn began the practice.
The compromise is a big deal for LinkedIn users, said John Pescatore, an analyst with Gartner. “LinkedIn definitely had to have some kind of serious security incident for this to happen. And they probably had lax security policies or controls for a simple unsalted hash file like this to exist,” he said.
One worrisome aspect of the breach is that it could enable more targeted phishing attacks, he said. “LinkedIn is a great research site for hackers creating targeted phishing attacks to go after system administrators, CFOs, etc.” he said. “If they had access to the non-public parts of people’s LinkedIn profiles we will see even better targeted phishing attacks.”
