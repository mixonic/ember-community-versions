Web content never expires. A blog post written in 2011 will live on in search
engine results for years.

[Ember.js](http://emberjs.com/), the JavaScript framework for ambitious apps, has already been
around for several years. This means the Internet is littered with content
and posts that were accurate at the time, but have since been obsoleted.

To ensure old content gets properly flagged, with no effort needed by the
author, we've created a GitHub-driven badge service. See
[the user-friendly website](http://mixonic.github.io/ember-community-versions/)
for more details on the general idea.

## Updating a badge

Badges are stored as Jekyll posts. For example, the badge for this blog post:

* "Previewing Ember 2.0 on Canary" [madhatted.com/2015/5/14/ember-js-2-0-preview-with-canary](http://madhatted.com/2015/5/14/ember-js-2-0-preview-with-canary)

Is stored at:

* [\_posts/2015-05-13-previewing-ember-2-0-on-canary.md](https://github.com/mixonic/ember-community-versions/blob/gh-pages/_posts/2015-05-13-previewing-ember-2-0-on-canary.md)

Versioning informations is store in the YAML front-matter of that post:

```
---
layout: post
url: http://madhatted.com/2015/5/14/ember-js-2-0-preview-with-canary
title: "Previewing Ember 2.0 on Canary"
date: 2015-05-13
start_version: 1.13
end_version: 2.0 # end_version is optional
---
```

To update the badge (as seen the blog post at madhatted.com), open a PR changing
the YAML front-matter.

## Creating a badge

To create and embed a badge, first author a Jekyll post with the version
information as exists. Most badges are likely to be for current content, and
thus may only have a `start_version` property.

To embed your badge, use the filename to determine the badge URL. For example
this filename:

```
_posts/2015-05-13-previewing-ember-2-0-on-canary.md
```

Is used as a badge with the following markup:

```html
<iframe
  width="178" height="24" style="border:0px"
  src="http://mixonic.github.io/ember-community-versions/2015/05/13/previewing-ember-2-0-on-canary.html">
</iframe>
```

Please help ensure your own blog posts are correctly flagged by add a badge
when you publish.

Linking to a URL that does not exist, such as before your
PR with the new badge is merged, will simply result in a blank space. As
soon as the PR is merged and GitHub pages updates, the badge will appear.
