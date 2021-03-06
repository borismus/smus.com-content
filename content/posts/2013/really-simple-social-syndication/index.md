Really simple social syndication
================================
posted: 2013-03-14

I've been thinking about this for a while, but the recent [sunset
announcement of Google Reader][sunset] made me revisit this topic.
Google Reader isn't the only thing that's dead. RSS (aka. Really Simple
Syndication) has long been proclaimed dead as well. In fact most people
never even knew what RSS was. That said, it was a very useful tool for
me and many others that like to stay up-to-date in their areas of
interest. Increasingly, I've been getting my dose of news through social
networks. However, social networks contain a lot of noise that I care
little for. I want to rebuild the RSS spirit using modern social
networks. This post describes one possible approach, which I refer to as
**Really Simple Social Syndication (RSSS)**.

<!--more-->
[sunset]: http://googlereader.blogspot.ca/2013/03/powering-down-google-reader.html

## Really simple syndication: the good old days

Here's what the content flow used to be with blogs and RSS:

![RSS-based content syndication](rss-flow.png)

It was simple. Really simple, actually!

## Social syndication: today

I don't care much for social networks. I mostly see them as a two-way
utility for ultimately connecting content creators to content consumers.

One way, social networks like Facebook, Twitter, G+, etc are just
vehicles for finding out what to read based on your interests. I spend
too much time checking them individually for my news, and this is
unfortunate. 

The other way, social networks make it easier to have your content read
by a bunch of the right people. In my case, the vast majority of
non-organic search traffic comes from social sources (mostly twitter). I
waste a bit of time tweeting, and G+ing new posts on my blog as they
come out, but sometimes they are picked up by others and I don't
actually need to do that.

As long as the content itself stays outside of the walled gardens of the
social networks, I think we can come to a syndication solution that
might rival the old RSS-based one, but enjoy the benefits of having some
extra signals from all of the social network junk. Here's the model I'm
thinking of:

![Social-based content syndication](social-flow.png)

Now for a little bit more about Pub and Sub.

## Sub: Requirements for consumption

- **Reuse existing feeds**. I don't want to re-create my sources. Use
  existing people you follow on Twitter, from G+ circles, Facebook
  friends.

- **De-duplicated content**. Some people post the same link on multiple
  networks. Some popular posts are reshared by everyone. I only want to
  see a post once.

- **Content centric**. Show me the content in some standard, readable
  way. Hide the social stuff unless I explicitly ask. Most of the time I
  don't care where it came from, don't care how many people liked it, or
  what they wrote in the comments. Sometimes I'm curious and want a way
  to trace it back.

- **Social signals as a metric**. If many of my sources share something,
  I probably should at least take a skim.

- **Web based service** so that I can use it anywhere.

- Set a **volume-based daily quota**. If I'm busy today I'd like to only
  see the top N articles, sorted by some transparent metric of my
  choosing.

Flipboard, Pulse, Feedly all sort of fit into this class of readers.
Ideally this would be an API that just lets me connect a few social
accounts, and get back a filtered feed of content. This could be the API
for the product - a Really Simple Social Syndication (RSSS) feed.

Anyone could then build a UI on top of it for their favorite platform
(Google Reader-like).

## Pub: Requirements for content production

- Automatically post content to a bunch of social services. 

- Intelligent shortening of links and content (eg. for twitter, to fit
  in 140 chars).

Wordpress plugins, Tumblr and others provide ways to automatically tweet
and otherwise post new updates to your content. There needs to be some
other way that works in general for any type of content. Such a service
could be similar to feedburner, in that it would take an existing RSS
feed and socialize it.

## Social networks, let's be friends!

I'm not religious about Google Reader or RSS. It was a good solution for
content syndication at the time, but I'm ready to accept that perhaps
it's time to move on. Hopefully with tools like the above, we can have
something that comes close to the utility of RSS feeds.

Social networks could do some evil stuff which would preclude RSSS from
happening. Economically, they are incentivized own content, create
walled gardens, insert advertisements, and prevent access to their
feeds. I'm hoping that some human element will prevent that from
happening.

Here is a short list of what we need from the social networks:

- The content itself must be free from walled gardens (eg. paywalls,
  login walls, etc)

- Social network feeds are available to read in full, as is, without
  magical suggestions, collaborative filtering, etc.

- Social networks provide some programmatic way to post content.

Once we have a good flow for the production and consumption of content,
using social networks as a delivery mechanism, I will be very happy to
minimize the amount of time spent on social networks directly, and focus
on consuming and producing interesting things. Also, happy &pi; day!
