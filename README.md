# Benstar Learning Hub — GitHub Pages starter

This is a proposed recreation, not an export or verified visual match. The current Google Site could not be inspected. Text, colours and structure are provisional. There are no external dependencies or build steps. No site has been deployed and no GitHub repository has been created.

## Files

- `index.html`: homepage and course cards
- `aa-sl.html`, `ai-sl.html`, `myp.html`: course pages with accessible expandable topics
- `about.html`: purpose and approach
- `assets/css/style.css`: all styling; edit colour variables at the beginning
- `assets/images/`: approved logo and images
- `assets/downloads/`: public, modest-sized PDFs
- `docs/`: migration inventory and instructions (not the website's publishing folder)
- `.nojekyll`: serves this as plain static files

## Preview and edit

Open `index.html` in a browser. Edit text with VS Code, save and refresh. HTML defines content; CSS defines appearance. No JavaScript is needed for the expandable topics.

Optionally run `python3 -m http.server 8000` from this folder and visit http://localhost:8000. This is only a local preview.

## Publish with GitHub Desktop (beginner route)

1. Unzip the starter. Install GitHub Desktop and sign in.
2. Choose File → New repository; name it `benstar-learning-hub` and choose its parent folder. Copy the contents of this starter into that repository, including `.nojekyll` and `.gitignore`. Avoid an extra nested starter folder.
3. Review files, write a summary such as `Add Benstar starter`, and select Commit to main. A commit is a saved checkpoint.
4. Publish repository. Review every included file before making the repository public. Public Pages hosting does not provide a private student area.
5. On GitHub open Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save.
6. Wait for the Pages deployment to finish. The expected project URL is `https://YOUR-USERNAME.github.io/benstar-learning-hub/`; GitHub will show the actual URL.
7. Test all pages and downloads on desktop and mobile. Every link is relative so it works under the repository subfolder.

Do not select `/docs` as the publishing source: this starter puts its site at the repository root. No Actions workflow is required for this approach.

## Optional command-line route

Create an EMPTY GitHub repository first; do not initialise it with README files. In this starter folder run these commands, replacing YOUR-USERNAME:

```sh
git init -b main
git add .
git commit -m "Add Benstar starter"
git remote add origin https://github.com/YOUR-USERNAME/benstar-learning-hub.git
git push -u origin main
```

Then configure Pages as above. Authenticate using GitHub's supported sign-in flow; never put a token in site files.

## Regular updates

Fetch/pull the latest changes, edit one small task, preview, then review the diff (the lines changed). Commit with a meaningful message and push (upload the commits). Publishing from main means each push updates the live website. For larger changes create a branch, a separate working version; use a pull request to review it before merging into main. To undo a bad published commit use Revert, then push; avoid rewriting shared history.

To add a PDF: place a public PDF at `assets/downloads/binomial-practice.pdf` and insert `<a href="assets/downloads/binomial-practice.pdf">Binomial practice (PDF)</a>` in the appropriate page. Replace “coming soon” only when the link works. To add a page, copy an existing HTML file and update the title, heading and navigation in EVERY page. This small amount of duplication is intentional for a beginner starter; move to a generator when it becomes burdensome.

No licence has been assigned to your teaching resources. Decide separately what visitors may reuse.

Read `docs/MIGRATION.md` before migrating content.
