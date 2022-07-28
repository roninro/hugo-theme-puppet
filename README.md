# Hugo Theme Puppet

> Ported Theme of [Hux Blog](https://github.com/Huxpro/huxpro.github.io), Thank [Huxpro](https://github.com/Huxpro) for designing such a flawless theme.

## Installation

```bash
$ git clone https://github.com/roninro/hugo-theme-puppet.git themes/puppet
```

## Configuration

Config.toml example

```toml
baseurl = "/"
title = "Puppet"
languageCode = "en-us"
paginate = 10 # Number of posts per page
theme = "puppet"

disqusShortname = "" # Enable Disqus comments by entering your Disqus shortname

enableInlineShortcodes = true
enableEmoji = true


[outputs]
home = ["HTML", "JSON"]

[taxonomies]
category = "categories"
tag = "tags"
series = "series" #

[markup]
[markup.highlight]
codeFences = true
guessSyntax = true
lineNos = true
lineNumbersInTable = false
style = "dracula"

[markup.goldmark.renderer]
unsafe = true

[menu]
[[menu.main]]
identifier = "home"
name = "Home"
url = "/"
weight = -100
[[menu.main]]
identifier = "about"
name = "About"
url = "/about/"
weight = 100
[[menu.main]]
identifier = "archive"
name = "Archive"
url = "/archive/"
weight = 10


[params]
author = "Puppet"
description = "A simple and clean theme for Hugo"
keywords = "blog,developer,personal"
img_home = "/img/home-bg.jpg"
img_404 = "/img/404-bg.jpg"

[params.sidebar]
enable = true
avatar = "/img/home-bg.jpg"
bio = "John Doe's personal website"

[params.social]
rss_enable = true
twitter = "johndoe"
facebook = "johndoe"
zhihu = "johndoe"
weibo = "johndoe"
github = "johndoe"
linkedin = "johndoe"

[[params.friends]]
name = "John Doe"
url = "https://gohugo.io"

[[params.friends]]
name = "John Doe"
url = "https://gohugo.io"

# See https://giscus.app/
[params.giscus]
enable = false
repo = ""
repo_id = ""
category = ""
category_id = ""
input_position = ""
theme = "light"
```

## Front Matter example

see [default.md](archetypes/default.md)

```markdown
+++
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
header_img: ""
short: false
toc = true
tags = []
categories = []
+++
```

## License

[MIT](LICENSE)