---
layout: post
title: 'Tutorial: How to Generate A Self Sign Cert with OpenSSL on CENTOS'
date: '2015-03-31T23:31:00-07:00'
tags: 

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png
---


What is openSSL and SSL, and why should you care? 

The OpenSSL Project is a collaborative effort to develop a robust, commercial-grade, full-featured, and Open Source toolkit implementing the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) protocols as well as a full-strength general purpose cryptography library. 

SSL (Secure Sockets Layer) is a standard security technology for establishing an encrypted link between a server and a client—typically a web server (website) and a browser; or a mail server and a mail client.


 Normally, data sent between browsers and web servers is sent in plain text—leaving you vulnerable to eavesdropping. If an attacker is able to intercept all data being sent between a browser and a web server they can see and use that information. SSL allows sensitive information such as credit card numbers, social security numbers, and login credentials to be transmitted securely. 

It's pretty much straight forward, and easy to generate as illustrated below. 

{% gist 0ba9b3f3c966be074fa1 %}


