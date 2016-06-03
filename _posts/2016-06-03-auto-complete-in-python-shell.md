---
layout: post
title: "auto complete in python shell"
description: "auto complete in python shell"
tagline: by Luye & zhoujj
category: python
tags: [python linux]
---
{% include JB/setup %}

Create a file .pythonrc for all python shell.

<!--more-->

I may have found a way to do it.

Create a file .pythonrc

{% highlight bash %}
# ~/.pythonrc
# enable syntax completion
try:
    import readline
except ImportError:
    print("Module readline not available.")
else:
    import rlcompleter
    readline.parse_and_bind("tab: complete")
{% endhighlight %}

then in your .bashrc file, add

{% highlight bash %}
export PYTHONSTARTUP=~/.pythonrc
{% endhighlight%}

That seems to work.

{% highlight bash %}
import readline
readline.write_history_file('/path/to/where/I/want/to/save/history.txt')
{% endhighlight%}


