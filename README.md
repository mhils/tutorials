Tutorials
=========

Contents can be written both in HTML and [Markdown](http://daringfireball.net/projects/markdown/basics).

Build and serve tutorials locally
---------------------------------

The tutorials are hosted using GitHub Pages.
You can build and serve tutorials locally using Jekyll.
Please see [GitHub's help on how to use Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages).

As some URLs within the tutorials require the full hostname, you may encounter situations where you will not see local modifications, because the generated site still refers to a remote resource/a remote URL.
For that reason we included a local config that adjusts the URLs used to your local site.

Append `--config _config.yml,_config_local.yml` to your Jekyll command to override the remote URL setting.
It is important that `_config_local.yml` is provided as the second comma separated parameter!

Create new tutorials
--------------------

### Create directory and content
To create tutorials for a new lecture, create a directory in `lectures`.
As the directory name is being used for the URL and other configurations, you should choose an established abbreviation (i.e. eai for Enterprise Application Integration).

Each lecture has to have a `index.md` file that describes the lecture.
The file has to start with the Liquid declaration of the lecture's full title and the document's layout:
```
---
title: Enterprise Application Integration
layout: lecture
---

Description of the lecture in *Markdown syntax*
```

Each lecture is contained in a single file that you can name at your convenience.
Please note that tutorials within a lecture are sorted by their respective file names; therefore using numbers as prefixes allows you to control the order of appearance in the overview and table of contents (e.g. 010-introduction.md, 020-basics.md, etc).
A tutorial's content file also has to start with a Liquid declaration for the tutorial's title and its layout:
```
---
title: Introduction to EAI
layout: recipe
---

Content of the tutorial, which could also be put into a html file.
```

### Update configuration
To make a lecture's tutorials appear, you have to add information for `lectures` and `contacts` in `_config.yml`.