---
title: 'Brief journey of setting up graphql to send email using nodemailer and gmail'
excerpt: 'Setting up mail notification using nodemailer, gmail'
coverImage: '/assets/blog/email/cover.jpg'
date: '2022-11-03T05:35:07.322Z'
author:
  name: Jose KJ
  picture: '/assets/blog/authors/tim.jpeg'
ogImage:
  url: '/assets/blog/email/cover.jpg'
---

Used nodemailer package please checkout https://nodemailer.com/usage/


configured the follwoing in gmail  the follwoing steps to successfully send email [copied from stackoverflow answer https://stackoverflow.com/a/73327545/19976827]
   1.  Open Mail > Settings > See all Settings > Forwarding and POP/IMAP.
   2.  Enable POP download: & Enable IMAP access: (then save the settings).
   3.  Open Your Gmail Account > security > 2-step verification(enable it).
   4.  Go to App Passwords > select device > select app(you can create any custom app).
   5.  Copy App Password and use it in your application

just follow the node mailer sending mail doc, then add service, username, password, title, text, subject and then u are ready to send mails.... not that hard

other email services u can use are aws SES which has araound 62,000 emails per month if u call the from an ec2 instance.

