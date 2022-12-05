+++
title = "Puppet - Getting Started (hugo module)"
date = 2022-12-05T21:24:01+01:00
description = "Set up your new hugo site with theme puppet theme as hugo module"
header_img = ""
toc = true
tags = ["documentation", "guide"]
categories = []
series = []
+++

Puppet is a responsive, simple and clean [Hugo](https://gohugo.io/) theme based on the [Huxblog Jekyll theme](https://github.com/Huxpro/huxpro.github.io). 

<!--more-->

## Install Hugo

Make sure you have installed the latest version of [Hugo-extented](https://gohugo.io/getting-started/installing/).

## Create a New Site

```
hugo new site mysite
```

## Import the Puppet theme module as a dependency of your site

To turn your site into a Hugo Module and declare the puppet theme module as a dependency for your site.

```bash
cd mysite
hugo github.com/me/mysite
hugo mod get github.com/roninro/hugo-theme-puppet
```

Puppet is now declared and ready to be used.

### Add Config File

For getting started, you can copy the `config.toml` file from the theme's exampleSite directory to the root directory of your site.

```bash
cp themes/puppet/exampleSite/config.toml .
```

### Declare theme

Identify these two lines inside the file `config.toml` you just copied.

```toml
# using theme as hugo module (modern)
# theme = "github.com/roninro/hugo-theme-puppet"
```

Uncomment the trailing hash sign from the second line of the snippet so that theme declaration takes effect. 

Comment out or remove these lines inside the config file:

```toml
# using theme as git clone or submodule (traditional)
theme = "puppet"
themesDir = "../.."
```

## Add Some Content

Create a new post with the following command.

```bash
hugo new posts/my-first-post.md
```

Edit the content of the post.

```markdown
+++
title = "{{ replace .Name "-" " " | title }}"
date = {{ .Date }}
description = ""
draft = true
subtitle = ""
header_img = ""
toc = true
tags = []
categories = []
series = []
comment = true
+++

Your content here...
```

Some front-matter used for SEO, others used for displaying contents, configuration, etc.

## Serve your new site

From the root of your newly created site:

```bash
hugo server
```

Hugo now downloads the theme directly from GitHub and serves the contents of your new site.
