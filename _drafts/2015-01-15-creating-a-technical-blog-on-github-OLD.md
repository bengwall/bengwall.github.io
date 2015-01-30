---
published: false
layout: post
title: Create a Technical Blog on GitHub in 15 minutes- Part 2
---

## Setup

### Step 1) Create the repo

- Fork [Jekyll Now](https://github.com/barryclark/jekyll-now) to new repository called `bengwall.github.io`
- Your site should not be immediately available at http://bengwall.github.io.


### Step 2) Customize and view your site

#### _config.yml

- `name: Brent Engwall`
- `description: Web App Designer/Architect/Developer`
- `github: bengwall/bengwall.github.io`
- `markdown: redcarpet`  (This enables code highlighting more compatible with Markdown.)


#### _scss/_highlights.scss

- added `overflow:auto`

```
.highlight pre {
  overflow: auto;
  /* overflow: scroll; Prefer no word wrap? Uncomment this line and comment out the 2 lines below. */
  //word-break: break-all;
  //word-wrap: break-word;
}
```

- changed a few colors

`.highlight .c1 { color: #009966 } // Brent - from #586E75`
`.highlight .nx { color: #666 } // Brent - from 555`


### Step 3) Setup Disqus comments (Optional)

- Signup for a [Discus](www.disquc.io) account.

#### _config.yml

- Add the disqus name
	`disqus: 'bengwall'`


### Step 3) Setup Google Analytics (Optional)

- Signup for a [Google Analytics](http://www.google.com/analytics/) account.
- Create a 'property' and call it`Brent Engwall Blog`
- You will receive a tracking id like 'UA-12341234-1'

#### _config.yml

- Add that tracking id:
	`google_analytics: UA-12341234-1`


### Step 4)  Use a real domain name (Optional)

I wanted the blog to have my domain name  `www.brentengwall.com` instead `bengwall.github.io`.

#### Modify the Domain Registrar

- Created `CNAME` to `bengwall.github.io`

#### Modify the CNAME file

- added `www.brentengwall.com`



## Tips

- I use [prose.io](http://prose.io) to create the posts and do quick edits.  I initally create the posts in the _drafts folder until I'm ready to publish.
- Sometimes I'll paste the markdown in [stackedit.io](www.stackedit.io) because the preview is much better than prose.


## Credits

- [Jekyll Now](http://www.jekyllnow.com/)
