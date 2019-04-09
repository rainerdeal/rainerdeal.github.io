---
# Predefined Globals
layout: post                            # layout for this post
permalink: /:categories/:title          # overrides the default URL
published: true                         # flag to publish post

# Custom Vars
image: null                             # Hero image to display at top of post ex: /path/to/image
youtube: https://www.youtube.com/embed/Q34dZ6VmI04  # embed URL
spotify: spotify:track:6TGGxrlz1okTBbrHZugkBI       # URI
soundcloud: https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/188383713&color=%23ff5500 # embed URL
excerpt: false                          # flag for post excerpt displayed on index.html
spoiler: false                          # flag for spoiler warning on index.html
explicit: false                         # flag for explicit content warning on index.html

# Predefined Vars
date: 1993-01-26                        # publish date
categories: [these, are, categories]    # overrides path/URL (order matters)
tags: [these, are, tags]                # used for finding related content (order doesn't matter)

# note: Defaults are defined in _config.yml
---

#### Markdown Cheat Sheet
- [Markdown Documentation](https://daringfireball.net/projects/markdown/syntax) by John Gruber
- [GHF Markdown Guide](https://guides.github.com/features/mastering-markdown/)

#### Pictures
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

#### Code Snippets
    if (isAwesome) {
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

```
if (isAwesome) {
  return true
}
```

And if you'd like to use syntax highlighting, include the language:

```javascript
if (isAwesome) {
  return true
}
```

#### Footnotes
- prolefeed[^1]
- anarcho-socialist[^2]

#### Quotes
> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

[^1]: [Prolefeed](https://en.wikipedia.org/wiki/Prolefeed) is an Orwellian term that describes media designed to distract the masses.
[^2]: [Anarcho-socialism](https://en.wikipedia.org/wiki/Social_anarchism)