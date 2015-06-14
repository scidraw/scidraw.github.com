---
layout: post
title: "Install biodalliance genome browser debian"
description: "tutorial for biodalliance install and data preparation"
tagline: by Luye & zhoujj
category: draw
tags: [bioinformtics]
---
{% include JB/setup %}

[Dalliance](https://github.com/dasmoth/dalliance) is a genome viewing tool that aims to offer a high level of interactivity while working entirely within your web browser. It works with current versions of Chrome, Firefox, and Safari and (with minor visual glitches) Internet Explorer 11. It is also usable with current mobile web browsers. As mention in my previous post, researcher need a good genome browser for visualization and prepare figures for publication.

<!--more-->

## Install dependencies,[Node.js](http://nodejs.org/), [Gulp](http://gulpjs.com/), which is needed for the NPM package manager.

{% highlight bash %}

[user]$ sudo apt-get install build-essential

[user]$ apt-get install libbz2-1.0 libbz2-dev bzip2

[user]$ tar zxvf Python-2.7.2.tgz
[user]$ cd Python-2.7.2/
[user]$ make
[user]$ make install

# install node.js
[user]$ tar zxvf node-vX.XX.XX.tar.gz
[user]$ cd node-vX.XX.XX/
[user]$ ./configure
[user]$ make

# install gulp
[user]$ sudo npm install -g gulp
[user]$ npm install # Install dependencies
[user]$ gulp        # Build Dalliance

{% highlight end %}

if ./build dir have been created without error, we have successfully install Dalliance genome browser.

## Test Dalliance

http://YourServerIP/dalliance/example-browsers/human37.html

if you can see the genome browser view like the one showed in [biodalliance](http://www.biodalliance.org/index.html). You can create a browser for your project by amending the code in human37.html. But the genome you interested show have a public data support, like DAS, UCSC, Ensembl, EBI or other data server.


## Create a local assembly track hub

Dalliance support UCSC assembly track hub, so we can create a track hub for a specific genome.

Regarding to UCSC assembly track hub, you can referring to [UCSC assembly track hub guideline](http://genome.ucsc.edu/goldenPath/help/hgTrackHubHelp.html).

Regarding to different for used in data resource, you can referring to [https://genome.ucsc.edu/FAQ/FAQformat.html#format1].

## Apply and share your assembly track hub

For source data configuration, you should read [Dalliance configuring](http://www.biodalliance.org/config.html) and [source configuring](http://www.biodalliance.org/config-source.html).

For data sharing, you should try to learn how to import a hub assembly in Dalliance genome browser.


## Create a good look for Dalliance genome browser

For the web front design, you can referring to [bootstrap](http://getbootstrap.com/getting-started/).


