# COG Qatar — Wi-Fi Landing Page

A single-file, static landing page shown when someone scans the **"Scan to Connect to Church Wi-Fi"** QR code around the church. It acknowledges the Wi-Fi moment, then invites the visitor into worship, fellowship, youth gatherings and other church activities.

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Point the Wi-Fi QR code (or captive-portal redirect) at the resulting URL.

No build step, no dependencies to install. Tailwind CSS and the fonts load from CDN; everything else is inline.

## Editing

| What | Where in `index.html` |
| --- | --- |
| Hero headlines (one is chosen at random per page load) | the `HEADLINES` array in the small script just below the `<h1>` |
| Quick-link chips under "While you're here…" | `WHILE YOU'RE HERE` section — replace each `href` with a real page, WhatsApp, or Maps link |
| Activity cards | `FIND YOUR PLACE` section — six `<a>` cards, each with its own `id` the chips link to |
| Rotating inspirational lines | the `lines` array in the script at the bottom |
| Bible verse | `FEATURED VERSE` section |
| Colours and fonts | the `tailwind.config` block in `<head>` |

## Notes

- Mobile-first; the first viewport holds the connection indicator, headline, supporting line and primary CTA.
- All motion is CSS-based and disabled under `prefers-reduced-motion`.
- No images are required — the atmosphere is pure CSS gradients, so the page looks right even on a slow or partially blocked connection.
- For rich link previews when the URL is shared, add a 1200×630 `og-image.jpg` beside `index.html`.
