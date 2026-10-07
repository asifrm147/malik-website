# Opening the portal

While the portal (app.asifmalikmd.com) isn't ready, the website's **Book**,
**Send a review request**, **Open a case** and **Sign in** buttons go to
`/book`, `/request` and `/sign-in`, which show the `opening-soon` page
(email asif.malik@psychiatrygroup.com, no medical details by email).

When the portal is live and taking real payments, replace the `"rewrites"`
block in **both** `vercel.json` and `website/vercel.json` with:

```json
"redirects": [
  { "source": "/book", "destination": "https://app.asifmalikmd.com/book", "permanent": false },
  { "source": "/request", "destination": "https://app.asifmalikmd.com/login", "permanent": false },
  { "source": "/sign-in", "destination": "https://app.asifmalikmd.com/login", "permanent": false },
  { "source": "/login", "destination": "https://app.asifmalikmd.com/login", "permanent": false }
]
```

Then change the "Contact" line in `website/index.html` back to the portal.
