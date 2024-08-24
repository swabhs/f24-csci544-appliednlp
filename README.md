# USC CSCI 699 Data-Centric NLP Course Website

This is the source code for the course website for [USC CSCI 699: Data-Centric NLP](https://swabhs.com/csci699-dcnlp/), to be taught in Fall 2022.

It is a [Jekyll](https://jekyllrb.com) site based on a few modifications to the [Just the Class](https://github.com/kevinlin1/just-the-class) template,
which is itself built on the [Just the Docs](https://github.com/pmarsceill/just-the-docs) theme.
See those repositories for details on their structure and features.
Additional thanks to [Julian Michael](https://julianmichael.org/) for sharing the codebase for the [UW CSE 599D1 Computational Ethics in NLP class](https://courses.cs.washington.edu/courses/cse599d1/22wi/).

## Usage

<!-- We are hosting the site using the UW CSE course website webserver, which statically serves documents
from the CS UNIX machines. Continuous integration has been set up so that updates pushed to the
`main` branch of this repository get automatically copied to the webserver. -->

To preview the site locally, make sure ruby is installed, then run `bundle exec jekyll serve` from
the base directory of the repository. Then you can see the site at
[`localhost:4000/courses/22f/csci699-dcnlp/`](localhost:4000/courses/22f/csci699-dcnlp/).
See
[Setting up your GitHub Pages site locally with Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
for more details.

```
git add
git commit -m "Message"
git push
```

No need for special ruby environments.
