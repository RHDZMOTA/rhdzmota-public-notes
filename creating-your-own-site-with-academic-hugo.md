
The [Academic Theme] for [Hugo] allows you to easily create a website using [markdown] and/or [jupyter] files. This blog-post is just a personal test, but might be useful for beginners wanting to create their site. 

[Academic Theme]: https://sourcethemes.com/academic/
[Hugo]: https://gohugo.io/
[markdown]: https://en.wikipedia.org/wiki/Markdown
[jupyter]: https://jupyter.org/

## Setup

Go to a [working fork of the academic-kickstart github repository](https://github.com/rhdzmota/academic-kickstart)
and fork the repository. Note that the version I provide on my github is compatible with the instructions on this
blogpost. You can try forking the latest [academic-kickstart github repository](https://github.com/sourcethemes/academic-kickstart)
but be aware you might have to use another hugo version than the one provided on this guide.


Now download the content with:


```commandline
$ mkdir my-site && \
    wget -O - https://github.com/github-username/academic-kickstart/tarball/master | \
    tar xz -C my-site --strip-components 1
```

**Replace** `my-site` with the name of the repository that will contain your site's code (optional) and `github-username` with your github username (or use `rhdzmota` if you didn't fork the repo). 


Install hugo (select your version [here](https://github.com/gohugoio/hugo/releases)). For debian-based distributions: 

```commandline
$ sudo apt install wget && \
    wget -O hugo.deb 'https://github.com/gohugoio/hugo/releases/download/v0.55.6/hugo_extended_0.55.6_Linux-64bit.deb' && \
    sudo dpkg -i hugo.deb
```

**Note** that [academic version 4.3.1+ requires hugo-extended 0.55.6+](https://github.com/gcushen/hugo-academic/issues/1092).  

Verify your installation by running: `hugo version`. 

Now enter your site's directory and create the git-repository:

```commandline
$ cd my-site && \
    rm -rf themes/academic .gitmodules && 
    git init && git submodule add https://github.com/gcushen/hugo-academic themes/academic 
```

You should be able to preview the site with: `hugo serve -D`

For now on, feel free to configure your site. You can see a [live example here](https://academic-demo.netlify.com/) with the [github code here](https://github.com/gcushen/hugo-academic/tree/master/exampleSite). 

## Publishing with github pages

Add the following line anywhere on `config/_default/config.toml`:

```text
publishDir = "docs"
```

Now when running `hugo` on the commandline, a `docs` directory will appear. This directory contains a set of static files that can be directly published to github pages. 

Just configure your repository in github and push into master. More documentation [here](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages). Integration with custom domains guide [here](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages) and [here](https://dev.to/trentyang/how-to-setup-google-domain-for-github-pages-1p58).
