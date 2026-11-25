# Zhuochao Huang — personal academic website

This is a one-page Quarto website using the native `jolla` about template. The profile text is in `index.qmd`; the photograph is in `images/profile.jpg`. The `docs/` directory contains a ready-to-publish static HTML edition generated from the same content with Pandoc and the shared CSS. It is not the output of a Quarto render; Quarto was unavailable in the creation environment.

## Option A — publish immediately (no installation)

1. Create a public GitHub repository named `YOUR-USERNAME.github.io` (substitute your GitHub username).
2. Upload the contents of this project folder to the root of that repository (not the enclosing folder). Keep `docs/`, `images/`, `index.qmd`, `_quarto.yml`, and `styles.css` in their existing locations. Make sure `docs/index.html` and `docs/images/profile.jpg` are present.
3. Open **Settings → Pages → Build and deployment**. Set Source to **Deploy from a branch**, branch `main`, folder `/docs`, and Save. If the optional workflow runs while this source is selected, it can be ignored, or simply leave the workflow out when using this option.
4. Your site is available at `https://YOUR-USERNAME.github.io/` after deployment succeeds.

## Option B — build and publish with Quarto automatically (recommended for ongoing edits)

1. Upload the project as above, including `.github/workflows/publish.yml`. If the browser uploader omits hidden folders, create that file at exactly that path using GitHub's **Add file → Create new file** and copy the contents from the included workflow.
2. In **Settings → Pages**, choose **GitHub Actions** as the source instead of Deploy from a branch.
3. Open **Actions → Build and publish Quarto website → Run workflow** on `main`. The workflow installs Quarto, renders `index.qmd`, and publishes `docs/`. After that, each edit committed to `main` triggers another build.

## Edit locally (optional)

Install Quarto from https://quarto.org/docs/get-started/ and optionally RStudio. Open `index.qmd` in RStudio's Visual editor, or use a text editor. In a terminal in this project directory:

```sh
quarto preview
quarto render
```

`quarto preview` opens the local preview; `quarto render` regenerates `docs/`. If using Option A, upload the refreshed `docs/` after editing. If using Option B, commit your edited source files; GitHub renders them.

To replace the photo, overwrite `images/profile.jpg` and re-render. No image-hosting service is required.

The site intentionally contains no phone number, CV download, tracking, or separate publication list. The contact email and portrait are public when the site is published.

References: https://quarto.org/docs/websites/website-about.html and https://quarto.org/docs/publishing/github-pages.html
