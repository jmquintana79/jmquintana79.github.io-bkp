# JEKYLL QUICK START

Jekyll Bootstrap is a powerful framework to create easily a static website. On the other hand, GitHub provide a hosting and enviroment to develop and launch this kind of website. 

Furthermore, in my case I have use a theme developed by  <a href="https://panossakkos.github.io/" target="\_blank">Panos Sakkos</a> to build a more awesome web profile. After of include this theme, I have improved and customized to 

## 1. Host in 3 minutesbe update to my needs.

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
In order to preview your blog locally you'll need to install the Jekyll ruby gem. 

<pre><code data-trim class="bash">
sudo apt-get install ruby1.9.3 ruby1.9.1-dev nodejs
</code></pre>

Note gem dependencies will also be installed. You don't have to run a local version but it helps if you want to preview your content before publishing. 

<pre><code data-trim class="bash">
$ gem install jekyll
</code></pre>

If you run into a problem please consult the original <a href="http://jekyllrb.com/docs/installation/" target="\_blank">Jekyll installation documentation</a>.

Once the gem is installed you can navigate to your Jekyll-Bootstrap directory. If you've followed the homepage instructions this will be: <a href="" target="\_blank">USERNAME.github.com</a>. Once in the directory you'll run jekyll with server support:

<pre><code data-trim class="bash">
$ cd USERNAME.github.com 
$ jekyll server --host $IP --port $PORT
</code></pre>

Your blog is now available at: <a href="" target="\_blank">http://localhost:4000</a>. In order to stop the server it is only necessary use **(Ctr + C)**. On the other hand, while you are developing or customizing the blog, to update changes is necessary stop and re-start the server.

## 3. Create a Post
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
Jekyll-Bootstrap can be used as-is as a basic blogging platform but also it could be customizing deeply:

#### Themes

Jekyll-Bootstrap supports modular theming. Themes can co-exist and be enabled/disabled on demand. In my case, I have used a theme developed by  <a href="https://panossakkos.github.io/" target="\_blank">Panos Sakkos</a>.

#### Blog Configuration

Jekyll and Jekyll-Bootstrap has a simple but powerful Jekyll Configuration System. You can:

Specify a custom permalink format for blog posts.
Specify a commenting engine like disqus, intensedebate, livefyre, or custom.
Specify an analytics engine like google, getclicky, or custom.

#### Jekyll Introduction

I highly recommend reading the <a href="http://jekyllbootstrap.com/lessons/jekyll-introduction.html" target="\_blank">Jekyll Introduction</a> if you plan to customize your blog. 

## Licensing

This work is distributed under the MIT license (LICENSE-JMQuintana.mit) with theme copyright Panos Sakkos from 'PanosSakkos/personal-jekyll-theme'. This one is also distributed under the MIT license (LICENSE-PanosSakkos.mit).
