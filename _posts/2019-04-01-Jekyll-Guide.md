---
title: Getting Started With Jekyll
date: 2019-04-03
image: /images/blog/jekyll.jpg
soundcloud: https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/506094486&color=%23ff5500
categories: [tutorial, jekyll]
tags: [jekyll, HTML, CSS, github pages, web dev, ruby]
---

{% raw %}
### What is Jekyll
Jekyll is a static site generator and web template system. In other words, you can use Jekyll, along with a template, to build a website and then take the output and host it somewhere. The HTML and CSS for your site can be broken down into boilerplate chunks of code that will be reused and inherited by each page. For example, even though I have a nav bar on each page of my site, it's only written once and then included in each page. This makes it both easier and faster to make changes to my website's front-end and I'm also less likely to make mistakes.

### Environment Setup
To get started, you'll have to install a few things:
- Ruby 💎
- Bundler
- Jekyll 🌡

I like to use rbenv to manage different versions of Ruby:
```
brew install rbenv
```

Use rbenv to install the latest version of Ruby:
```
rbenv install {latest_version}
```

Use RubyGems to install Bundler and Jekyll:
```
gem install bundler jekyll
```

### Directory Structure
If you run the below command, Jekyll will generate a sample website and the directory structure will look like this:
```
jekyll new myBlog
```
```
myBlog:
├── _config.yml
├── _posts
├── 404.html
├── about.md
├── Gemfile
├── Gemfile.lock
└── index.html
```
> Any file or directory beginning with an underscore is special to Jekyll.

Now run:
```
cd myBlog
bundle exec jekyll serve
```
Then open up your favorite browser and connect to `localhost:4000` and you'll see the sample website. Take a minute to explore.

If you check the `myBlog` directory now, you'll see a new folder was created called, `_site`. This is the static website that Jekyll generated for you! When you run `bundle exec jekyll serve`, Jekyll generates the static site in `_site` and hosts it locally on `localhost:4000`. It has a basic hierarchy of inheritance that it follows to do this. Your template is a blueprint for a website and then Jekyll uses that to build it.

> Everything down here is still a work in progress.

At this point, it seems like magic. I personally found it difficult to understand what was going on under the hood. So I decided to use my personal site's directory structure to help explain and talk about some of the other special Jekyll directories.

### My Personal Site
```
rainerdeal.github.io:
├── _drafts                                     // [Optional] Holds unfinished posts.
    └── Sample-Post-Guide.md                    // A draft is just a post without the date.
|
├── _includes                                   // [Optional] Holds boilerplate code.
    ├── footer.html                             // I made my footer, header, and nav sections
    ├── header.html                             // includes because they are shared across all
    └── nav.html                                // of my pages.
|
├── _layouts                                    // Holds the themes for your site.
    ├── about.html                              // You should have a layout for each different
    ├── default.html                            // type of page.
    ├── details.html
    └── post.html
├── _portfolio
├── _posts
    ├── 2018-10-23-Cutting-My-Fingers-Off.md
    ├── 2018-10-23-Ghost-in-the-Shell.md
    ├── 2019-01-02-Blue-Apron-Review.md
    └── 2019-04-01-Jekyll-Guide.md
├── _sass
    └── post.scss
├── images
├── styles
    ├── bootstrap
    └── main.scss
├── _config.yml
├── .gitignore
├── about.md
├── CNAME
├── favicon.ico
├── Gemfile
├── Gemfile.lock
├── index.html
├── portfolio.html
└── README.md
```

```
<!doctype html>
<html lang="en">

{% include header.html %}

<body>

    {% include nav.html %}

    {{ content }}

    {% include footer.html %}

</body>

</html>
```

{% endraw %}
