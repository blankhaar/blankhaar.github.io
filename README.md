# blankhaar.github.io

Personal website. Built with Jekyll, hosted on GitHub Pages.

## Local preview (optional)

GitHub will build the site for you when you push, so this is only needed if
you want to see changes before pushing.

```bash
bundle install
bundle exec jekyll serve
# open http://127.0.0.1:4000
```

If you don't have Ruby/Bundler set up, the simplest path on macOS is:

```bash
brew install ruby
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
gem install bundler
bundle install
```

## Publishing

The repo must be named **`blankhaar.github.io`** so the site lives at
`https://blankhaar.github.io`.

First-time setup:

```bash
cd /Users/boyl/projects/website
git init
git add .
git commit -m "Initial site"
gh repo create blankhaar.github.io --public --source=. --remote=origin --push
```

Then on GitHub: **Settings → Pages**, source = *Deploy from a branch*, branch
= `main`, folder = `/ (root)`. Save. The site appears at the URL above within
a minute or two.

After that, every `git push` triggers a rebuild automatically.

## Editing

- **About / bio** — `index.md`
- **News feed** — `_data/news.yml`
- **Featured papers** — files in `_papers/`. Add a new file, fill in the
  front matter, and write the lay summary in Markdown. It will show up in the
  Papers list and the homepage automatically.
- **Research themes** — `research.md`
- **CV** — `cv.md`. Drop the PDF at `assets/files/lankhaar-cv.pdf`.
- **Talks** — `talks.md`
- **Code** — `code.md`
- **Notes (blog)** — files in `_posts/`, named `YYYY-MM-DD-title.md`.
- **Photos** — `assets/img/`.
- **Styling** — `assets/css/main.css`.

## Adding a new paper feature

Create `_papers/short-slug.md` with this front matter:

```yaml
---
title: The title of the paper
authors: A. Author, B. Lankhaar, C. Author
journal: Astronomy & Astrophysics
year: 2026
date: 2026-01-15
doi: 10.1051/0004-6361/...
arxiv: "2601.12345"
summary: One-sentence hook for the cards.
figure: /assets/img/papers/my-figure.jpg
figure_alt: Description of the figure.
figure_caption: Optional caption shown under the figure.
press:
  - outlet: BBC News
    url: https://...
  - outlet: UiO press release
    url: https://...
---
```

Then write the body in Markdown — short headers like *In one sentence*,
*What's the question?*, *What did we do?*, *Why does it matter?*, *My role*.

## Anti-spam email

The contact email is built in JavaScript at click time
(`_includes/email.html`) so it never appears as plain text in the page
source — most scrapers will skip past it.
