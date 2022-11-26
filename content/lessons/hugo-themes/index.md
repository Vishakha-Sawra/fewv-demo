---
title: How to use hugo themes and build our website.
lastmod: 2022-11-21T08:11:12-07:00
publishdate: 2022-11-21T08:11:12-07:00
author: Vishakha Sawra
draft: false
pro: true
description: Using hugo themes to build our own website/blog.
tags:
  - hugo

youtube: XP_ikf4Jh18
---

## >> How To Use [Hugo Themes](https://themes.gohugo.io/)?

1. Go to [themes.gohugo.io](https://themes.gohugo.io/)

2. Select the theme of your prefered choice.

3. Go in their demo site and look for the documentation and follow it for building your website.

---

## >> Using [FixIt theme](https://themes.gohugo.io/themes/fixit/)

1. Open [Fixit demo](https://fixit.lruihao.cn/).
2. In docs link, click basic and go through the documentation.

---

## >> To build new Hugo site

1. To build new Hugo site in your system, run the command in command prompt or vs code terminal

```
hugo new site your_site_name
```

The above line will create your hugo website in

```
local disc C: > User
```

2. Now go in directory of your website folder with

```
cd your_site_name
```

3. After, all these steps are done clone your choosen hugo theme in themes folder of your website folder, in my case this link is provided in FixIt documentation.

```
git clone https://github.com/hugo-fixit/FixIt.git themes/FixIt
```

4. This will clone your choosen theme in **themes** folder of your website folder.

---

## >> Mention theme name in config.toml file

1. **Don't forget this step** it's the most important.

2. Type this code in config file.

```
theme = 'YOUR_CHOOSEN_THEME_NAME'
```

3. In my case it's

```
theme = 'FixIt'
```

4. If this is forgotten, hugo site will throw you any **Page Not Found Error**.

---

## >> Create first post

1. To create first post run the command.

```
hugo new posts/first_post.md
```

2. This will create your first_post.md file in content folder of website.

3. By default our post is set to **draft: true** so make that **draft: false** in your **first_post.md** file.

---

## >> To make changes in title. avatar, social links

To make changes in your website use **config.toml file**, every thing needed to be changed is in config.toml file.

---
