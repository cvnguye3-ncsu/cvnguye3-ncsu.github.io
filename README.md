# Calvin Nguyen — Resume Website

Personal resume and research website for [Calvin Nguyen](https://cvnguye3-ncsu.github.io), built with Jekyll and the [Academic Pages](https://academicpages.github.io/) theme.

## Site content

- `_pages/about.md` — homepage
- `_pages/cv.md` — web CV
- `_publications/` — research and publication entries
- `_config.yml` — site URL, metadata, and sidebar profile
- `_data/navigation.yml` — header navigation
- `calvin-nguyen-resume-updated.pdf` — downloadable resume
- `3748636.3762766.pdf` and `IEEE_DSAA_2026___Cloud_Segmentation.pdf` — downloadable research papers
- `me.jpg` — sidebar profile photo
- `2025_ACM_SIGSPATIAL_picture.png` — SIGSPATIAL comparison figure shown on the Research page

Jekyll writes the generated site to `_site/`. Do not edit or commit that directory.

## Build locally with Ruby

### 1. Install prerequisites

Install Git, Ruby 3.2 or later, a compiler toolchain, and Bundler.

Ubuntu/Debian or WSL:

```bash
sudo apt update
sudo apt install git ruby-full build-essential zlib1g-dev
gem install bundler
```

macOS with Homebrew:

```bash
brew install git ruby
```

Follow Homebrew's printed instruction to add its Ruby `bin` directory to `PATH`, restart the terminal, and then run:

```bash
gem install bundler
```

### 2. Clone and install dependencies

```bash
git clone https://github.com/cvnguye3-ncsu/cvnguye3-ncsu.github.io.git
cd cvnguye3-ncsu.github.io
bundle config set --local path vendor/bundle
bundle install
```

The local Bundler setting keeps gems inside the repository's ignored `vendor/bundle` directory and avoids system-gem permission errors.

### 3. Preview the site

```bash
bundle exec jekyll serve --livereload
```

Open <http://127.0.0.1:4000>. Stop the server with `Ctrl+C`. Restart it after changing `_config.yml`.

### 4. Create a production build

```bash
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
```

A successful command creates the deployable site in `_site/`.

## Build locally with Docker

Docker is the simplest option when Ruby is not installed:

```bash
docker compose up --build
```

Open <http://127.0.0.1:4000> and stop the server with `Ctrl+C`.

To run a one-time production build:

```bash
docker compose run --rm -e JEKYLL_ENV=production jekyll-site \
  bundle exec jekyll build --strict_front_matter
```

## Deploy to `cvnguye3-ncsu.github.io`

This is a GitHub user site, so the repository must be named exactly `cvnguye3-ncsu.github.io`. The checked-in `_config.yml` is already configured with:

```yaml
url: https://cvnguye3-ncsu.github.io
baseurl: ""
repository: "cvnguye3-ncsu/cvnguye3-ncsu.github.io"
```

### First deployment

1. Push the repository to `cvnguye3-ncsu/cvnguye3-ncsu.github.io`.
2. On GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select the `master` branch and the `/(root)` folder, then click **Save**.
5. Open the repository's **Actions** tab and wait for the Pages build and deployment to finish.
6. Visit <https://cvnguye3-ncsu.github.io>. In **Settings → Pages**, enable **Enforce HTTPS** if GitHub does not enable it automatically.

GitHub recommends branch publishing when a site does not need a custom build process. See GitHub's documentation for [configuring a Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) and [using Jekyll with GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).

### Publish later updates

Build locally first, then commit and push the source files:

```bash
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
git status
git add _config.yml _data _includes _layouts _pages _publications _sass README.md *.pdf me.jpg 2025_ACM_SIGSPATIAL_picture.png
git commit -m "Update resume website"
git push origin master
```

Every push to the configured publishing branch triggers a new Pages deployment. Do not add `_site/`; GitHub builds it from the Jekyll source.

## Updating the resume

Replace `calvin-nguyen-resume-updated.pdf` with the new PDF, then update the corresponding web content in `_pages/about.md`, `_pages/cv.md`, `_data/cv.json`, and `_publications/`. Run the production build before pushing so broken YAML front matter or Liquid templates are caught locally.

## Troubleshooting

- **`bundle` is not found:** install Bundler with `gem install bundler` and ensure Ruby's `bin` directory is on `PATH`.
- **Gem permission errors:** run `bundle config set --local path vendor/bundle`, then `bundle install` again.
- **Pages shows a 404:** confirm the repository name, Pages source (`master` and `/(root)`), and the successful deployment in the Actions tab.
- **Links or styles are missing:** keep `baseurl: ""` for this user site and restart the local Jekyll server after editing `_config.yml`.
- **GitHub rejects a Pages build:** run the production build locally with `--strict_front_matter` and fix the first reported error.
