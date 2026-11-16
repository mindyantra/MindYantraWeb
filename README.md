# Mind Yantra Solutions website

A responsive static website. It has no build step or runtime dependencies, so the same files can be previewed locally and deployed to static hosting.

## Project structure

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   ├── images/
│   │   └── mind_yantra_logo.png
│   └── js/
│       └── script.js
└── readme.md
```

- `index.html` contains the page structure and content.
- `assets/css/styles.css` contains layout, theme and responsive styles.
- `assets/js/script.js` contains mobile navigation, the copyright year and email-enquiry behavior.
- `assets/images/` contains the logo used by the page.

Keep the homepage at the project root for straightforward static hosting. Put new images, stylesheets and scripts in their corresponding `assets/` directories, and update their paths in `index.html`.

## Preview locally

From the project root, run:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`. You can also use a local static-site preview extension in your editor.

## Deploy with GitHub Pages

1. Push the project files and `assets/` folder to the root of a GitHub repository.
2. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and the `/(root)` folder, then save.
3. Wait for the Pages deployment to finish and open the URL shown in the Pages settings.
4. For a custom domain, configure it in Pages settings and follow GitHub's current DNS instructions. Add the corresponding `CNAME` file at the repository root only after confirming the domain to use. Do not change email-related DNS records.

See GitHub's current guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Before publishing

- Confirm the contact email and business details in `index.html`.
- Review all course, service and placement-related claims.
- The enquiry form opens the visitor's email application; this site does not store or submit enquiries to a server. Use a form service or backend if stored submissions are required.
- Check that the deployed site loads the logo, styles and script, including on mobile.
