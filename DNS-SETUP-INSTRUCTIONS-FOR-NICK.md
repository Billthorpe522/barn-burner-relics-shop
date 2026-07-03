# DNS Setup for shop.barnburnerrelics.net — for Nick

## What I need from you (Nick) — 5 minutes

The catalog site is built and ready to go. It's sitting on GitHub waiting for `shop.barnburnerrelics.net` to point at it. You're the one with the Squarespace account, so only you can do this.

### Step 1: Open Squarespace DNS settings
1. Log into Squarespace (the account that owns `barnburnerrelics.net`)
2. Go to **Settings → Domains → barnburnerrelics.net → DNS Settings**
   (Or for newer Squarespace UI: **Domains → barnburnerrelics.net → Advanced → DNS**)
3. Look for the **Custom Records** section

### Step 2: Add ONE CNAME record
Click "Add Record" and enter:

| Field         | Value                          |
|---------------|--------------------------------|
| Type          | CNAME                          |
| Host          | `shop`                         |
| Points To     | `billthorpe522.github.io`      |
| TTL           | 3600 (or default)              |

That's it. Save.

### Step 3: Wait
- DNS propagation: 5 min to 1 hour (usually fast)
- GitHub Pages will detect the CNAME and provision an SSL cert automatically (5-15 min after DNS resolves)
- The site will appear at **https://shop.barnburnerrelics.net**

### Step 4: Add a button on your front page
In the Squarespace page editor:
1. Edit your homepage
2. Add a **Button** block (near the "CONTACT US" button, or wherever you want it)
3. Button text: **"View Current Inventory"**
4. Button link: **https://shop.barnburnerrelics.net**
5. Open in new tab: ON (recommended)
6. Style to match your existing button (dark background, light text)

### What you'll see
- Clicking the button takes visitors from your marketing Squarespace page to the catalog site
- The catalog has a "← Main Site" link in the header that brings them back to your Squarespace home

### If something breaks
- If `shop.barnburnerrelics.net` doesn't load after an hour: text me — probably the CNAME has a typo or GitHub is still provisioning SSL
- If you want to change the subdomain from `shop` to `sales` or `catalog` later: just rename the CNAME record in Squarespace (and tell me so I can update the GitHub side)

— Bill (via Hermes)

