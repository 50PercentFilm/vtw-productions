# VTW Productions

Website and brand kit for VTW Productions (Valerie & Tom Webster Productions). Domain: vtw-productions.com

- `index.html` is the website (single file, no build step)
- `brand-kit/index.html` is the brand kit and business brief

## Put it on GitHub
```
git init
git add .
git commit -m "VTW Productions website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/vtw-productions.git
git push -u origin main
```
(Create an empty repo called vtw-productions on github.com first, without a README.)

## Deploy on Netlify
- Drag this folder onto the project's Deploys tab, or link the GitHub repo (no build command, publish directory `/`).
- Every push to `main` then redeploys automatically.

## Connect vtw-productions.com
1. Netlify > your project > Domain management > Add a domain > vtw-productions.com.
2. At your registrar's DNS settings add:
   - A record, host `@`, value `75.2.60.5`
   - CNAME record, host `www`, value `YOUR-SITE-NAME.netlify.app`
   (or use ALIAS/ANAME `@` to `apex-loadbalancer.netlify.com` if your registrar supports it)
3. Back in Netlify, click Verify DNS, then Provision certificate (free HTTPS). Propagation can take up to 48 hours.
4. Optional: set www.vtw-productions.com as the primary domain.

## Email
hello@vtw-productions.com needs an inbox: use Google Workspace, Zoho Mail or your registrar's email forwarding, and add the MX records they give you.

Note: Clue is subject to licensing (Concord Theatricals). Dates and prices for Clue are placeholders.

## Security
- `_headers` adds HTTPS-only (HSTS), a content security policy, clickjacking protection and other standard headers. Keep it in the folder you deploy.
- Netlify provides the free HTTPS certificate. For vtw-productions.com it appears after the DNS records are verified (see above).
