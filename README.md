# Medinote prototype

Static HTML and JavaScript demo for Medinote / IPMS OPD.

## Publish with GitHub Pages

1. Create a GitHub repository.
2. Push this folder to the repository root, including the `assets/` folder and the hidden `.nojekyll` file:

   ```sh
   git init
   git add .
   git commit -m "Medinote prototype"
   git branch -M main
   git remote add origin https://github.com/USERNAME/REPOSITORY.git
   git push -u origin main
   ```

3. Open **Settings > Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select your branch (usually **main**) and **/(root)**, then save.
6. Wait for the Pages deployment to finish. The Pages settings screen will show the published link, usually `https://USERNAME.github.io/REPOSITORY/`.

`index.html` opens `Prototype Index.dc.html`. Keep the original filenames and folder structure: navigation uses relative links so the demo works within a repository subdirectory.

The `.nojekyll` file disables Jekyll processing so the prototype's `{{ ... }}` template expressions are served unchanged.

## Preview locally

From this folder, run:

```sh
python -m http.server 8000
```

Open `http://localhost:8000/`. Use an HTTP server because the runtime fetches page content and the mobile JSX component.

## Runtime dependencies

The runtime downloads React, React DOM and Babel from unpkg, and fonts from Google Fonts. Visitors need internet access to these services.

This is a demonstration using fictional data and browser storage. GitHub Pages supplies static hosting; production authentication, shared persistent data and server operations require a separate backend.
