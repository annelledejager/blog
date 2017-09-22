---
layout: post
title:  customize your jekyll blog
date:   2017-09-22 08:37:00
description: adding comments, analytics and customizing your theme
comments: true
---
#### Customizing your Jekyll theme's CSS

1. Create a file /css/style.scss 
2. Add the following content to the top of the file
3. Add custom CSS 

{% highlight ruby %}
---
---
@import "{{ site.theme }}";
{% endhighlight %}


#### Customizing your Jekyll theme's HTML layout

1. Create a file /_layouts/custom.html 
2. Customize the layout as you'd like
3. Change the layout the front matter to use the custom template

{% highlight ruby %}
---
layout: custom
title: blogging like a pro
---
{% endhighlight %}


#### Comments
I chose <a href="https://disqus.com/">Disqus</a> for adding commenting functionality to my blog. The integration was simple and quick to understand. 

1. Register on Disqus
2. Create a file _includes/disqus.html
3. Add the code provided by Disqus after registration
4. Modify the file _layouts/post.html to include `include disqus.html`


#### Analytics
1. Create an account through Google Analytics Admin
2. Google will provide a JavaScript tracking snippet". Add it to _includes/head.html so that it will be added to every page.
{% highlight ruby %}
<!-- Global Site Tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-106746652-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments)};
  gtag('js', new Date());

  gtag('config', 'UA-XXXXXXXXXXX);
</script>
{% endhighlight %}

#### References
<a href="https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/">Customizing CSS and HTML in your Jekyll theme</a>
<br /> 
<a href="http://romantsegelskyi.github.io/blog/2015/07/26/personal-page-blog/">Personal page and blog using Github pages and Jekyll</a>
