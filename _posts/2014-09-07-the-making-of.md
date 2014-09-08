---
layout: post
title: The Making Of
---

When I set out to make this site, I was interested in a minimal structure that used tools I was already familiar with.  I settled on [Jekyll](http://jekyllrb.com/), because I could write pages and posts in [Markdown](http://daringfireball.net/projects/markdown/) and use [Github](https://github.com/) for hosting.

I started by building a very basic site following the [documentation](http://jekyllrb.com/docs/home/) on Jekyll.  However, I soon found [this tutorial](http://joshualande.com/jekyll-github-pages-poole/) from Joshua Lande, and found it incredibly helpful.  It walked me through setting up the site with [Poole](https://github.com/poole/poole), a very clean and beautiful fork of Jekyll.  I recommend this tutorial to anyone looking to build a similar site to mine.  Below I've noted a couple small details to supplement Josh's extensive walkthrough.

#### MathJax support

[MathJax](http://www.mathjax.org/) is a Javascript library that allows for live rendering of LaTeX-like equations.  I wanted this feature to be able to include nicely formatted equations in my posts, like this: 

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(x)}{n!} x^n.$$ 

To add MathJax support, I put the following in `_includes/head.html `:

```html
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js"></script>
<script>
MathJax.Hub.Config({
            config: ["MMLorHTML.js"],
            extensions: ["tex2jax.js","TeX/AMSmath.js","TeX/AMSsymbols.js"],
            jax: ["input/TeX"],
            tex2jax: {
                inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                processEscapes: false
            },
            TeX: {
                TagSide: "right",
                TagIndent: ".8em",
                MultLineWidth: "85%",
                equationNumbers: {
                   autoNumber: "AMS",
                },
                unicode: {
                   fonts: "STIXGeneral,'Arial Unicode MS'" 
                }
            },
            showProcessingMessages: false
        });
</script>
```

The configuration script is not necessary, but it make the typesetting a little prettier, and allows me to typeset inline equations (ike this one: $y = f(x) + z_0$) by surrounding the LaTeX code with single dollar signs.

#### Domain name hosting

Perhaps the single best feature of Jekyll is that you can host your site for free on [Github pages](https://help.github.com/articles/what-are-github-pages).  So, my site is hosted on Github at [jnaecker.github.io](http://jnaecker.github.io), simply by virtue of having my site's repository pushed to Github.  I got the domain name [jeffnaecker.com](http://jeffnaecker.com) from [Namecheap](https://www.namecheap.com/).  Here are directions on [setting up your custom domain with Github pages](http://davidensinger.com/2013/03/setting-the-dns-for-github-pages-on-namecheap/).

#### Permalinks

You might notice that the url of this page is [jeffnaecker.com/blog/the-making-of](http://jeffnaecker.com/blog/the-making-of), not [jeffnaecker.com/blog/2014/09/07/the-making-of](http://jeffnaecker.com/blog/2014/09/07/the-making-of).  To get the simpler URL, I set the `permalink` entry in `_config.yml` to `/blog/:title`.  For more details, see the comments on [Josh's post on this issue](http://joshualande.com/short-urls-jekyll/).
