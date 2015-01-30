---
published: true
layout: post
---

In starting my blog, I've been researching a lot around how to best create a technical blog.  My first few blog posts will cover what I'm seeing as a worthy tools and workflows.

One of the items I'm come across is Markdown.  I first learned of Markdown years ago, but now am revisiting it for blogging.

### Pros of Markdown
* It is widely accepted.  Many guides, editors, and converters exist.
* It easy to use.
* It looks nice.  In my opinion, it creates nice looking, consistent technical documentation.  Much better than I could do on my own.
* It is becoming more and more popular

### Cons of Markdown
* I could not find enterprise tools which are adapting to used it.  SharePoint and Word do not support Markdown.
* Tools still seem to immature.


##Online Tools

I really wanted to find a nice workflow to use Markdown to create this blog and create technical documentation.  I wanted to get started quickly and without installing software.  Below are my findings:

###[markable.in](http://markable.in)
* **Editing:**      Best editor.  Colorized, easy to read.  Editing produces flashes when the review pane updates.
* **Previewing:**   Best preview style.  Scrolling the review pane does not scroll the editor.
* **Exporting:**    Worst exporting.  No built in support to export to pdf (To print to PDF you can View -> Single Page Preview -> Print -> Print to PDF)
* **Integrating:**  Worst integration.  No Google Drive, but Dropbox
* **Other:**        I like the fact that you can have an account to save your docs

###[dillinger.io](http://dillinger.io)
* **Editing:**      Best editor.  Colorized, easy to read.  Very fast reflection on the review pane.
* **Previewing:**   Worst preview style.  Scrolling the review pane does not scroll the editor.
* **Exporting:**    Worst Export.  Exports to PDF, but ugly.
* **Integrating:**  OK Integration.  Github, Dropbox & Google drive integration

###[stackedit.io](http://stackedit.io)
* **Editing:**      Worst Editor.  Hard to read the editor (no colorizing), but scrolling the preview pane does scroll the editor.
* **Previewing:**   Good preview.  I do not like the preview style as much as Markable, but it really does not matter that much becuase I find the editor difficult to see.  It is nice that scrolling the preview pane will scroll the editor pane.
* **Exporting:**    Best Exporting.  Exports to pdf correctly.
* **Integrating:**  Best Integration.  Dropbox & Google drive synchronization.


> **Note:** I liked the **Markable** preview style better than the **Stackedit** style.  You can improve the export to PDF by using the Markable css.  Go to the settings and use these files in the template.
```HTML
//Remove this line:   
<link rel="stylesheet" href="https://stackedit.io/res-min/themes/base.css" />

//Add these lines:    
<link rel="stylesheet" href="http://markable.in/site_media/static/bootstrap/css/bootstrap.min.css">
<link rel="stylesheet" type="text/css" href="http://markable.in/site_media/static/editor/css/view_file.css">
```

##Decision Time
Well, there is not one perfect solutions for me.  I'm going to try using the **Markable** editor (which is the best editor and has the best preview style).  Once I have it edited I'm going to store it in **Stackedit** where I like the integration and export features.  In the end, I wish **Stackedit** had a colorized editor.  That would make it the perfect solution in my opinion.

##Markdown Help
* [Markable's style guide](http://markable.in/file/aa191728-9dc7-11e1-91c7-984be164924a)
* [David Loeffler's style guide](http://ddloeffler.blogspot.com/2013/04/how-i-use-markdown-for-posting-to.html)

> Side Note: I did not see many installed tools that I would be interested in.  One I did see was [Moo](http://mouapp.com/).  When I get a Mac I'll check it out.