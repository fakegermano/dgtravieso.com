---
title: "Creating This Site"
date: 2021-08-11T21:24:46-03:00
draft: true
toc: false
images:
tags: 
  - untagged
---

Hello folks. This will be the first post on this website, and as it is, it will follow my process of building this site with [hugo](https://gohugo.io). Hugo is a pretty cool tool to allow you to build and manage static sites in a _dynamic_ way. To start, I installed the hugo binary in may system following the official documentation.

Next, it was time to start a new hugo site. You can do this with the command `hugo new site <site-name>`, in my case I ran:

```shell
$ hugo new site dgtravieso.com
```

This will create the directory structure for the new hugo site. It contains some files but for now we won't touch on them. First we need to choose a theme. I could build a new theme from scratch using `layouts` and `partials` but in the spirit of not wasting too much of my time, I chose a simple but effective theme to host this site. The theme is named [hermit](https://github.com/Track3/hermit) and is licensed under a [MIT](https://github.com/Track3/hermit/blob/master/LICENSE), so I'm free to use it in any way, given that I propperly credit it's author (as the theme does automatically in the footer of the page).

To install the theme, I used git (as I already had it installed in my machine) and ran the following code:

```shell
$ git clone https://github.com/Track3/hermit.git themes/hermit
```

Then, I copied the `config.toml` from the `themes/hermit/exampleSite` folder, and edited it, changing the values I found necessary for my case. When I was finished, I needed to generate the _about_ and this _post_ pages, this was done using the `hugo new` command. Please note that you need to change in the `config.toml` file the location/url for the about page.

```shell
$ hugo new about.md
$ hugo new posts/creating-this-site.md
```

Then I copied the files from the `themes/hermit/assets/scss` directory to the directory `assets/scss` so I can customize the theme. I based this theme's colors from the [zenburn](https://kippura.org/zenburnpage/) theme, which ~~funny story~~ I found out **today** that uses the same theme I am using right now, but doesn't customize its colors.

I then had to customize the `index.html` layout to include copyright attribution information to the home page.