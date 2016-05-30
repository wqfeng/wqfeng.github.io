---
layout: post
title:  "20分钟搭建一个博客!"
date:   2016-05-30 09:42:18 +0800
categories: jekyll
---
这是我用[Jekyll][jekyll]搭建的博客，托管在[GitHub Pages][github-pages]上。如果您愿意花费20分钟，也可以搭建一个同样的博客。

1. 在GitHub上创建一个新的代码仓库`wqfeng.github.io`，请用你的GitHub用户名替换掉`wqfeng`，选择默认的`Jekyll .ignore`文件。

2. 将代码仓库`clone`至本地，在这里使用Jekyll生成博客。

3. 如果您尚未安装Ruby，建议使用[RVM][rvm]安装Ruby。

	3.1 安装[RVM][rvm]。

	3.2 使用RVM安装Ruby 2.3.1：`rvm install 2.3.1`

	3.3 安装Bundler：`gem install bundler`

	3.4 如果您和我一样， RubyGems被墙，使用淘宝提供的镜像站点：

		gem sources --add https://ruby.taobao.org --remove https://rubygems.org

4. 在代码仓库的根目录创建Gemfile。
	
	`touch Gemfile`

5. 将下面的内容拷贝至Gemfile。

		source 'https://ruby.taobao.org'
		gem 'github-pages', group: :jekyll_plugins

6. 使用Bundler安装依赖。

	`bundle install`

7. 使用Jekyll生成网站。

	`bundle exec jekyll new . --force`

8. 更改`_config.yml`配置。

		# Site settings
		title: Udacity 学习笔记
		email: qunfengw@gmail.com
		description: 学而不思则罔，思而不学则殆。
		baseurl: "" # the subpath of your site, e.g. /blog
		url: "https://wqfeng.github.io" # the base hostname & protocol for your site

9. 在本地运行并测试。

	`bundle exec jekyll serve`

10. 测试完成后将变更`push`到GitHub，访问：[https://wqfeng.github.io][blog]，不出意外的话，恭喜你，又给自己弄了个博客！

11. 后续使用MarkDown格式在`_posts`目录下编写新的文章，文件名遵循`YYYY-MM-DD-name-of-posts.markdown`的格式，`push`到GitHub即可发布。

[jekyll]: http://jekyllrb.com/
[github-pages]: https://help.github.com/articles/user-organization-and-project-pages/
[rvm]: https://rvm.io
[blog]: https://wqfeng.github.io
