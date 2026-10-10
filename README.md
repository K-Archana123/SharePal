# SharePal – Gaming Gadgets on Rent (Bangalore)

A recreation of https://sharepal.in/bangalore/gaming-gadgets-on-rent built as a static site (HTML, CSS and vanilla JavaScript, no build step or dependencies).

- **Live URL:** https://k-archana123.github.io/SharePal/
- **Source:** this repository

## Run locally
Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy
Push to GitHub, then Settings → Pages → deploy from the `main` branch (root). It also works on Netlify or Vercel as a static site.

## Files
| File | Purpose |
|---|---|
| `index.html` | The full page (markup, styles, scripts). Product data is embedded, so no server or fetch is needed. |
| `product-list.json` | The supplied product data (kept for reference). |

## What is recreated
- Purple header with the logo tab, city / Delivery Date / Pickup Date / Select pill, search, cart and login
- Category tabs (Photography, Gaming, Outdoor, Entertainment)
- Sidebar of sub-categories (All, Handheld, GTA VI, PS5 Console, Xbox Console)
- Gaming Consoles banner, "Total items" heading and responsive product grid
- Product cards: tag pills (New, Trending, Vote to Launch), rating, booked count, per-day rent, out-of-stock state, and the "Launching at 1k votes" note
- Dark navy SEO and footer section with Read More, five link columns, Go up, copyright line, sticky "Select rental dates" button and chat bubble
- Hover lift and image zoom on cards, staggered fade-in, floating banner images, toasts, and reduced-motion support

## My improvements
1. **Date-aware pricing:** choosing delivery and pickup dates updates every card with the total for that rental length, and the sticky button reflects the selection. "Rent now" prompts for dates first so users never rent blind.
2. **Search, sort and filters:** live search, sort (most booked, price, rating) and an "In stock only" toggle.
3. **Wishlist:** a heart on every card, saved in the browser.
4. **Notify me:** out-of-stock items offer a "Notify me" action instead of a dead end.
5. **Vote to Launch:** voting works, updates the count and remembers the vote.
6. **Empty states:** categories with no products (GTA VI, Xbox) show a friendly message rather than a blank page.
7. **Skeleton and fallbacks:** a loading shimmer while images load, and a placeholder if one fails.
8. **Mobile layout:** sidebar becomes a horizontal scroller, the grid becomes two columns, and the date pill becomes a sticky bottom button.
9. **Accessibility:** labelled controls, alt text on images, focus rings and `prefers-reduced-motion`.

## Known limitations and assumptions
- I could not inspect the live site's exact CSS, so colors, spacing and the Inter font were matched visually from screenshots.
- Banner artwork is built from the supplied product photos, and the brand marks (Xbox, PS5, Meta) are text. Sidebar icons for All, GTA VI and Xbox are placeholders. The original assets were not available.
- Cart, login, the city selector and the other category tabs are visual only.
- Product images load from `images.sharepal.in`, so an internet connection is needed.
- Wishlist, votes and notify choices are stored in `localStorage`, not on a server.
