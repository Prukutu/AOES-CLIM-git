---
title: Github Pages
teaching: 10
exercises: 0
questions:
- "What is Github Pages?"
- "How can I use it to create a project web site?"
objectives:
- "Understand how to create a web page associated with a repository on github."
- "Understand how to use Jekyll formatting templates."
---

## Github Pages

Build your own web sites for your projects on Github.

#### Web link to your web pages 
You will have a URL associated with your Github pages of the form:

  `https://username.github.io/` 
  
where _username_ is your Github user name.
  
#### Links to individual repositories
You can have a site for every repository - the will have a similar form:
  
  `https://username.github.io/repo-name/` 
  
where _repo-name_ is the name of the repository.
  
#### Set up a repo for your class project

If you have not alreasdy created a repository for your class project, you can do that now. 
For example, if you will call it `clim680_project`, click on **Repositories** at the top of 
the page and click **New** to create a new repository.

To make a repository web site, go into your repository and click **Settings** at the top
of the page, and **Pages** on the left side. 
Choose a branch to deploy, and click **Save**

#### index.html is your landing page
You can add a file called `index.md` in your repository. It is a markdown file that will become the 
default page when someone accesses the web page link for the repository. 
You can compose your web page using standard markdown language. 
For your project, this could be the page for your final report, or it could be a page that links
to it, and any other pages. 

To link to other pages, add a link to `pagename.html` in `index.md`, and edit the corresponding `pagename.md` to create the new page.
You can use this method to create a set of links, e.g., one to your 5-minute project proposal 
(perhaps as link `proposal.html` with contents in `proposal.md`), one for your final project, 
one to your data description (copied from Blackboard), etc.

In the absence of a `index.md` file in your repostiory, the Github Pages web link will default to your `README.md` file.

#### Formatting markdown in Github
Formatiing is basically the same as markdown in Jupyter notebooks.  There is a 
[formatting guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) that lists all the codes.
Github Pages very nicely converts markdown codes into _html_ codes when it creates web pages from your `*.md` files.

And directory structures work the same as elsewhere. 
You can use relative paths from your repository's directory. 
For instance, in your repository you can create a directory called `figures` 
(this is done by clicking on **add file** and adding a file called `figures/filename` where `filename` 
can be anything, including the name of a figure file), and put 
your figures there (as .pdf files, .png files, .jpg, .svg, etc.) and embed them in your markdowns as images
linked by their relative paths. 
Likewise for any other content links.

#### Styles from Jekyll

In your repository, adding a file `_config.yml` with the following line will apply a 
formatting style to your default web page.  A single line of code should be
added to this file:
`theme: jekyll-theme-xxxxxx`
where `xxxxxx` is the name of one of the following themes:
* architect
* cayman
* dinky
* hacker
* leap-day
* merlot
* midnight
* minima
* minimal
* modernist
* slate
* tactile
* time-machine
You can try them out to see how they look 
([more about themes](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll)).
