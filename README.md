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
- ?[Poole](https://github.com/poole/poole) + [Lanyon](http://lanyon.getpoole.com/)
- some mobile-first (mobile-only?) css
- perhaps a cronjob to regenerate the homepage instead of isotope+company. with css variables perhaps it can be randomized in css and not via js.

Things which will make this better, offsite:
- ramnode $5/mo vps
- cloudflare OR cloudfront+s3 + s3cmd
- mod_pagespeed
- spdy/tls

### Still to research
what jekyll plugins does github pages support? (IE: can there be a stripped down version of this project which can be run entirely through github, with an acceptable level of compromise to the design constraints?)

is jQuery even feasible on mobile, due to how fucking gigantic it is? can a smaller version be built that gets rid of animations and things, while being significantly smaller? -> jQlite seems to answer this. How powerful it is, is another question. I'd rather avoid js anywhere other than the editing interface, if I can (and for that, prose will do).

analytics for journalists -> interviews for what qualifies as a good article

### Provisional front-end stack
- [LeafletJS](http://leafletjs.com/) or [OpenLayers](http://openlayers.org/)
- [Isotope](http://isotope.metafizzy.co/) or [Masonry.js](http://masonry.desandro.com/) or [Salvattore](http://salvattore.com/) or [FreeTile](http://yconst.com/web/freetile/)
- [ImagesLoaded](http://imagesloaded.desandro.com/)
- [Lato](https://www.google.com/fonts/specimen/Lato) or [Raleway](http://www.google.com/fonts/specimen/Raleway) 900 for titles, [Merriweather](http://www.google.com/fonts/specimen/Merriweather) for body. [Source Code Pro](https://www.google.com/fonts/specimen/Source+Code+Pro) for blockquotes. With money, use [skolar](https://www.rosettatype.com/Skolar)/[huronia](https://www.rosettatype.com/Huronia) for body, [Satyr](https://monokrom.no/fonts/satyr) for blockquotes, idk for titles maybe [Lumin Sans Thin](https://www.typotheque.com/site/fonts.php?id=79&tn=sample_text&style=1199&size=waterfall&regen=1) or something.


### Scratchpad
militant transparency without Real Names™
transparency without authority. authentication without authorization
collaborative news, at writing and editing level, with nyms not names
http://openrouteservice.org/
http://www.hotosm.org/
http://mapnik.org/
principle of least effort
principle of least authority
privacy: the capacity to continue personal information asymmetries
static pages as technological force multiplier due to global caching
ads = brand dilution.
must be able to run site on income of a coffee farmer
hmmhmm. public infrastructure is public whether the law reflects that or not. Usage patterns are defacto.
risk is energy, it cannot be created or destroyed only changed. 
conservation of mass, conservation of energy, laws of thermodynamics, all are the same thing.
you can transfer risk onto another party via contract, practice, or system, but it can never be created or destroyed. 
what principles guide this software? how is the world constructed?
https://versahq.com/
embedly
challenge: being leaked to

this is just a mirage, a collation. disregard. PR's welcome.

ideé: because this is designed to be loaded via 3g, pop a small js in that quicktests the navigationtiming1/2 PLT. If it's under a ceiling, ajax in extra functionality.

### spam (copy-pasted from notepad)
list: chartbeat (for total time reading and similar), gravity, outbrain, storify, versahq for news sites to deliver Featured Perspectives at 100-290 CPMv, 
licenses: ask author, CC selection. 
jekyll for output, something which can emit markdown for the writing interface. apache for writing interface, nginx/lighttpd for static html. 

so, use prose.io with a private github repo (25/mo for org), with jekyll-hook and a 5/mo digital ocean box for hosting. google apps for email.
ask joepie for recs around this. why can't I do this without github? can prose be deployed with no git backing? can I just use, say, cryto git hosting? could even take jekyll-hook and push to s3 with cloudfront in front. 
embedly, 
https://github.com/developmentseed/jekyll-hook, 
http://hallojs.org/demo/markdown/ ( https://github.com/bergie/hallo )
http://joshualande.com/jekyll-github-pages-poole/
https://github.com/kylepaulsen/Jekyll-Sort
https://github.com/developmentseed/jekyll-ga
http://jekyllrb.com/docs/plugins/
https://github.com/barryclark/jekyll-now
http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/
https://help.github.com/articles/using-jekyll-plugins-with-github-pages
https://github.com/chartbeat-labs
https://github.com/jarofghosts/peabody

http://aloha-editor.org/ http://wymeditor.github.io/wymeditor/
http://developmentseed.org/blog/all/
MOD PAGESPEED! AND CLOUDFLARE

jquery all over the homepage, which will be ranked popular/recent posts (no carousels. ever.), and things like http://isotope.metafizzy.co/ for dynamic views every time someone looks at it. 

TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256