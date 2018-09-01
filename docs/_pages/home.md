---
layout: splash
permalink: /
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/homepage-feature.jpg
  cta_label: "<i class='fas fa-play'></i> Get Started"
  cta_url: "/docs/quick-start-guide/"
  caption:
excerpt: 'A Minecraft Server community providing helpful documentation and open source tools for running Minecraft servers.<br /> <small>Server Running: Spigot 1.12.2</small><br /><br />'
feature_row:
  - title: "Server Admin Guides"
    excerpt: "Learn how to build and manage your own Minecraft server for your friends and family, or learn to build a large public Minecraft server community."
    url: "/docs/server-admin-guide"
    btn_class: "btn--primary"
    btn_label: "Admin Guides"
  - title: "Server Admin Tools"
    excerpt: "Get the right Minecraft administration tools you need to build and manage your Minecraft server, as well as tools to help manage your server community."
    url: "/docs/server-admin-tools/"
    btn_class: "btn--primary"
    btn_label: "Admin Tools"
  - title: "Free as in Speech"
    excerpt: "Our website, server guides, and many of our server tools are Open Source to allow free and open access to building a Minecraft server or community of your own."
    url: "https://github.com/sk33lz/yourcraftserver"
    btn_class: "btn--primary"
    btn_label: "Learn More"
feature_row2:
  - image_path: /assets/images/logo.png
    alt: "vote for yourcraftserver"
    title: "Vote for YourCraftServer"
    excerpt: 'We are a growing Minecraft server community and can use the votes. Thanks!'
    url: "/vote"
    btn_label: "Vote now"
    btn_class: "btn--primary"
github:
  - excerpt: '{::nomarkdown}<iframe style="display: inline-block;" src="https://ghbtns.com/github-btn.html?user=sk33lz&repo=yourcraftserver&type=star&count=true&size=large" frameborder="0" scrolling="0" width="160px" height="30px"></iframe> <iframe style="display: inline-block;" src="https://ghbtns.com/github-btn.html?user=sk33lz&repo=yourcraftserver&type=fork&count=true&size=large" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>{:/nomarkdown}'
intro:
  - excerpt: 'Play @ mc.yourcraftserver.com'
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="feature_row2" type="center" %}

{% include feature_row %}

## Minecraft News

{% for post in site.posts limit: 5 %}
  {% include archive-single.html %}
{% endfor %}

[More Minecraft News](/yourcraftserver/news/ "More Minecraft News")
