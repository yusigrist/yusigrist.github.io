Static site for a browser-based LLM demo

This repository is a static website. To run it locally and test the `context.txt` loading behavior, serve the folder with a static HTTP server.

Quick local test (Python 3):

```bash
cd /path/to/repo
python3 -m http.server 8000
# open http://localhost:8000 in your browser
```

Notes
- Opening `index.html` via the file:// protocol may prevent `fetch('./context.txt')` from working in some browsers. Use a static server as shown above or deploy to GitHub Pages.
- The page attempts to fetch `context.txt` at the root of this folder. Edit that file to change the assistant context.

Deploy to GitHub Pages
- Push the repository to GitHub and enable Pages from the `main` branch (root). GitHub Pages will serve the site as static files.

If you'd like, I can also:
- Add a small admin UI to edit the context in-browser (client-side only), or
- Add a GitHub Actions workflow to automatically publish to GitHub Pages on push.
