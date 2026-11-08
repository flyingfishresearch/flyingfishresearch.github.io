# Tongji Flying Fish Research Lab Website

This is the website of the Tongji Flying Fish Research Lab at the Shanghai Research Institute for Intelligent Autonomous Systems (SRIAS), Tongji University.

This website is built with Jekyll, Bootstrap, and Bootswatch. It uses Jekyll Scholar to generate publication lists.

## Working across computers

Only committed changes that have been pushed to GitHub are available to another computer. Before switching computers, commit and push your work. On the next computer, pull the latest changes before editing.

### First-time setup

Install Git. From the folder where you want to keep the project, run:

```shell
git clone --branch main https://github.com/flyingfishresearch/flyingfishresearch.github.io.git
cd flyingfishresearch.github.io
git config user.name "Your Name"
git config user.email "your-email@example.com"
```

Replace the name and email with your own commit identity. These settings apply to this local repository. Public read access allows cloning and pulling; pushing requires authentication with a GitHub account that has write access.

### Each editing session

Open a terminal in the repository folder and check for unfinished local work:

```shell
git status
```

Once the working tree is clean, switch to the source branch and pull:

```shell
git switch main
git pull --ff-only origin main
```

Edit and review the content, then commit and push:

```shell
git diff
git add -A
git commit -m "Update website content"
git push origin main
```

Use `main` for source changes. The `gh-pages` branch contains generated files. An `Already up to date.` message means there are no newer commits to pull. If local and remote commits have diverged, `--ff-only` stops so the histories can be reconciled explicitly.

See the official [git clone](https://git-scm.com/docs/git-clone), [git pull](https://git-scm.com/docs/git-pull), and [GitHub authentication](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github) documentation for details.

## Editing content

| Content | File or folder |
| --- | --- |
| Page text | `_pages/` |
| News items | `_data/news.yml` |
| Team member profiles | `_data/team_members.yml` |
| Publication records | `_bibliography/uscl_publications.bib` |
| Publication formatting | `_layouts/bib.html` and `_bibliography/ieee-with-url-mod.csl` |
| Site title, contact details, and configuration | `_config.yml` |
| Header, navigation, and footer | `_includes/header.html` and `_includes/footer.html` |
| Page layouts and home page logo | `_layouts/` |
| Custom style overrides | `css/main.scss` |
| Supporting Sass styles | `_sass/` |

Preserve YAML indentation and field names when editing news and member profiles. Add new news items at the top of `_data/news.yml`. The home page uses the first five entries; the News page lists all entries. The limit is set in `_includes/news.html`.

## Local preview

Git is sufficient for pulling, editing, committing, and pushing the source. Local preview also requires Ruby, its required build tools, and Bundler. Once those are installed, run:

```shell
bundle install
bundle exec jekyll serve
```

Open the local URL printed by Jekyll. Restart the preview server after changing `_config.yml`. To generate the static files in `_site/` without starting a server, run `bundle exec jekyll build`. See the [Jekyll documentation](https://jekyllrb.com/docs/) for setup instructions.

## Publishing

The workflow in `.github/workflows/deploy.yml` runs when changes are pushed to `main` or `master`. It builds the website with Jekyll and publishes the generated files to `gh-pages`. Check the `deploy` workflow in the repository's Actions tab after pushing, then review the published website.

## Credits and license

The design was adapted primarily from [Allan Lab](https://www.allanlab.org). This website builds on the work of the Jekyll, Bootstrap, Bootswatch, and Jekyll Scholar communities.

The code is released under the MIT License.
