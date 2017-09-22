---
layout: post
title:  jekyll setup
date:   2017-09-21 09:02:00
description: my quick start guide
comments: true
---
There are plenty of articles out there to create a blog using Jekyll. Here are the high-level steps I took to create mine. The easiest way to get a great looking blog is to use Github Jekyll themes. There are quite a few to choose from <a href="https://github.com/jekyll/jekyll/wiki/themes">here</a>. These themes are also easy to customize later. 

Please refer to <a href="https://annelledejager.github.io/blog/2017/09/20/whyjekyll.html"><b>why I chose jekyll</b> post</a> for an intro to Jekyll and why I chose it.

1. Choose a Github Jekyll theme, I chose https://github.com/bogoli/-folio/
2. Create a user account on Github if you don't already have one
3. Create a new repository called for example blog
4. Create a new branch in your blog repository called `gh-pages`

<blockquote>
	GitHub Pages is a static site hosting service.
		—<a href="https://help.github.com/articles/what-is-github-pages/">Github pages</a> 
</blockquote>

5. Remove the `master` branch, you will be commiting to the `gh-pages` branch from now on
6. Download your selected theme to local from Github
7. Get familiar with the theme, the directory structure and how you can customize it. Please see below.
8. Add the theme to your repository branch `gh-pages`
9. Go to your blog repository settings to find your blog url. You have to be the main contributor to see the `settings`. The url will look something like {username}.github.io/blog/

#### Running Jekyll locally
1. Install Jekyll `$ gem install jekyll`
2. Go to the Jekyll repository on your local machine `$ cd blog/`
3. Run `$ Jekyll serve`
3. http://127.0.0.1:4000/ in browser 

Jekyll provides a variety of options <a href="http://jekyllrb.com/docs/usage/">here</a>.

#### File structure

<ul>
	<li>_config.yml - important file where the configuration data live</li>
	<li>_site - this folder is generated, don't commit it and don't change it, because any changes will be overwritten</li>
	<li>_includes - partials that can be added to your posts for example</li>
	<li>_layouts - describes how your posts should look</li>
	<li>_posts - a folder containing your posts in the format YEAR-MONTH-DAY-title.MARKUP</li>
</ul>

Jekyll will transform any .html, .markdown or .md files.

#### A frew tricky things
- If your css looks originally looks a bit weird, change the baseurl in config the file.
- Add your favicon link to the header.  If your favicon does not want to appear, refresh your browser cache. 
```<!-- {{ site.title }} instead of blog -->
<a class="page-link" href="{{ site.baseurl }}/">blog</a>```

Start blogging! 
