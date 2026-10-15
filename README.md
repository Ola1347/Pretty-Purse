# Pretty Purse

A Y2K-style expense tracker, earnings log and invoice maker. It is one web page with no build step and no server. Each person's data stays in their own browser.

## What is in this folder

| File | What it is |
| --- | --- |
| `index.html` | The whole app. This is the file you edit to change anything. |
| `manifest.webmanifest` | Lets people install Pretty Purse as an app. |
| `sw.js` | Lets the app open offline. |
| `netlify.toml` | Settings for Netlify. |
| `favicon.ico` | The tab icon. |
| `icons/` | Your PP logo in every size the browser and phones need, plus the picture shown when the link is shared. |

Upload **all** of these, including the `icons` folder.

## Step 1: Put it on GitHub

1. Go to github.com, click **New repository**, name it `pretty-purse`, and click **Create repository**.
2. On the new repository page, click **uploading an existing file**.
3. Unzip the download, then drag **everything inside the folder** into the page: `index.html`, `manifest.webmanifest`, `sw.js`, `netlify.toml`, `favicon.ico`, `README.md` and the `icons` folder.
4. Click **Commit changes**.

Check that `index.html` is in the top level of the repository and not inside another folder.

## Step 2: Put it on Netlify

1. Go to app.netlify.com and sign in (you can use your GitHub login).
2. Click **Add new site**, then **Import an existing project**, then **GitHub**, and pick `pretty-purse`.
3. Leave **Build command** empty. Set **Publish directory** to `.` (a single dot). `netlify.toml` already says this.
4. Click **Deploy**. In about a minute you get a link ending in `netlify.app`.

## Step 3: Choose your final web address now

In Netlify, open **Site configuration**, then **Change site name**, and pick something like `prettypurse`. Your address becomes `prettypurse.netlify.app`.

Decide this before you share the link. People's saved expenses and invoices are tied to the exact web address. If the address changes later, they will open an empty app and their history will look gone. They can bring it back with the Backup and Restore buttons on the History page. If you want your own domain (for example `prettypurse.com`), add it under **Domain management** now, before sharing.

## Step 4: Fix the link preview

Open `index.html` on GitHub (click the file, then the pencil icon). Near the top, replace both `https://YOUR-SITE.netlify.app` with your real address, then click **Commit changes**. This makes the PP picture show when your link is shared on WhatsApp, X and similar apps.

## Step 5: Test it

1. Open your link. You should see the PP icon in the browser tab and the welcome screen.
2. In Chrome or Edge, click **Install app** at the top of the page, or the install icon in the address bar.
3. Add an expense, issue an invoice, and click **Download PDF**. Open the file and check it.
4. Press **Test voice** on the Profile & Style page.
5. Open the link on a phone.

## Updating later

Change a file on GitHub (open it, click the pencil, edit, commit). Netlify redeploys on its own within a minute.

## Things to know

- The PDF library and fonts load from the internet the first time. After that the app can open offline.
- There are no accounts. A person's data lives only in their browser. Clearing browser data, or switching device, loses it unless they saved a backup.
- If you later collect emails or add accounts, add a privacy note first.
