---
layout: post
section-type: post
title: Jekyll Quick Start
category: tech
tags: [ 'tutorial', 'jekyll' ]
---

The user's taste and needs of developers about webpages changes very quickly. Users require awesome websites with a very clear exposition of the information. On the other hand, developers need tools easy to be deployed and specially easy to be filled, customized and updated. Jekyll Bootstrap provides with a very powerfull tool to create awesome websites in a few minutes. 

Jekyll has a plugin system with hooks that allow you to create custom generated content specific to your site. You can run custom code for your site without having to modify the Jekyll source itself.

But of course, a website need a host and a plainfull way to update changes between local development places and the host. GitHub is the social code-hosting platform based on Git used to store, share and manage open source projects. It is completally free and there are 8.2 million people collaborating across 19 million GitHub repositories. 

In my case, my needs were very simple. I only need a easy way to create a very simple homepage to show my skills, include my work into my leisure time and the most important thing, to update the information very quickly, without the necesity of writing very long scripts of for example html to create a beautiful web where display my experiencies. Furthermore I have found very instering the possibility to include shortcodes into GitHub Gists in order to be used while I am developing. Now, It is not necessary that I remember too much command and statements. Now I can counsult in my personal library of small codes.


## 1. Host in 3 minutes

Host Jekyll project on GitHub is possible setup in only in 3 Minutes. Firstly it is necessary join in GitHub if you are not an account before.

After of this, you can start:

### 1. Create a New Repository on GitHub

Go to your <a href="https://github.com" target="\_blank">https://github.com</a>
 and create a new repository named "USERNAME.github.com"

### 2. Install Jekyll-Bootstrap on GitHub

Enter these commands into your terminal in a directory you want your blog to be:

<pre><code data-trim class="bash">
$ git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com
$ cd USERNAME.github.com
$ git remote set-url origin git@github.com:USERNAME/USERNAME.github.com.git
$ git push origin master
</code></pre>

### 3. Profit

After GitHub has a couple minutes to do your blog will be publicly available at 
<a href="" target="\_blank">http://USERNAME.github.com</a>.

Already have your blog on GitHub?

When you have installed, run Jekyll-Bootstrap locally to check:

<pre><code data-trim class="bash">
$ git clone https://github.com/plusjade/jekyll-bootstrap.git
$ cd jekyll-bootstrap
$ jekyll serve
</code></pre>

See it in action at <a href="" target="\_blank">http://localhost:4000</a>


## 2. Run Jekyll Locally
In order to preview your blog locally you'll need to install the Jekyll. 

<pre><code data-trim class="bash">
sudo apt install jekyll
</code></pre>

If you run into a problem please consult the original <a href="http://jekyllrb.com/docs/installation/" target="\_blank">Jekyll installation documentation</a>.

Once the gem is installed you can navigate to your Jekyll-Bootstrap directory. If you've followed the homepage instructions this will be: <a href="" target="\_blank">USERNAME.github.com</a>. Once in the directory you'll run jekyll with server support:

<pre><code data-trim class="bash">
$ cd USERNAME.github.com 
$ jekyll serve --host $IP --port $PORT
</code></pre>

Your blog is now available at: <a href="" target="\_blank">http://localhost:4000</a>. In order to stop the server it is only necessary use **(Ctr + C)**. On the other hand, while you are developing or customizing the blog, to update changes is necessary stop and re-start the server.

## 3. Create a Post

In order to create easily  a post, page (next point) or another elements it is possible use <a href="http://octopress.org/docs/blogging/" target="\_blank">rake command</a>. For this, it is required include a <a href="http://octopress.org/" target="\_blank">**Octopress**</a> "Rakefile" file into your website folder. This file include customizable rules to be launched with *rake tasks*. Any complete example of "Rakefile" file could be download from official <a href="https://github.com/imathis/octopress" target="\_blank">source website</a>.

Create posts easily via rake task:

<pre><code data-trim class="bash">
$ rake post title="Hello World"
</code></pre>

The rake task automatically creates a file with properly formatted filename and YAML Front Matter. After you have to set your own title while, by default, the date would be set with the current date.

These included post could be Markdown files. This format allow a very easy way to include new content quickly.

## 4. Create a Page
Create pages easily via rake task:

<pre><code data-trim class="bash">
$ rake page name="about.md"
</code></pre>

Create a nested page:

<pre><code data-trim class="bash">
$ rake page name="pages/about.md"
</code></pre>

Create a page with a "pretty" path:

<pre><code data-trim class="bash">
$ rake page name="pages/about"
# this will create the file: ./pages/about/index.html
</code></pre>

The rake task automatically creates a page file with properly formatted filename and YAML Front Matter as well as includes the Jekyll Bootstrap "setup" file.

## 5. Publish
After you've added posts or made changes to your theme or other files, simply commit them to your git repo and push the commits up to GitHub.

<pre><code data-trim class="bash">
$ git add .
$ git commit -m "Add new content"
$ git push origin master
</code></pre>

A GitHub post-commit hook will automatically deploy your changes to your hosted blog. You will receive a success or failure notice for every commit you make to your blog.

## 6. Customize
Jekyll-Bootstrap can be used as a basic blogging platform but also it could be customizing deeply:

#### Themes

Jekyll-Bootstrap supports modular theming. Themes can co-exist and be enabled/disabled on demand. In my case, I have used a theme developed by  <a href="https://panossakkos.github.io/" target="\_blank">Panos Sakkos</a>.

#### Blog Configuration

Jekyll and Jekyll-Bootstrap has a simple but powerful Jekyll Configuration System. You can:

- Specify a custom permalink format for blog posts.
- Specify a commenting engine like disqus, intensedebate, livefyre, or custom.
- Specify an analytics engine like google, getclicky, or custom.
- Install and use available plugins as for example:

<pre><code data-trim class="bash">
$ gem install jekyll-paginate   
$ gem install jemoji
</code></pre>


#### Jekyll Introduction

I highly recommend reading the <a href="http://jekyllbootstrap.com/lessons/jekyll-introduction.html" target="\_blank">Jekyll Introduction</a> if you plan to customize your blog. 

