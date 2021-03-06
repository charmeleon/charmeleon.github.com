---
layout: post
title: "Jekyll Installed"
tagline: "And the world is better for it"
description: "Successful jekyll installation"
category: "miscellaneous"
tags: [miscellaneous, ruby, jekyll installation, rbenv, rvm]
---
{% include JB/setup %}
So after a very long day, Jekyll is finally up and running. I had tons of issues getting it to run properly on Ubuntu 12.04. The peskiest error was this:
{% highlight bash %}$ It seems your ruby installation is missing psych (for YAML output). To eliminate this warning, please install libyaml and reinstall your ruby. {% endhighlight %}
<p>Since I know nothing of Ruby, I went through a few tutorials trying to get this to work. I did what the warning asks - installed libyaml and then re-installed ruby, while making sure that the version that I had just installed was the one being used by the operating system. I did this at least twice but the warning wouldn't go away.</p>
<p>Something that I eventually noticed was that these tutorials asked me to install two entirely different things: rbenv and rvm. Both are virtual machines to manage multiple ruby environments (among other things, I suspect). Thus, if you are getting this warning in Ubuntu and it isn't going away, these are the steps I took:
<ol>
  <li>Uninstall rvm from the terminal (rm -rf ~/.rvm)</li>
  <li>Uninstall rbenv from the terminal (rm -rf ~/.rbenv)</li>
  <li>Uninstall any existing ruby installation. Make sure to clean up any leftover files</li>
  <li>After the aforementioned steps, follow the instructions detailed on <a href="http://www.stehem.net/2012/05/08/how-to-install-ruby-with-rbenv-on-ubuntu-12-04.html">this blog post</a>. When I reached the "Install Ruby" section, I personally changed it so that it would use the latest revision of ruby (1.9.3-p286 as of this writing)</li>
</ol>
Once this is properly setup, you should have no issue following the <a href="http://jekyllbootstrap.com/usage/jekyll-quick-start.html">Jekyll Quick Start</a> guide.</p>
