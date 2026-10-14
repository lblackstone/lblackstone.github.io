# leviblackstone.com

Personal site, built by GitHub Pages' native Jekyll. No build pipeline or dependencies to maintain.

## Publishing an essay

Add a Markdown file to `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: My Essay Title
---

Body in GitHub-flavored Markdown.
```

Push to `main`. It appears at `/writing/slug/` and at the top of the Writing page, which replaces "Coming soon..." once a post exists. Add `description:` to the front matter to control the link-preview text.

## Preview locally

```sh
docker run --rm -p 4000:4000 -v "$PWD":/site -w /site ruby:3.3 \
  sh -c 'gem install github-pages webrick && jekyll serve --host 0.0.0.0'
```
