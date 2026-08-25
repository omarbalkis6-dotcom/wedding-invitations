# Getting these online at your own domain

You need two things: a **host** (free) and a **domain** (about $10 a year). They
are bought separately, then pointed at each other.

---

## Step 1 — Buy the domain

Register at **Cloudflare Registrar**, **Porkbun**, or **Namecheap**. Cloudflare
sells at wholesale price with no markup and no first-year-cheap-then-expensive
trick, so it is usually the best value.

Some name ideas for selling wedding invitation sites:

| Style | Examples |
| --- | --- |
| English | `invitely.co` · `thevowsite.com` · `paperandvow.com` |
| Arabic-friendly | `zaffa.studio` · `daawa.co` · `farah.cards` · `zawaj.site` |
| Personal brand | `omarstudio.com` · `omar.design` |

Prefer `.com` if you can get it — it still signals "real business" to buyers
more than anything else. `.co`, `.studio`, `.design` and `.cards` are good
second choices and often available.

Avoid hyphens and creative misspellings; you will be reading this domain aloud
to customers.

---

## Step 2 — Put the site on a host

### Option A — Cloudflare Pages (best if you bought the domain at Cloudflare)

1. <https://pages.cloudflare.com> → **Create a project** → **Upload assets**
2. Drag the whole `wedding-websites-for-sale` folder in
3. Give the project a name → **Deploy**
4. **Custom domains** tab → **Set up a domain** → type your domain → **Activate**

If the domain is registered at Cloudflare, the DNS records are created for you
and HTTPS turns on within a minute. Nothing to configure by hand.

### Option B — Netlify (best if you bought the domain elsewhere)

1. <https://app.netlify.com/drop> → drag the folder in → you get a live URL
2. Sign up free to keep it
3. **Domain management** → **Add a domain you already own** → enter it
4. Netlify shows you the DNS records to create at your registrar

---

## Step 3 — Point the domain at the host

At your registrar's DNS page, create these two records. Replace
`your-project.pages.dev` (Cloudflare) or `your-site.netlify.app` (Netlify) with
what your host actually gave you.

| Type | Name | Value |
| --- | --- | --- |
| CNAME | `www` | `your-project.pages.dev` |
| CNAME (or ALIAS/ANAME) | `@` | `your-project.pages.dev` |

Notes:

- The `@` record means the bare domain (`yourdomain.com` with no `www`). Plain
  DNS does not allow CNAME on `@`, so registrars offer **ALIAS** or **ANAME**
  instead — Cloudflare, Netlify DNS and Porkbun all support it. If yours does
  not, use the A records your host lists instead.
- **Netlify's A record** for the bare domain is `75.2.60.5`. Cloudflare Pages
  handles the bare domain automatically when the domain is on Cloudflare.
- DNS changes take anywhere from two minutes to a few hours. If it does not work
  immediately, wait before changing anything — repeatedly editing records is the
  usual cause of a long outage.
- **HTTPS is automatic and free** on both hosts. Never pay for an SSL
  certificate for this.

---

## Step 4 — Check it worked

Once live, confirm all four pages:

- `https://yourdomain.com/` — the showcase
- `https://yourdomain.com/midnight-gold/`
- `https://yourdomain.com/blush-heart/`
- `https://yourdomain.com/arabic-arch/`

Then open the showcase on an actual phone. These are mobile-first designs and
the phone is where every one of your customers will see them.

---

## Selling from that domain

**Give each client their own link.** The cleanest model is one folder per
couple:

```
yourdomain.com/aya-ahmad/
yourdomain.com/sara-omar/
```

Copy a design's `index.html` into a new folder, change the `CONFIG` block and
the names, re-upload. Each couple gets a private-feeling link, and you keep the
showcase at the root for new customers.

**Per-guest personalisation** is your differentiator — most competitors do not
have it. Any link accepts a guest name:

```
yourdomain.com/aya-ahmad/?to=أبو%20خالد
```

The invitation then greets that guest by name. A couple can send 200 links, each
one personal.

**What to charge.** Custom wedding invitation sites like these commonly sell for
$50–$250 depending on how much you personalise. Bundle a few revisions and the
guest-link generation, and you are at the upper end.

**Before selling, read the photo licensing section** in
`HOW-TO-PUBLISH-AND-SELL.md`. Short version: the code and fonts are free to
sell; the Unsplash photographs are fine on your demo but should be replaced with
the client's own photos in anything you deliver or package.

---

## Files in this folder that the host uses

| File | What it does |
| --- | --- |
| `index.html` | the showcase page |
| `404.html` | styled "page not found", served automatically |
| `_headers` | security and caching rules (Netlify and Cloudflare both read it) |
| `robots.txt` | lets search engines index the site |

Ask me when you have picked a domain and I will check what needs changing.
