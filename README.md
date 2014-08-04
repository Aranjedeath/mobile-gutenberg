mobile-gutenberg
================

It's my intent to create a guide, and glue-code where necessary, for a news site which is collaboratively written and edited. This is the repository for such.

### Intentional Design Constraints
Site is to be optimized for phone access via 3g (not 3.5g). Writing, editing, and all the rest, should all be possible on a smartphone. Any page load optimizations which can be made at generation-time, should be made. Every KiB counts on an unstable/slow connection. TLS is mandatory (you don't hate your users, writers, contributors, or editors, do you?). Ads are not allowed. 

### Prerequisites
- Github account
- [Prose](http://prose.io/) / [hallo](http://hallojs.org/) + ???
- [jekyll](https://github.com/jekyll/jekyll)
- [jekyll-hook](https://github.com/developmentseed/jekyll-hook)
- [jekyll-sort](https://github.com/kylepaulsen/Jekyll-Sort)
- [jekyll-ga](https://github.com/developmentseed/jekyll-ga) or similar
- [jekyll-filename](https://github.com/developmentseed/jekyll-filename)
- [jQuery](http://jquery.com/) / [jQlite](https://code.google.com/p/jqlite/)
- [Isotope](http://isotope.metafizzy.co/)
- some mobile-first (mobile-only?) css
- perhaps a cronjob to regenerate the homepage instead of isotope+company. with css variables perhaps it can be randomized in css and not via js.

Things which will make this better, offsite:
- ramnode $5/mo vps
- cloudflare OR cloudfront+s3 + s3cmd
- mod_pagespeed
- spdy/tls

### Still to research
what jekyll plugins does github pages support? (IE: can there be a stripped down version of this project which can be run entirely through github, with an acceptable level of compromise to the design constraints?)

is jQuery even feasible on mobile, due to how fucking gigantic it is? can a smaller version be built that gets rid of animations and things, while being significantly smaller?






