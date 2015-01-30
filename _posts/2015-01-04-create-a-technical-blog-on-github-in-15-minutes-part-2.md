---
published: true
layout: post
---

I've tried several ways of creating a Jekyll blog, but the fastest way is to just clone someone else's blog.  That way you get all the configurations and a good examples to start with.  I've never found a blog which fulfills my desire to have a good code highlighter and one which uses Bootstrap and SASS.  If this is what you desire also, you can clone my repository, else you can use this method on anyone else's GitHub hosted blog.

###Step 1) Fork my blog's repository to your own GitHub User repository

- Fork [bengwall.github.io](https://github.com/bengwall/bengwall.github.io) to new repository named with your own GitHub name `YourGitHubName.github.io`  such as `johnjones.github.io`.

###Step 2) Customize and view your site

Set your name, description and github repository name in the `_config.yml` file.  Other optional configurations are later in this post.

- `name: Brent Engwall`
- `description: Web App Designer/Architect/Developer`
- `github: bengwall/bengwall.github.io`

Making changes to `_config.yml` will trigger a rebuild of your blog on GitHub at http://YourGitHubName.github.io.  This make take a few seconds to a many seconds before you will see your changes. 

> There are 2 ways to edit your blog:
> 
1.	Edit your files directly on GitHub.  This is certainly the fastest way to get your blog up and running and will be easier if you are not using a Mac.  TIP:  You can use [prose.io](http://prose.io) to create the posts and do quick edits.  Also, you can initially create the posts in the `_drafts` folder until I'm ready to publish.
2.	Setup Jekyll locally, `git clone` your blog repository, and make changes and test locally.  I would recommend this method if you are on a Mac and are comfortable with GIT.  Having the build process run locally is faster than having it on GitHub.  I will detail later in this post.

### Step 3) Create your first post

Look in the `_posts` directory to see the posts for my blog.  Open one post to see how it is structured and how the [front-matter](http://jekyllrb.com/docs/frontmatter/) header is constructed.  


### Setup Jekyll locally

The instructions below are setting up your blog environment locally.  For Windows, this will be slightly different.

1) Open Terminal and install Jekyll:  `$ gem install jekyll`
>You may need to use `sudo gem install` for permissions

2) Navigate to your Documents directory.  Create a directory called `gitrepos`.  Clone your new repository:
```
$ git clone https://github.com/YourGitHubName/YourGitHubName.github.io.git
```

3) Navigate `$ cd YourGitHubName.github.io.git` directory.
4) Serve up the site: `$ jekyll serve`.  (Jekyll will watch for any markup or sass changes and automatically rebuild the blog site.)
5) View your blog at http://0.0.0.0:4000.
6) Commit your changes and push them back up to GitHub.


### Optional Blog Configurations

#### Setup Disqus comments (Optional)

- Signup for a [Discus](www.disquc.io) account.

**_config.yml**

- Add the disqus name.  I called mine `bengwall`
	`disqus: 'bengwall'`

#### Setup Google Analytics

- Signup for a [Google Analytics](http://www.google.com/analytics/) account.
- Create a 'property' and call it `Brent Engwall Blog`
- You will receive a tracking id like 'UA-12341234-1'

**_config.yml**

- Add that tracking id:
	`google_analytics: UA-12341234-1`

#### Use a real domain name

I wanted the blog to have my domain name  `www.brentengwall.com` instead `bengwall.github.io`.

**Modify the Domain Registrar**

- Created `CNAME` to `bengwall.github.io`

**Modify the CNAME file**

- added `www.brentengwall.com`


### Additional Tips
- Sometimes I'll create the markdown in [stackedit.io](www.stackedit.io) because to be able to see the preview is so powerful.

###Credits
- (Getting Started with GitHub Pages)[http://24ways.org/2013/get-started-with-github-pages/] - By Anna Debenham
- (Jekyll GitHub Pages Poole)[http://joshualande.com/jekyll-github-pages-poole/] - By Joshua Lande
- (Blogging on GitHub)[http://loyc.net/2014/blogging-on-github.html]
- (Setting up Jekyll with Bootstrap, SASS, and Pygments)[http://kvurd.com/blog/my-jekyll-blog-setup-bootstrap-sass-pygments/] - by Karl Urdevics
- (Jekyll Now)[https://github.com/barryclark/jekyll-now] - By Barry Clark

