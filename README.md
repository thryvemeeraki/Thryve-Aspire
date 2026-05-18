# Thryve Aspire Form

Static deployment package for the Thryve Aspire assessment form.

## Test On GitHub Pages

1. Create a GitHub repository, for example `thryve-aspire-form`.
2. Upload these files from this folder:
   - `index.html`
   - `.nojekyll`
   - `netlify.toml`
   - `README.md`
3. In GitHub, open `Settings > Pages`.
4. Set source to `Deploy from a branch`.
5. Select branch `main` and folder `/root`.
6. Save and wait for GitHub Pages to publish.
7. Open the published GitHub Pages URL.
8. Generate a test student link from the counsellor dashboard.
9. Open the generated student link and submit a test response.
10. Check the Google Sheet and admin/student email inboxes.

## Deploy Final Version To Netlify

1. In Netlify, choose `Add new site > Import an existing project`.
2. Connect the same GitHub repository.
3. Build command: leave blank.
4. Publish directory: `.`
5. Deploy.
6. Open the Netlify URL and generate new student links from the Netlify version.

## Important

- Generate final student links only from the final hosted URL.
- If the Google Apps Script is edited, deploy a new Apps Script web app version and update `APPS_SCRIPT_URL` inside `index.html` if Google gives you a new `/exec` URL.
- The form uses Google Apps Script in `no-cors` mode so static hosting on GitHub Pages or Netlify can submit responses without browser CORS blocking.
