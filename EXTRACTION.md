# Smart Autoscaling extraction

Source deployment: https://smart-autoscaling-dashboard--leodasandco11.replit.app

This folder contains a runnable copy of the public browser entrypoint. The deployment exposes the compiled Vite assets:

- `assets/index-C7jLUdhq.js` - compiled client bundle
- `assets/index-C7qhsiaH.css` - compiled stylesheet
- `assets/favicon.svg` - favicon
- `index.html` - local entrypoint wired to those assets

The original React source, package files, server code, and configuration are not exposed by the deployed app. The source-map URL was checked and returned the deployment HTML shell rather than a map.

To populate the asset files from the deployment:

```sh
curl -L 'https://smart-autoscaling-dashboard--leodasandco11.replit.app/assets/index-C7jLUdhq.js' -o assets/index-C7jLUdhq.js
curl -L 'https://smart-autoscaling-dashboard--leodasandco11.replit.app/assets/index-C7qhsiaH.css' -o assets/index-C7qhsiaH.css
curl -L 'https://smart-autoscaling-dashboard--leodasandco11.replit.app/favicon.svg' -o assets/favicon.svg
```

Serve this directory over HTTP, for example with `python3 -m http.server 8000`, then open `http://localhost:8000`.
