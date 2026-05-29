# Adding Content

## New Blog Post

Create a file in `content/posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: 2026-06-15
tags: [RF, circuits]
---

Post body in Markdown here.
```

- `date` must be `YYYY-MM-DD`
- `tags` is a list — creates tag pages automatically
- The post appears on `/blog/` and the homepage preview updates to the latest post

## New Publication

Edit `content/publications.md` and add an entry under the relevant section in `page.publications`:

```yaml
- title: "Paper Title"
  venue: "Conference Name 2026"
  year: 2026
  authors: "Bhaskaran, D. and Co-Author, X."
  abstract: "One-paragraph abstract."
  doi: "10.1109/XXXX.2026.YYYYYYY"
  tags: [RF, CMOS]
```

To also show it on the homepage, add it to `content/index.md` under `featured_pubs`.

## New Project

Edit `content/projects.md`. Add to an existing category or add a new one:

```yaml
categories:
  - name: "New Category"
    entries:
      - title: "Project Name"
        description: "One-sentence description."
        tags: [Verilog, FPGA]
        link: "https://github.com/..."   # optional
```

## Build & Preview

```bash
export NVM_DIR="$HOME/.nvm" && source "$NVM_DIR/nvm.sh"
npm run dev          # dev server at http://localhost:5173
npm run build        # production build to dist/
```

## Deploy

Push to `main` — GitHub Actions builds and deploys automatically to GitHub Pages.
