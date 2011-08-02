# Your Jekyll & GitHub Pages Blog
This is a basic website shell using [Jekyll](https://github.com/mojombo/jekyll/wiki) (blog engine) and [GitHub Pages](http://pages.github.com/) (hosting). It is a stripped down version of [my website](http://sumeetjain.com).

I'm a freelance web developer, so my website is structured for my expected audience - namely potential clients. The homepage is a summary of my skills and work experience. I also keep a journal for friends and family (and strangers). And I sometimes write more technical articles, so there's a category for those too.

Here's what the website looks like:

![Homepage](http://f.cl.ly/items/1m112R0s030c2O390J3C/Homepage.png)

![Listing Page](http://f.cl.ly/items/223f4146283I3l1f2Q3m/Listing%20Page.png)

![Post](http://f.cl.ly/items/1J3I3O2X1j1D1b3o0x0F/Post.png)

## GitHub Pages - Briefly.
If you have a GitHub repository called "*your_username*.github.com", it is automatically hosted with [GitHub Pages](http://pages.github.com/). Every time you push commits to that repository, the hosted version of the files is also updated. So my [sumeetjain.github.com](https://github.com/sumeetjain/sumeetjain.github.com) repository contains all of the files for my website; and whenever I want to update my website, I just push the changes to the repository.

*(Strictly speaking, you don't need to use GitHub Pages for hosting - this website shell should work equally well on any server that has Jekyll installed.)*

## Jekyll - Briefly.
Jekyll *generates* files for your website. So opening this repository's `index.html` file in a web browser won't do much for you. Rather, you'll need to run a mini-server so that Jekyll can generate the real website files. Then Jekyll will give you a URL for your website (usually [http://localhost:4000](http://localhost:4000)). If this sounds scary, don't worry. It is very simple - everything is built in.

## What You'll Need

- [Jekyll](https://github.com/mojombo/jekyll/wiki/install)
- [GitHub](http://github.com) - Not actually necessary, but strongly recommended.

I suggest [installing Jekyll](https://github.com/mojombo/jekyll/wiki/install) before you continue any further.

## "Enough already! Give me the website!"
It's easy, but there are several steps:

1. Fork this repository. (Click the 'Fork' button at top-right.)
2. From your Fork's page, click [Admin](you.github.com/admin) and rename the repository to "*your_username*.github.com". This is important.
3. Get your new repository! (In *Terminal*, run `git clone git@github.com:your_username/your_username.github.com.git`.)
4. Use a code editor to replace my information with yours in `_includes/settings.html`.
5. Edit `images/me.png` with a picture of yourself.
6. (Optional) Add your own Google Analytics code to `_includes/ga.html`.
7. In *Terminal*, type `jekyll --server`, and press `ENTER`. This runs the mini-server for your website.

Go to [http://localhost:4000](http://localhost:4000) to see your new website.

*(Type `CTRL-C` any time to shut the server down.)*

## Using Jekyll
Full instructions are available from the [Jekyll Wiki](https://github.com/mojombo/jekyll/wiki/). Usage instructions for this website shell follow:

### Blog Posts
To add a new post, make a new file in the `_posts` directory. Name the file with the date and title of the post (You can change both later).

Say you make a new file named `2011-08-03-my-first-post.markdown`. Add the following code to it:

```markdown
--- 
layout: post
category: journal
title: "My First Post"
---

Type your post here.
```

Save that and run `jekyll --server` in *Terminal* again. Go to [http://localhost:4000](http://localhost:4000) in your browser, and check out your journal:

The post was given a date of August 3, 2011 - you indicated that date through the filename. It also belongs to the Journal - instead of the Tech Writings or Photo sections - because you indicated "journal" in the `category` field. And everything below the `---` section makes up the content of your blog post.

**What are the available categories?**  
You can enter *journal*, *tech*, or *photos* in the `category` field.

**What if I want a post to belong to multiple categories?**  
Just put the categories in a comma-separated list inside square brackets. Like this: `category: [journal, tech]`.

**Are there any other fields besides category and title?**  
Just one. You can enter a link to your post's submission on Hacker News. I do this sometimes to direct my site's readers there for a healthy discussion of my post. To add a link to Hacker News, add `hn: http://news.ycombinator.com/item?id=1699523` inside the `---` section. (Obviously change the link itself to your post's HN link.)

There are examples of all of this in the site files already. You'll see them when you run the site for the first time.

### Portfolio
Adding things to the portfolio is pretty easy, too. Take a look at the `portfolio` folder to see examples. Just copy/paste as needed.

### That's it.
Just `git push` your changes and check them out at [http://your_username.github.com](#).

## Using Your Own Domain
You can use a custom domain for the website if you want. You'll need a paid account on GitHub. If you have one, it's pretty easy to set up:

1. Add your domain to `CNAME`. For example, my `CNAME` file is just one line: `sumeetjain.com`. That's probably all you'll need, too.
2. Add an entry in your DNS host for GitHub. [Details here.](http://pages.github.com/#custom_domains)