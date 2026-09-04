# isotupa.github.io

Personal site: a profile page plus one write-up per project.

```
index.html              profile, project grid, experience, education
projects/*.html         one page per project
assets/css/site.css     the only stylesheet
assets/img/             figures, taken from the projects themselves
assets/video/           ThirdPerson flight demo
```

Plain static HTML with no build step and no dependencies. To preview locally:

```sh
python3 -m http.server 8000
```

then open <http://localhost:8000>.

## Deploying

Push to a GitHub repository named `isotupa.github.io`, then in
**Settings → Pages** set the source to *Deploy from a branch*, branch `main`,
folder `/ (root)`. The site appears at <https://isotupa.github.io> within a
minute or two. `.nojekyll` is present so GitHub serves the files as-is.

## Adding a project

Copy the closest existing page in `projects/`, change the `<title>`, meta
description, header block and body, then add a card to the grid in `index.html`
and fix the prev/next links at the bottom of the neighbouring pages.
