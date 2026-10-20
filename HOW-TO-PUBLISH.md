# Publishing lizsites.com without Wix

The whole site is `index.html` plus an `images` folder; keep them together. It needs no build step, no database, and no monthly Wix plan.

## 1. Finish the content

Open `index.html` in any text editor and replace every yellow-highlighted placeholder (search for `class="ph"`):

- Manuscript titles, age ranges, word counts, and hooks (the "My Books" section)
- Status line ("Seeking representation" or whatever is accurate)
- School visit details (or delete that section)
- The public email address

When a placeholder is filled in, remove its `<span class="ph">…</span>` wrapper so the yellow highlight goes away.

**Photos:** the four photos live in the `images` folder. To swap one, replace the file with a new photo of the same name.


## 2. Host it free (pick one)

**Netlify (easiest):** go to app.netlify.com/drop, sign up, and drag the folder containing `index.html` onto the page. It goes live at a netlify.app address within seconds. To update later, drag the folder again.

**Cloudflare Pages:** dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets. Same drag-and-drop idea.

## 3. Move the lizsites.com domain

1. In Wix, check where the domain is registered (Settings → Domains).
2. **If Wix registered it:** either point it elsewhere by changing its DNS records, or transfer it to a registrar like Cloudflare or Porkbun (about $10–12/year). Transferring makes canceling Wix clean.
3. In Netlify (Domain settings → Add custom domain) or Cloudflare Pages (Custom domains), add `lizsites.com` and `www.lizsites.com`. Follow the DNS records they show you.
4. HTTPS is set up automatically. Once the new site loads on lizsites.com, cancel the Wix premium plan, but keep the domain registration active until any transfer finishes.

## 4. Turn on the newsletter (optional)

Sign up for Buttondown or Mailchimp (both have free tiers for small lists). Copy the form's action URL from their embed code and change the form tag to:

```html
<form class="news" action="https://buttondown.com/api/emails/embed-subscribe/YOURNAME" method="post">
```

Then delete the `news-form` submit handler at the bottom of the file (the block starting `var form = document.getElementById('news-form')`).

## 5. Once it's live

- Submit the site in Google Search Console so search results update from the old "Personal Details" title.
- Update the link in the Instagram bio if it points anywhere else.
