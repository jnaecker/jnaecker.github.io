---
layout: default
title: The Making Of
---

I started by reading the documentation on Jekyll: http://jekyllrb.com/docs/home/ and build a very basic site by following along there.

I created this site using [Jekyll](http://jekyllrb.com/) with help from [Poole](https://github.com/poole/poole).  I followed [this nice tutorial](http://joshualande.com/jekyll-github-pages-poole/) by [Joshua Lande](http://joshualande.com/).

Hosting by Github pages: https://help.github.com/articles/what-are-github-pages

DNS by Namecheap: https://www.namecheap.com/

Directions on setting up your custom domain with Github pages: http://davidensinger.com/2013/03/setting-the-dns-for-github-pages-on-namecheap/

Added MathJax support with 

```
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js"></script>
```

Customized MathJax with 

```js
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

Both of these went in `_includes/head.html `

Favicon from here: http://www.softicons.com/web-icons/alphabet-icons-by-supratim-nayak/j-orange-icon
