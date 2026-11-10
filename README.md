# FusionCore IT: Under Construction page

A single-page holding site for fusioncoreit.co.uk while the full site is finished.
Plain HTML and CSS, no build step. Styling matches the main site (fusioncore-it-website).

## Files

- `index.html`: the Under Construction page (all CSS is inline)
- `404.html`: sends any old or broken link back to the home page
- `CNAME`: tells GitHub Pages to serve this on fusioncoreit.co.uk
- `.nojekyll`: tells GitHub Pages to serve the files as-is

## Publish on GitHub Pages

1. Create a new public repo on GitHub, e.g. `fusioncore-it-coming-soon`.
2. From this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Add Under Construction page"
   git remote add origin https://github.com/fusioncoreit/fusioncore-it-coming-soon.git
   git push -u origin main
   ```

3. In the repo: Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.

## The custom domain

GitHub only lets one repo use a domain at a time. The main site repo
(`fusioncore-it-website`) currently has `fusioncoreit.co.uk` in its CNAME.

Before step 3 above, go to the `fusioncore-it-website` repo > Settings > Pages and
remove the custom domain (or unpublish that site). Then in this repo's Settings > Pages,
confirm the custom domain shows `fusioncoreit.co.uk` and tick "Enforce HTTPS" once it's available.

If the main site already loads on fusioncoreit.co.uk, your DNS is already pointing at GitHub Pages and doesn't need to change.

## Going live with the full site later

Remove the custom domain from this repo, add it back on `fusioncore-it-website`, and
remove the "Under Construction" banner from the main site's pages.
