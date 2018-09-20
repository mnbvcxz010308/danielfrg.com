---
title: "My Static Website Workflow on iOS"
slug: my-static-website-workflow
date: 2018-09-18
tags: ["Blogging","iOS"]
author: Vipin G S
---

This blog is a static website built with Hugo. This means that after writing a post, the entire site is rebuilt at which point the new content is visible. This differs from a dynamic website, such as Wordpress, which makes a call to a database to retrieve the desired content each time a page is loaded. 

My workflow until September was pretty simple:

1. write content (in BBEdit or Coda 2)
1. 1build website locally
1. commit to GitHub
1. upload the generated _site directory to Surge
I had to migrate this workflow to iOS.
### 1. WRITING CONTENT
There are many capable Markdown editors for iOS, almost too many to mention. When writing posts on iOS, I’ve settled on the excellent Drafts app from Agile Tortoise.  

As an added advantage, Drafts supports the TextExpander keyboard. I consider this essential as I have many blog post expansions in TextExpander, such a Jekyll’s YAML front matter. For example, the front matter for this post is as follows:  

---
	```
	layout: post
	title: My Static Website Workflow on iOS
	excerpt: “How I migrated my static website workflow from macOS to iOS."
	categories: [iPad Pro, Working Copy, Drafts, Netlify]
	date: 2016-11-02T08:00:00+08:00
	#modified:
	identifier: CC6E9F6D-2A90-4434-A9CF-CBE9F0602C47
	#image:
	#link: 
    ```
---  
### 2. BUILDING THE WEBSITE
On macOS it’s possible to build the website locally, via Terminal, as Jekyll can be installed. On iOS this isn’t possible. My approach to this problem: remove this step from the workflow.

When I tried to solve this problem initially, the question I was trying to answer was how do I continue to do this? Over time, that changed to do I need to do this? The answer is no.

### 3. COMMITTING TO GITHUB
My solution for committing to GitHub was to start using Working Copy which allows me to manage the website’s GitHub repository.

So now, after a post is written in Drafts, I copy the content to a new file in the _posts directory in the website’s GitHub repository using Working Copy, commit and push the changes.  

### 4. UPLOADING _SITE
Instead of using Surge to host my site, I now use Netlify. Netlify monitors changes to the website’s GitHub repository and when a change is made they do the rest, in their own words. In short, Netlify:
	checks out the repository
	builds the site using the command I’ve provided: bundle exec jekyll build
	uploads the generated _site/ directory

With my new iOSified workflow I no longer have to worry about building my website locally or uploading it. This doesn’t preclude me from continuing to build my site locally on macOS — indeed, if I am making design changes I will work on a Mac — but the move to iOS forced me 
to fundementally re-think and simplify my workflow.

I now write, commit, and wait for changes to be visible.