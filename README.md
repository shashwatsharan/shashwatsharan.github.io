# shashwatsharan.github.io

Personal and academic website of Shashwat Sharan. Live at <https://shashwatsharan.github.io>.

GitHub builds this site automatically with Jekyll every time a file changes (about a minute).

## Where things are

| File | What it is |
|---|---|
| `index.md` | Home page (intro, news, contact) |
| `research.md`, `publications.md`, `teaching.md`, `cv.md` | The other pages |
| `_config.yml` | Site title, subtitle, nav menu, footer links |
| `_layouts/default.html` | Shared header/footer around every page |
| `assets/css/style.css` | All styling (fonts, colours, spacing) |
| `assets/img/` | Images (`profile.jpg` = your photo, `wave.svg` = header line) |

## How to…

**Edit a page.** Open the `.md` file on GitHub, click the pencil icon, edit, commit.

**Write maths.** Use double dollar signs, inline or on their own line:

```
The coupling $$g_{1D} = \tfrac{2}{3}\mu/R_{TF}$$ appears inline.

$$
i\hbar\Psi_t = -\frac{\hbar^2}{2m}\nabla^2\Psi + g\lvert\Psi\rvert^2\Psi
$$
```

Use `\lvert x \rvert` rather than `|x|` for absolute values.

**Add a news item / CV entry.** Copy an existing two-line block:

```
Jul 2026
: What happened.
```

**Add your photo.** Upload a square-ish `profile.jpg` into `assets/img/`. It appears on the home page automatically.

**Add a CV or statement PDF.** Upload `cv.pdf`, `research-statement.pdf` or `teaching-statement.pdf` into `assets/`. The links appear on the CV page automatically.

**Add a figure.** Upload the image to `assets/img/`, then in a page:

```html
<figure>
  <img src="/assets/img/my-figure.png" alt="short description">
  <figcaption>What the figure shows.</figcaption>
</figure>
```

**Add a video.** Either upload a short `.mp4` (under ~50 MB) to `assets/video/` and use

```html
<figure>
  <video controls muted loop playsinline src="/assets/video/my-sim.mp4"></video>
  <figcaption>Caption.</figcaption>
</figure>
```

or, for longer videos, put them on YouTube and paste:

```html
<figure>
  <div class="video"><iframe src="https://www.youtube.com/embed/VIDEO_ID" allowfullscreen></iframe></div>
  <figcaption>Caption.</figcaption>
</figure>
```

**Add a page.** Create `newpage.md` with this at the top, then add it to `nav:` in `_config.yml`:

```
---
layout: default
title: New Page
---
```
