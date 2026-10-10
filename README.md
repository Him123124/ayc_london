# AYC London Boutique website

Hijabs and abayas, 114 High Rd, Leyton.

## Put it online with GitHub Pages (free)
1. Create a new repository on GitHub and upload everything in this folder (drag the files in, keep the folders).
2. In the repository go to **Settings > Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, choose branch **main** and folder **/ (root)**, then Save.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

The files in the root (`index.html`, `shop.html`, `visit.html`, `static/`) are the live site. GitHub Pages has no server, so the bag and contact form finish on WhatsApp.

## Edit the content
Easiest: edit `flask-app/data/products.json` and `flask-app/data/site.json`, then run `python flask-app/freeze.py` (needs `pip install flask`) and upload the updated root files.

Prices, sizes and product descriptions are placeholders. Replace them before launch.

## Full version with saved orders (`flask-app/`)
```
cd flask-app
pip install -r requirements.txt
ADMIN_PASSWORD=choose-a-password SECRET_KEY=long-random-text python app.py
```
Orders and messages are saved to a database and shown at `/admin`. This needs Python hosting (Render, PythonAnywhere, Railway), not GitHub Pages.
