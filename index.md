---
layout: page
title: Community Versioning for Ember Content
---

Web content never expires. A blog post written in 2011 will live on in search
engine results for years.

[Ember.js](http://emberjs.com/), the JavaScript framework for ambitious apps, has already been
around for several years. This means the Internet is littered with content
and posts that were accurate at the time, but have since been obsoleted.

To ensure old content gets properly flagged, with no effort needed by the
author, we've created a GitHub-driven badge service.

<iframe width="178px" height="20px" style="border:0px" src="/ember-community-versions/2015/05/13/previewing-ember-2-0-on-canary.html"></iframe>

Posts with this badge should work (without deprecation) when using an appropriate
version of Ember.

If you see an inaccurate badge, please help us by
[opening a pull request](https://github.com/mixonic/ember-community-versions)
to change the version number. All entries are made as blog post files for
Jekyll, and should include the URL of the original entry. For example:

{% highlight yaml %}
layout: post
url: http://madhatted.com/2015/5/14/ember-js-2-0-preview-with-canary
title: "Previewing Ember 2.0 on Canary"
date: 2015-05-13
start_version: 1.13
end_version: 2.0 # end_version is optional
{% endhighlight %}

Please help ensure your own blog posts are correctly flagged by add a badge
upon publication, even if you only provide a starting version. See
[mixonic/ember-community-versions](https://github.com/mixonic/ember-community-versions)
for more information.

