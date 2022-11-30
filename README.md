#### My website



This is the website of my first homepage. It is based on the Jekyll theme [al-folio](https://github.com/alshedivat/al-folio).

The source code is in the `main` branch, and the publish version (the generated static website) is in the `gh-pages` brach. Since the standard flow of GitHub Pages do not support Jekyll plugins beyond a [spported version list](https://pages.github.com/versions/), I enoutered building errors and could not publish the generated sites.

After search, I find one workaround is to use __GitHub Actions__, which allow us to use any version of Jekyll and Jekyll plugins. To set up the action, we need to create a workflow file in the `{project root directory}/.github/workflows/xxx.yml` (e.g., github-pages.yml). The workflow can automatically update the website based on every github push operation. The details can be find in this [tutorial](https://jekyllrb.com/docs/continuous-integration/github-actions/).

You can change the website configuration by editing the `_config.yml` configration file. Please pay attention to the `url` and `baseurl`. Due to the incorrect settings of these two fields, I came accross some issues, e.g., the generated static website cannot be well redered and images cannot be loaded appropriately. Basically, the `url` should be my GitHub website, and the `baseurl` should be the repository name, e.g., `/miao.github.io`. To change the page content, one can edit the `.md` files in the `_pages` directory. Also, publications can be added by editing the `_bibliography/paper.bib`. News can be added by creating new announcement file in the `_news` directory.

After editing, one can check it locally by running the command `bundle exec jekyll serve --watch` in the project root directory. The locally generated website is in the `_site` directory
