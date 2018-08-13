---
title: "Rocket.Chat accelerates collaboration at Southeastern Louisiana University"
categories:
  - Case Studies
  - News
date: 2016-06-13 14:04:15
author: Marcelo Schmidt
cover: /images/posts/2016/06/rocketchat-accelerates-collaboration-at-southeastern-louisiana-university/cover-accelerates-collab.jpg
redirect_from: /blog/rocketchat-accelerates-collaboration-at-southeastern-louisiana-university
---
<img style="float: right; margin: 0px 0px 50px 50px;" src="/images/posts/2016/06/rocketchat-accelerates-collaboration-at-southeastern-louisiana-university/image00.jpg" width="100" />

We recently spoke with Matthew Gill, a System Administrator at Southeastern Louisiana University where they have adopted Rocket.Chat for collaboration across the technology development team.

### The team trials chat solutions

"Generally speaking, our teams had been using ICQ as the go-to service for internal communication but its biggest problem was the lack of cohesion and centralized communication possible on the platform. You could send individual private messages and there is a rudimentary chat-room-like functionality, but the solution itself felt lacking."

After that they tried Google Chat but most team members went back to ICQ pretty quickly. Matt tried to encourage the teams to use more innovative platforms but funding was limited; "departmental funding was never allocated to purchase a solution, so we effectively needed something free."

Slack was next and the team used that for a few months before realizing that the free version wasn't going to achieve everything they needed. "We liked the features, but would never be able to afford it."

They tried freeware, including ChatGrape and Glip, but found the services weren't as accessible as the team needed them to be and required more admin due to team members creating different accounts.

"In the end I brought three standards to my supervisor. The communication platform to replace everything we were using up until then needed to be locally hosted, configurable (open source would be great) and able to use our Active Directory authentication (ldap)."

### Matt discovers Rocket.Chat

Matt came across the okTurtles blog entry [Five Open Source Slack Alternatives](https://blog.okturtles.com/2015/11/five-open-source-slack-alternatives/), which led him to Rocket.Chat.

"I remember initially fiddling with MatterMost but when I jumped into the public RC open server and tested out the features, I was a believer!" That version was a little buggy at the time but Matt immediately saw its potential.

Matt created a VM to host the Rocket.Chat and MongoDB server and installed and configured the system without container management.

In retrospect, he says he might have deployed using Docker, but hosting the system on a VM allowed them to migrate easily to an existing Disaster Recovery site and create near-instant clones.

### The team adopts Rocket.Chat

The team was initially slow to adopt Rocket.Chat, so Matt arranged meetings with all the team-leads in the department. Rocket.Chat was fully implemented and is now adopted by nearly 100% of all teams.

"Our department is separated into three teams: Infrastructure, Services and Software. Despite being split into separate teams with seemingly clear duties and responsibilities, members of different teams are often found working on solutions outside of their original team. Cross-collaboration is important and effective communication helps immensely.

"From a software design aspect we've integrated GitLab and Active Directory automation into a channel in Rocket.Chat. This allows those responsible to quickly get updates on changes in important repositories and status changes affected by automation. All without reading an email."

### "Ideas are communicated better and quicker"

"Intra-team communication has benefitted greatly and the quick search feature built into Rocket.Chat means users are easily able to recall information sent to them from other team members. This is a big change from sticky-notes and poorly-subjected emails!"

"Perhaps the most noticeable change is that our teams are finally able to collaborate using easy private groups and channels. Ideas are communicated better and quicker, development time has benefitted and team participation has risen."

"Despite only having about 60 active members, over 44,000 messages have been sent, spread over 300 rooms and channels and over 200 direct message rooms!"

### "There are so many awesome features packed into Rocket.Chat"

SLU have been using Off-The-Record, OTR, WebRTC (Audio/Video Chat) and will likely begin to use LiveChat.

"All in all, Rocket.Chat is a fantastic, feature-rich communication platform that has greatly increased productivity across the board for all teams involved."

"I look forward to the features outlined in the posted roadmap, including the native mobile applications and XMPP support!"


If you're interested in contributing a customer story to our blog, [please get in touch](https://rocket.chat/contact)!

<a style="background-color:black;color:white;text-decoration:none;padding:4px 6px;font-family:-apple-system, BlinkMacSystemFont, &quot;San Francisco&quot;, &quot;Helvetica Neue&quot;, Helvetica, Ubuntu, Roboto, Noto, &quot;Segoe UI&quot;, Arial, sans-serif;font-size:12px;font-weight:bold;line-height:1.2;display:inline-block;border-radius:3px;" href="https://unsplash.com/@jannerboy62?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge" target="_blank" rel="noopener noreferrer" title="Download free do whatever you want high-resolution photos from Nick Fewings"><span style="display:inline-block;padding:2px 3px;"><svg xmlns="http://www.w3.org/2000/svg" style="height:12px;width:auto;position:relative;vertical-align:middle;top:-1px;fill:white;" viewBox="0 0 32 32"><title>unsplash-logo</title><path d="M20.8 18.1c0 2.7-2.2 4.8-4.8 4.8s-4.8-2.1-4.8-4.8c0-2.7 2.2-4.8 4.8-4.8 2.7.1 4.8 2.2 4.8 4.8zm11.2-7.4v14.9c0 2.3-1.9 4.3-4.3 4.3h-23.4c-2.4 0-4.3-1.9-4.3-4.3v-15c0-2.3 1.9-4.3 4.3-4.3h3.7l.8-2.3c.4-1.1 1.7-2 2.9-2h8.6c1.2 0 2.5.9 2.9 2l.8 2.4h3.7c2.4 0 4.3 1.9 4.3 4.3zm-8.6 7.5c0-4.1-3.3-7.5-7.5-7.5-4.1 0-7.5 3.4-7.5 7.5s3.3 7.5 7.5 7.5c4.2-.1 7.5-3.4 7.5-7.5z"></path></svg></span><span style="display:inline-block;padding:2px 3px;">Nick Fewings</span></a>
