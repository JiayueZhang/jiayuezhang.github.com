---
layout: post
title:  "How to add comments in Jekyll"
date:   2017-09-25 18:05:45 -0400
categories: jekyll update
tags: Jekyll
comments: true
---

Since all the fancy blogs have comment function, why not take a shot? A simple way to implement it is to use [Disqus][disqus].

## 1
Sign up a Disqus account and choose "I want to install Disqus on my site". Then fill out the form and select a plan. I chose the commericial-free plan and the Jekyll platfrom.
## 2
Add `"comments: true"` to your YAML Front Matter.
{% highlight ruby %}
layout: post
title:  "How to add comments in Jekyll"
date:   2017-09-25 18:05:45 -0400
categories: jekyll update
tags: Jekyll
comments: true
{% endhighlight %}
## 3
Insert a ｛% if page.comments %｝and a｛% endif %｝tag in your post. And in between them, copy and paste the Universal Embed Code.

{% highlight ruby %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://https-jiayuezhang-github-io.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endhighlight %}

Then you will have your own comment system with Diqus.

[disqus]:https://disqus.com/



{% if page.comments %} 
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://https-jiayuezhang-github-io.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}