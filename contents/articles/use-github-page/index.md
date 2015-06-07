---
title: 用Github做静态网站服务器
author: lanfan
date: 2015-06-06 20:00
template: article.jade
tags: github, hexo
---

年初换了一台虚拟主机，但是没有把博客网站重新配置好。一拖又过了大半年时间。

近来想起应该分享一些想法，于是想起来要重新搭建一个博客站点。中途想试试新的静态网站生成工具。在 [StaticGen][0] 上看到一个列表，其中 [Hexo][1] 看起来是个比较流行的 JavaScript 静态网站生成工具。下午就试用了一下。

<span class="more"></span>

之后发现 Hexo 一个挺不符合使用习惯的地方：POST 的 md 源文件与内使用的图片资源组织结构与之前 [Wintersmith][2] 并不一样。最终折腾了几下又换回来了。然而不得不感叹 Hexo 模板的丰富是 Wintersmith 不能比的。所以之后自己又自行改了一下 css 样式，让原来的网站看起来不是很丑。

言归正传，选择 Github 寄放博客网站的原因是方便。

[Github Pages][3] 为每个用户，用户的每个项目都保留了一个静态页面站点。这些静态站点资源是通过 git 来部署的。个人站点需要在 github 上建立一个 `用户名.github.io` 的 repo，然后把相关文件 push 到 master 分支上。
通过 `https://用户名.github.io/` 访问。项目的站点是在相应的项目库中建立一个 gh-pages 分支，然后将其中的源代码等文件清空，并把网站文件加进去，通过 `https://用户名.github.io/项目名` 来访问。

个人站可以绑定个人域名，通过 CNAME 映射过去。同时要在根目录下放一个 CNAME 文件，其中写上个人域名地址，以便验证和授权。

所以，这跟以前用 ftp 上传文件没有什么区别。

现在，这个博客网站就是一个 Github Pages 站点，并且绑定了个人域名。 https://aristotle9.github.io/ 和 http://blog.mukio.org/ 都能访问。

[0]: https://www.staticgen.com/
[1]: http://hexo.io/
[2]: https://github.com/jnordberg/wintersmith
[3]: https://help.github.com/categories/github-pages-basics/