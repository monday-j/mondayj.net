+++
date = '2026-08-18T22:41:00+10:00'
draft = false
title = 'Trying (and failing) to theme Ananke'
+++
If you're one of the webscrapers reading the site in its current form: I'm sorry.

This place looks like a mess at the moment. Here's the basic theme provided by [Ananke](https://github.com/gohugo-ananke/ananke):

![screenshot of the front page of this blog](/images/base-ananke.png)

Now, this isn't actually Ananke's fault at all. They don't intend for you to use their base theme, that would be pretty silly. Instead, they expect you to use their theme as a base, and have you do the rest. We can choose to do this, or we have a few other options:

1. Use one of many [Community Themes](https://themes.gohugo.io/themes/)
1. Create our own theme

For now, I just want this place looking fairly normal, and I'm not exactly the world's best CSS coder at the moment, so let's keep things simple and build off of Ananke.

# Wait, hang on - what do we want this place to look like?

That's a good question!

Not only am I not a great wielder of CSS, I'm *also* not what you'd call a graphic designer. I do think however I can come up with a decent plan of attack here.

I want a very aggressive amount of padding on each side of the viewport when in landscape mode, because I think that helps readability. For fonts, I'm a bit of a sucker for monpspace, but think that it can get a bit painful for body text, so I'll use it tastefully as decoration. Finally, I do enjoy breaking out of the flat design habit, so I'll try to give the page some depth somehow.

Here's a quick sketch of what I'm thinking:

![A sketch showing a website layout](/images/site mockup.png)
*You know how I said I'm not a graphic designer? Extend that sentiment to artist, too.*

As you can see, I want a big purple logo up top, a greyish background, slightly lighter highlighting and then use a variety of dark greys for the headings and body text.

According to the [Ananke Documentation](https://ananke-documentation.netlify.app/customisation/colours/#background-colour), it supports using [Tachyons](https://tachyons.io/docs/themes/skins/) utility classes, so I'll use those to get the desired effect. I might tweak things a bit after initial deployment.

Changes themselves are written to the `hugo.toml` file located in the project root. I've read a lot of very strict comments telling me **not** to update anything in `themes/ananke/config/_default`, as any Ananke updates will cause them to get overwritten.

Getting some of the basics down is easy - background colour, header colour, text colour and font family, for example. However, I very quickly run into some strange constraints with how Ananke has been built; namely:
1. I can't seem to move the logo from the top left to the top centre
1. Headings can't be assigned a different font family
1. I can't globally remove the default "hero text", and can only do it on a per-post basis

It seems like the first two can be resolved by writing some custom CSS, and the last one is fixed by setting up some index pages, but I'm already feeling a bit frustrated at the lack of customisability we can get out of the gate. 

Even reading the [Ananke Documentation](https://ananke-documentation.netlify.app/), which is itself an Ananke hugo site, shows that they've had to provide custom CSS to get half of the design they wanted out of their own instance.

I'd really prefer not to have to handle CSS at the moment. If it's an absolute requirement, I'll come back to it, but for now: let's check out the other community themes.



