# Alfa Mind Hub — setup guide

This folder is your whole website, plus a free admin panel at `/admin` where
you can add coloring pages, upload PDFs, and edit the homepage text yourself —
no coding needed after today.

It's built to run on **Netlify** (free) with **Decap CMS** (free) as the admin
panel. Here's how to get it live, in order. It looks long but each step is
quick — budget about 15–20 minutes total.

## 1. Put this folder on GitHub (free)

1. Go to github.com and create a free account if you don't have one.
2. Click **New repository**. Name it something like `alfa-mind-hub`. Keep it
   **Public**. Create it.
3. On the new repo's page, click **uploading an existing file** and drag in
   everything from this folder (keep the folder structure — `admin/`,
   `content/`, `uploads/`, `index.html`, `netlify.toml`).
4. Commit the files.

## 2. Connect it to Netlify (free)

1. Go to netlify.com and sign up (you can sign up with your GitHub account —
   this makes step 3 easier).
2. Click **Add new site → Import an existing project**.
3. Choose GitHub, then pick the `alfa-mind-hub` repo you just created.
4. Leave the build settings as they are (there's nothing to build) and click
   **Deploy**.
5. Netlify gives you a free web address like `random-name-123.netlify.app`.
   You can change this: **Site configuration → Change site name**.

## 3. Turn on the admin login (free)

1. In your Netlify site dashboard, go to **Site configuration → Identity**
   and click **Enable Identity**.
2. Under Identity settings, set **Registration** to **Invite only** (so
   strangers can't sign up to your admin panel).
3. Scroll to **Services → Git Gateway** and click **Enable Git Gateway**.
   This is what lets the admin panel save your changes back to GitHub.
4. Go to the **Identity** tab and click **Invite users**. Invite your own
   email address.
5. Check your email, click the invite link, and set a password.

## 4. Log in and start editing

1. Visit `your-site-name.netlify.app/admin`.
2. Log in with the email and password from step 3.
3. You'll see two sections:
   - **Coloring Pages** — add a new design, upload its thumbnail photo and
     its PDF, set a price (or leave blank while you're not selling yet),
     and choose a card color.
   - **Site Text** — edit the homepage headline, subtitle, and about text.
4. Click **Publish** after any change. It updates your live site within a
   minute or two.

## A few things worth knowing

- **Don't just double-click `index.html` to preview it** — the product
  gallery loads its content from `content/products.json`, which only works
  when the site is actually served by Netlify (or any web server). Opening
  the raw file will show the one sample design as a fallback, but not your
  admin edits.
- Everything here is **free** — GitHub, Netlify's free tier, and Decap CMS
  don't cost anything at this scale. If your site later gets serious traffic
  (well beyond a small shop), Netlify's free bandwidth allowance is 100GB/month,
  which is worth knowing about but unlikely to matter early on.
- This site doesn't process payments — it's a showcase with free-sample
  downloads for now. When you're ready to actually sell, the cleanest low-cost
  option is linking each "Buy" button to a listing on **Etsy** or **Gumroad**,
  which I can wire up any time you have that link.
- If anything in these steps doesn't match what you see on GitHub or Netlify,
  just paste me a screenshot or describe what's on your screen and I'll walk
  you through it.
