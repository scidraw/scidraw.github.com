---
layout: post
title: "Add ssh key to github"
description: "Add ssh key to github"
category: github
tags: [github, linux]
---
{% include JB/setup %}

Add ssh key to github.

<!--more-->

## Generating ssh keys for github

https://help.github.com/articles/generating-ssh-keys/


## Push your code to a new repository

I want to push README.md to Github.
So, I commit in the following steps.

{% highlight bash %}
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/user/repo.git
git push -u origin master
{% endhighlight %}

But, below error occurred.

{% highlight bash %}
error: The requested URL returned error: 403 Forbidden while accessing https://github.com/user/repo.git/info/refs

fatal: HTTP request failed
{% endhighlight %}

This error can be solve in this way:

{% highlight bash %}
git remote set-url origin https://username@github.com/user/repo.git
git push origin master
Password: 
{% endhighlight %}

But I don't know how to push without password.

