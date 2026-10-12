# Michael Huang: personal site

Source for my personal website. It is built with [Jekyll](https://jekyllrb.com) from the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template and hosted on GitHub Pages.

## Before you publish

Everything on the site is real content, so it can go live as it is. These are the gaps, most important first. Each one is also marked `TODO` in the file it belongs to; `grep -rn "TODO" _config.yml _pages _research` lists them all.

1. **Links in the sidebar:** fill in `email` and `github` under `author:` in `_config.yml`. A link only shows once its field is filled in. The Contact section on the home page appears once `email` is set.
2. **Photo:** replace `images/profile.png` with your own square photo, keeping the file name.
3. **Home page:** `_pages/about.md` has no school or degree yet, and no line about what you're looking for.
4. **CV:** `_pages/cv.md` has no dates, job title or education. To offer a PDF, save it as `files/resume.pdf` and the download link appears on its own.
5. **Research pages:** the files in `_research/` are short. Each section has a comment listing what to add.

## Where things are

| To change | Edit |
| --- | --- |
| Name, sidebar bio, location, links, colour theme | `_config.yml` |
| Links in the header | `_data/navigation.yml` |
| Home page | `_pages/about.md` |
| Publications | one file per paper in `_publications/` (see below) |
| Research areas | one file per area in `_research/`; the `order` number sets the position |
| CV | `_pages/cv.md` |
| Writing | one file per post in `_posts/`; start from `_drafts/note-template.md` |
| PDFs and other downloads | `files/` |

The Writing link stays out of the header until `_posts/` has its first post.

Talks and Teaching pages come with the template and are switched off. To turn one on, delete the `published: false` line at the top of its file in `_pages/`, uncomment its link in `_data/navigation.yml`, and add entries to the matching folder (`_publications/`, `_talks/`, `_teaching/`). The [template's own repository](https://github.com/academicpages/academicpages.github.io) has example entries for each.

## Adding a publication

Create a file in `_publications/` named `YYYY-MM-DD-short-title.md`:

```markdown
---
title: "Title of the paper"
date: 2025-06-01
venue: "Conference or journal name"
authors: "First Author, Michael Huang, Last Author"
research_area: multimodal-representation-learning  # optional: file name of a page in _research/
paperurl: "https://..."   # optional: the paper (PDF or publisher page); each link adds a button
arxiv: "2501.01234"       # optional
doi: "10.1234/abcd"       # optional
code: "https://github.com/..."  # optional
---

Abstract, shown on the paper's own page.
```

Papers are listed newest first, grouped by year. The names in `publication_names` under `author:` in `_config.yml` are shown in bold in the author list. With `research_area` set, the paper is also listed at the bottom of that research page.

`site_theme` in `_config.yml` switches the colour theme: `default`, `air`, `sunrise`, `mint`, `dirt` or `contrast`. Each has a light and a dark version, and visitors can switch between them with the icon in the header.

## Preview on your own computer

You need Ruby and Bundler.

```bash
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll serve -l -H localhost
```

The site is then at <http://localhost:4000> and reloads as you edit. Changes to `_config.yml` need a restart.

## Publish on GitHub Pages

The site is published from the `nafmichael/nafmichael.github.io` repository at <https://michaelswhuang.com>.

1. In the repository on GitHub, open Settings, then Pages, and set Source to **GitHub Actions**. The workflow in `.github/workflows/jekyll.yml` builds and deploys the site on every push to `master`.
2. Until the domain is connected, the site is at <https://nafmichael.github.io>.

### Connecting michaelswhuang.com

1. At the domain registrar, add four `A` records for the bare domain (`@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`. Then add a `CNAME` record for `www` pointing to `nafmichael.github.io`.
2. In the repository on GitHub, open Settings, then Pages, and enter `michaelswhuang.com` under Custom domain. No `CNAME` file is needed, because the site is deployed by a workflow.
3. In your GitHub account settings (not the repository's), open Pages and verify the domain, so no one else's GitHub Pages site can claim it.
4. Once GitHub has issued the certificate, which can take up to a day after DNS is in place, tick **Enforce HTTPS** in the repository's Pages settings.

`url` in `_config.yml` is already set to `https://michaelswhuang.com`. If you change domains, change it there too.

## Credits

Built on [Academic Pages](https://github.com/academicpages/academicpages.github.io), which is a fork of [Minimal Mistakes](https://mademistakes.com/work/minimal-mistakes-jekyll-theme/) by Michael Rose. Both are released under the MIT License; see `LICENSE`.
