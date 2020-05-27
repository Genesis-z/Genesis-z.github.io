---
layout: post
title:  "My First bot - Telegram bot | python"
author: sal
categories: [ Python ]
image: assets/images/Telegram.png
beforetoc: "A step by step process to create your new telegram bot in python"
toc: false
featured: true
---

Telegram bots are simply  accounts operated by software – not people. They will be coded with AI intelligence, so that they can do anything like teach, play, search, broadcast, remind, connect, integrate with other services, or even pass commands to the Internet of Things.

The below are some of the bots available. You can search for their name in the search box and try it out to get idea on how does it work,

- [@PollBot](https://telegram.me/pollbot) – add this one to group chats to create polls.
- [@RateStickerBot](https://telegram.me/pollbot) – discover and rate new stickers.
- [@AlertBot](https://telegram.me/pollbot) – set a time and this bot will send you a reminder for anything you like.
- [@HotOrBot](https://telegram.me/pollbot) – find friends with this Tinder-like dating bot.
- [@GithubBot](https://telegram.me/githubbot) – track GitHub updates.
- [@StoreBot](https://telegram.me/githubbot) – find new bots and rate them.

It is very easy to create your own bot in telegram. All you have to do is use the [@BotFather](https://telegram.me/botfather)

![walking]({{ site.baseurl }}/assets/images/Botfather.png)

Type in `/start` and you can give your bot name and user name for the initial account creation. Then it will give you API secure token which you can use it in your code to control the bot.

![Botfather]({{ site.baseurl }}/assets/images/botfather2.png)

Your telegram bot is ready now.  A typical link to a bot looks like this:

<a href="https://telegram.me/your_bot">https://telegram.me/your_bot</a>


<p>Opening such a link starts a chat with that bot if you have Telegram installed. These links are easy to identify because all bot usernames must end in <strong>bot</strong>. If the bot developer wants to pass their bot some additional info (like an auth key for example, see <a href="https://core.telegram.org/bots#deep-linking">deep linking</a>), the link might also look like this:</p>

<p><a href="https://telegram.me/your_bot?start=value">https://telegram.me/your_bot?start=value</a></p>

<p>To get response from
your bot, you need to include your API key with your code to control your bot.
Your code can be in any language like GO, python, Java.</p>

<p>Here I used Python.</p>

<p><script src="https://gist.github.com/Dimension8d/59a6e97074a876f0edc85b3d13fa7673.js"></script></p>

<p>Please use your API token key and you can change the Bot name as per your requirement.  After you run the python code, then you could see response from your Bot. </p>

![Botfather]({{ site.baseurl }}/assets/images/Botfather3.png)

Hope this is useful. Would explore more on this and will share in coming days.