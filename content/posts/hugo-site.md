+++
title = 'Building a Static-Site With the Hugo Framework'
date = 2024-06-20T20:09:55-04:00
draft = true
tags = ['computing', 'go', 'hugo', 'web-dev']
+++

I did not have trouble getting [this site]() up at all. For several years up-until now I have long desired to launch a personal website and blog; I needed a place to keep all of my thoughts together, and to structure around some narrative ([being seen by the public at large](https://www.sciencedaily.com/releases/2018/04/180420122913.htm)) to both help me learn, and (perhaps) to help others as well. Yet as nearly all ideas fall to the wayside, so were my hopes of web (land) ownership dashed by incessant demands of work and school. And so I entered a long period, the search for an efficient framework for [static-site generation (SSG)](https://en.wikipedia.org/wiki/Static_site_generator), which went without much avail.

As a back-end developer, I have always found web development to be convoluted and too deeply obfuscated with too many dependencies, standards, and layers of abstraction. I **ALWAYS** stand by the [KISS principle]() ("Keep It Simple, Stupid!"). I have taken stabs at web development with courses in HTML/CSS and applying JavaScript web-frameworks like [React]() or [Next.js](). Although the basics are not complex, all of the paradigms that stand in-between the the rendered site in-broswer and the bare-metal process server-side do not serve as a good experience of dissection for one obsessed with the _why's_ and _how's_. And so, in keeping it all simple, I too needed an effective [Content Management System (CMS)](https://en.wikipedia.org/wiki/Content_management_system) into which I could quickly spin-up articles from Markdown files in my locally-hosted Obsidian repositories/knowledge base.

# Considering the Options

I had previously considered using [Pelican](https://getpelican.com/) but was very quickly turned off to the idea because it is written in Python. Python (and the [Python Software Foundation]()) with its numerous [known issues]() when it comes the many _intentional_ breakages between versions as well as all of its 3rd-party dependencies is not a language (nor platform) that I can feel any peace of mind with using. I was searching for something that was far more **simple** and **reliable**. I kept my eyes open, but was not keeping a look-out intensively.

Thus I came up with a list of _wants_ within an static-site generation framework:

1. A **simple** and **reliable** framework which is without extreme dependencies or suscept to random breakages and long-hours of needless tinkering and repair.
2. Support of simple Content Management System (CMS), i.e., Markdown.
3. **Lean** and **fast** content generation. I do not want to spend all day rebuilding the site after a single (small) change in some large quandry of HTML inheritence.
4. Written in a language that I understand (and thus is easily maluable to my needs).

In this, I also considered other classic SSGs like: [Jekyll](https://jekyllrb.com) and [11ty](https://11ty.dev), but they did not take my interest either. Jekyll is written in [Ruby](), which have no significant background in (nor any interest to learn at this point), and 11ty relies on [Node.js](), which I also try to avoid for the same reasons as stated above with Python. I briefly considered even writing one myself. If the job is not done well, then you might as well do it yourself, right? Yet, it was at this very moment that I stumbled across [Hugo](). Needless to say, when I did find out about Hugo, I was overjoyed. It really did tick off all of boxes, all the things that I wanted and/or really needed to see were present. If Go were Fort Knox, Hugo would be the biggest and shiniest gold bar in all the store.

# Diving into Hugo

Hugo, an open-source static-site generator written in Go famous for being the fastest way to render HTML in the world. Needless to say, it was love at first sight; and O I do bless you, [Fireship](), for introducing me to it in your ['Hugo in 100 Seconds']() on YouTube. After that video I dove head-first into the Hugo install and deployment. I followed the [quick-start guide](https://gohugo.io/getting-started/quick-start/) on the official documentation site, and within minutes I had a beautiful static-site spun up in mere minutes. Although known for it, the sheer speed with which it was able to generate the content still took me by surprise.

```bash
Start building sites …
hugo v0.127.0-74e0f3bd63c51f3c7a0f07a7c779eec9e922957e+extended linux/amd64 BuildDate=2024-06-05T10:27:59Z VendorInfo=gohugoio

                   | EN
-------------------+-----
  Pages            | 74
  Paginator pages  |  0
  Non-page files   |  0
  Static files     | 92
  Processed images |  0
  Aliases          |  1
  Cleaned          |  0

Built in 113 ms
Environment: "development"
Serving pages from disk
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
```

Only **113 ms**, O my! What a good deal. Following this I went over and checked out a series of tutorials from [Giraffe Academy](https://www.youtube.com/watch?embeds_referring_euri=https%3A%2F%2Fgohugo.io%2F&source_ve_path=Mjg2NjQsMTY0NTAz&feature=emb_share&v=ut1xtRZ1QOA). They helped me get a lot of my Hugo questions squared away, and I began to transfer a large chunk of my writings that I keep in Obsidian over to my content sections.

A [commenter](https://www.youtube.com/@mrbaeman39lolman60) on Fireship's video humorously noted:

> Hugo is the back-end developer's best friend for making front-ends.

And to that, my friend, I agree. I believe that once one gets a hang of its syntax and how it generates content, it is very easy to add new entries to or to customize to one's heart's desire—even for non-developers. So with that all said, to all readers: go off and have fun developing with Hugo!
