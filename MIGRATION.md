# Review and migration plan

## Review still needed

Share the current published Google Site URL. If it is inaccessible or draft-only, provide desktop/mobile screenshots of Home and one course page, the navigation list, and an example expanded topic. Do not share passwords. Earlier URLs could not be retrieved, so the starter is not a current-site audit.

## Extract and convert

1. Record every page and nested page in content-inventory.csv. Record headings, text, buttons, original URLs, file locations and embedded tools. Mark keep/revise/archive.
2. Use Google Takeout's applicable Drive/Sites export as a backup where available. Inspect its actual contents; an export is not a guaranteed deployable replica. Save your own embedded HTML snippets separately.
3. Copy approved text into semantic HTML: header, navigation, main, sections, headings and footer. Rebuild layout with clean CSS rather than relying on Google's generated DOM/classes/scripts.
4. Obtain original logo/photos and record usage rights. Use descriptive lowercase filenames and meaningful image alt text; compress large images. Do not assume an image's Google delivery URL is a durable asset URL.
5. Download public PDFs or keep reviewed Drive links. Large/changing files can stay in Drive. Check sharing in a signed-out browser. Repository history retains old file versions, so avoid repeatedly committing large videos/PDFs.
6. Keep YouTube videos as embeds or links. Keep Google Forms hosted by Google; rebuilding a form's appearance does not preserve response collection. Recheck each embedded item and its access settings. Never copy student response data into the repo.
7. Recreate Sheets/Docs/Slides embeds only if appropriate for public visitors. An iframe is a window showing another hosted page; its sharing remains controlled by that service. Add a descriptive title and a normal fallback link. Use the service's own supported embed code and verify it on mobile.
8. Recreate custom embedded HTML directly when source is available and compatible. Scripts tied to Google authentication or another backend require separate work. A static GitHub Pages site cannot supply a private login, database or server-side form handler by itself.
9. Reconfigure analytics intentionally; it will not transfer just because the page looks the same. Preserve original page titles and map old URLs to new ones. You generally cannot configure server redirects for a sites.google.com address; keep the old site with prominent links to the new location during transition.
10. Check every link, download, keyboard focus, mobile layout, embed permission and heading order. Replace sample copy and resources. Launch only after the inventory is complete.

## Architecture choices

- Plain HTML/CSS (this starter): best first step for a small hub; no build tooling. Shared navigation is manually maintained.
- Jekyll: useful when many resources/posts need shared layouts; supports Markdown (simple text with headings and links) and integrates with Pages. Adds templates and configuration.
- Hugo: useful for larger structured collections and fast generated sites; adds a local binary and usually an Actions deployment workflow. More setup than this hub needs initially.

A static site generator turns content and reusable templates into ordinary website files. Move to Jekyll when editing duplicate navigation or many resource pages becomes the main burden. Keep original resource links and filenames organised so that migration stays straightforward.

## Sources

- https://support.google.com/sites/answer/9759608
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
