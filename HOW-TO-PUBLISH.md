# Publishing lizsites.com without Wix

The whole site is `index.html` plus an `images` folder; keep them together. It needs no build step, no database, and no monthly Wix plan.

## 1. Content

All text and photos are filled in. To change wording, open `index.html` in any text editor.

**Photos:** the four photos live in the `images` folder. To swap one, replace the file with a new photo of the same name.


## 2. Host it free (pick one)

**Netlify (easiest):** go to app.netlify.com/drop, sign up, and drag the folder containing `index.html` onto the page. It goes live at a netlify.app address within seconds. To update later, drag the folder again.

**Cloudflare Pages:** dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets. Same drag-and-drop idea.

## 3. Move the lizsites.com domain

1. In Wix, check where the domain is registered (Settings → Domains).
2. **If Wix registered it:** either point it elsewhere by changing its DNS records, or transfer it to a registrar like Cloudflare or Porkbun (about $10–12/year). Transferring makes canceling Wix clean.
3. In Netlify (Domain settings → Add custom domain) or Cloudflare Pages (Custom domains), add `lizsites.com` and `www.lizsites.com`. Follow the DNS records they show you.
4. HTTPS is set up automatically. Once the new site loads on lizsites.com, cancel the Wix premium plan, but keep the domain registration active until any transfer finishes.

## 4. Adding a newsletter later

The site has no sign-up form for now. When Liz wants one, Buttondown and Mailchimp both offer a free tier and an embed form that can go in the Get In Touch section.

## 5. Once it's live

- Submit the site in Google Search Console so search results update from the old "Personal Details" title.
- Update the link in the Instagram bio if it points anywhere else.
