# CXaiS Bench &amp; Staffing Planner

A single self-contained HTML app — the bench skills matrix, role JDs, project staffing, exports, and the consultant self-assessment flow. No build step, no dependencies, no server.

## Deploy on GitHub Pages

1. Create a new GitHub repository (public or private).
2. Upload **`index.html`** and **`.nojekyll`** to the repository root.
3. In the repo: **Settings → Pages → Build and deployment**.
4. Set **Source** to *Deploy from a branch*, branch **`main`**, folder **`/ (root)`**, then **Save**.
5. Wait ~1 minute. Your app is live at:

   ```
   https://<your-username>.github.io/<repo-name>/
   ```

## The self-assessment links

Once live, the links work in any browser with no token:

- **Invite a consultant** — open the app → **People** tab → *Copy link* (this is `…/#onboard`). Send it to the consultant.
- **They complete it** on their own device and get a **submission link** (`…/#review=…`) to send back to Rachel.
- **You import it** — open their link → *Add to bench as pending* → confirm in the 1-2-1.

> The links are built from whatever URL the app is served at, so they only work once the app is hosted at a public address (this is why the editor-preview link asked for a token).

## Data &amp; privacy

All data is stored locally in each browser (`localStorage`) — nothing is sent to a server. A consultant's submission travels only inside the link they send back. There is no shared database; importing a submission link is what brings their data onto your bench.

## Updating

This `index.html` is a compiled bundle. To change the app, edit the source `CXaiS Bench Planner.dc.html`, re-export the standalone build, and replace `index.html`.
