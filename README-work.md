# Selected work upgrade: how to publish and edit

## Files in this package
- `index.html` and `Services.html`: the "Selected work" section is replaced in both (everything else is untouched)
- `work.css`, `work.js`: new styles and behaviour (tabs, gallery, lightbox)
- `images/work/posters/` (full size) and `images/work/posters/thumbs/` (fast previews)
- `images/work/logos/`

## Publish to your existing GitHub Pages site
Keep the same folder layout as your site (these files sit next to `index.html`).

Option A, in the browser
1. Open your repository on github.com (the one that serves your portfolio).
2. Add file > Upload files. Drag in `index.html`, `Services.html`, `work.css`, `work.js` and the whole `images` folder. If an `images` folder already exists, drag only `images/work` so your other images stay.
3. Choose "Commit changes" on the main branch.

Option B, with Git
```
git add index.html Services.html work.css work.js images/work README-work.md
git commit -m "Upgrade Selected work section with real projects"
git push
```

Then wait one to two minutes and hard-refresh the live page (Ctrl+Shift+R, or clear the cache on a phone).
Settings > Pages should show your site as published from your usual branch; nothing needs changing there.

## Website previews (drop-in screenshots)
Take a screenshot of each live site (about 1280 x 800, top of the home page) and save it with exactly these names inside `images/work/websites/`:

- `rise-women-empowerment-center.jpg`
- `hope-and-skills-center.jpg`
- `client-portfolio.jpg`

Upload them to GitHub next to the other images. The cards pick them up automatically; until a file exists the card shows the browser-bar stand-in.
For another website, copy one whole `<article class="web-card"> ... </article>` block in `index.html` and `Services.html`, change the title, text, link and the screenshot file name.

## Add or remove a poster
Each poster is one `<figure class="gal-item"> ... </figure>` block. Delete a block to remove it. To add one, copy a block,
change the image paths, title and description, and put the optimised files in `images/work/posters/` and `.../thumbs/` (thumbnail about 640 px wide).
