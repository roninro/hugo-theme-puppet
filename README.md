# Hugo Theme Puppet

[![Netlify Status](https://api.netlify.com/api/v1/badges/275ce227-7872-4314-8b54-5499ba237c18/deploy-status)](https://app.netlify.com/sites/hugo-theme-puppet/deploys)

> Ported Theme of [Hux Blog](https://github.com/Huxpro/huxpro.github.io), Thank [Huxpro](https://github.com/Huxpro) for designing such a flawless theme.

[Demo](https://hugo-theme-puppet.netlify.app/)

## Installation

```bash
$ git clone https://github.com/roninro/hugo-theme-puppet.git themes/puppet
```

## Configuration

Take a look inside the [exampleSite](exampleSite) folder of this theme. You'll find a file called [config.toml](exampleSite/config.toml). 
To use it, copy the [config.toml](exampleSite/config.toml) in the root directory of your website. Overwrite the existing config file if necessary.

## Content


### Archive Page

add `archive/_index.md` to your `content` folder. This file will be used as the archive page.

### About Page

like the archive page, add `about/_index.md` to your `content` folder.

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