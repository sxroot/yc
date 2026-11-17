# YOUR CHOICE — PHASE 01: Storefront Page Inventory & Implementation Status

**Brand Reference:** YOUR CHOICE® (`Always The Best Choice` · `Independent by Design`)  
**Design Tokens:** `--paper` (`#f5f5f1`), `--ink` (`#18191a`), `--blue` (`#2349ed`), `--cyan` (`#57dbf3`), `--obsidian` (`#121416`)  
**Typography:** `Barlow Condensed` (Display) · `DM Sans` (Editorial UI) · `IBM Plex Mono` (Technical Specs & Metadata)  
**Scope:** Frontend UI/UX Only (`localStorage`-persisted bag, wishlist, member profile & order state)

---

## Complete 24-Page Storefront Matrix

| # | Page Name | Canonical Route | Aliases | Status | Key UI/UX Features & Interactions |
|---|---|---|---|:---:|---|
| 00 | **Homepage (Design Reference)** | `/` | — | ✅ Complete | Preserves original hero (`NOT FOR EVERYONE. FOR YOU.`), manifesto ticker, collection filter grid, scroll-driven Expression Orbit, 12-strip Editorial Shutter story, horizontal scroll Rail, Design Studio & Newsletter |
| 01 | **Shop / All Products** | `/shop` | `/products` | ✅ Complete | Collapsible filter sidebar (keyword, colorway swatches, size chips, silhouette block, price tier), category tabs, sorting, 2/3/4-column grid density toggle, empty filter recovery & Fit Finder CTA |
| 02 | **T-Shirt Collection** | `/collections/t-shirts` | `/t-shirts` | ✅ Complete | Dedicated editorial campaign hero, 4-cell jersey spec ribbon (295–320 GSM), silhouette sub-filters (`Boxy`, `Mock-Neck`, `Oversized`, `Long-Sleeve`), size filter, sorting & block comparison cards |
| 03 | **Polo Shirt Collection** | `/collections/polo-shirts` | `/polo-shirts` | ✅ Complete | Dedicated campaign hero, piqué/knit spec ribbon, sub-style filters (`Heavy Piqué`, `Johnny Open-Collar`, `Half-Zip Knit`, `Long-Sleeve Rugby`), sorting & collar architecture editorial story |
| 04 | **Collection Details** | `/collections/:slug` | `/collections`, `/collection-details` | ✅ Complete | Supports `expression-vol-01`, `t-shirts`, `polo-shirts`, `outerwear-forms`; capsule switcher bar, campaign banner, spec matrix, curatorial essay, capsule product grid & next-chapter cards |
| 05 | **Product Details** | `/product/:slug` | `/product`, `/product-details` | ✅ Complete | 4-frame interactive studio/macro/editorial gallery + fullscreen zoom modal, colorway variant switcher, size selector with low-stock indicator, Size Guide modal trigger, quantity, Add to Bag, Express Buy Now, Wishlist toggle, 4 accordions & outfit cross-sell |
| 06 | **Search Results** | `/search` | `/search?q=...` | ✅ Complete | URL-synced live search input, trending query chips, scoped tabs (`All`, `Products`, `Collections`, `Care & FAQ`), category/price sorting & zero-results recovery |
| 07 | **Wishlist** | `/wishlist` | — | ✅ Complete | Persisted curation board, inline per-card size picker + `Move to Bag`, `Add All to Bag`, shareable link copy, clear/restore sample state & empty state |
| 08 | **Shopping Bag** | `/bag` | `/cart`, `/shopping-bag` | ✅ Complete | Free Express Delivery progress meter ($150), inline size switcher, quantity controls, Save to Wishlist, Rigid Collector Box (+$8) + custom gift note, working promo codes (`YC10`, `INDEPENDENT`, `FREESHIP`) & sticky order summary |
| 09 | **Checkout** | `/checkout` | — | ✅ Complete | 3-part structured checkout (Contact, Shipping Address & Courier Tier, Payment Method: Card / Apple Pay / Klarna 4x / COD), sticky manifest summary, validation & live client-side Order creation |
| 10 | **Order Confirmation** | `/order-confirmation/:orderId` | `/order-confirmation` | ✅ Complete | Obsidian header with Official Winged Crest, copyable `YC-2026-XXXX` order reference, garment manifest, delivery & payment breakdown, Print Receipt (`window.print()`) & direct Track Order CTA |
| 11 | **Order Tracking** | `/order-tracking` | `/track-order` | ✅ Complete | Order # + email lookup, 1-click sample/recent order pills (`In Transit`, `Out for Delivery`, `Delivered`), 5-stage visual milestone stepper, route summary & chronological carrier scan log |
| 12 | **Login** | `/login` | — | ✅ Complete | Split-screen editorial auth with Official Logo Lockup, show/hide password, 1-click demo member sign-in, plus interactive **Member Profile Dashboard** when signed in |
| 13 | **Registration** | `/register` | `/registration` | ✅ Complete | Split-screen Inner Circle registration, live 4-bar password strength indicator, wardrobe silhouette preference selector & instant session activation |
| 14 | **Forgot Password** | `/forgot-password` | — | ✅ Complete | Email recovery request form, dispatch confirmation screen & 1-click simulated reset token link |
| 15 | **Reset Password** | `/reset-password` | — | ✅ Complete | Verified recovery token state, live 4-rule security checklist & password updated confirmation |
| 16 | **About** | `/about` | — | ✅ Complete | Official YOUR CHOICE Winged Emblem & Monogram anatomy showcase, Three Pillars (`Design It · Wear It · Earn From It`), GOTS organic craft standards & studio metrics |
| 17 | **Contact** | `/contact` | — | ✅ Complete | Department-routed Concierge inquiry form generating ticket reference (`YC-CARE-XXXX`), global studio addresses (London, Porto) & self-service shortcuts |
| 18 | **FAQ** | `/faq` | — | ✅ Complete | Instant keyword filter, 6 category tabs, expand/collapse all & animated editorial accordions |
| 19 | **Size Guide** | `/size-guide` | — | ✅ Complete | Category tabs (`T-Shirts`, `Polo Shirts`, `Hoodies`, `Outerwear`), `CM / INCHES` unit converter, SVG garment schematic, **Interactive Fit Finder** calculator & how-to-measure guide |
| 20 | **Shipping & Delivery** | `/shipping-delivery` | `/shipping` | ✅ Complete | Interactive global destination zone selector (`UK & EU`, `North America`, `Asia-Pacific & UAE`, `Rest of World`), DDP duty clarity & archival packaging overview |
| 21 | **Returns & Refunds** | `/returns-refunds` | `/returns` | ✅ Complete | 30-day promise, 4-step return timeline, eligibility checklist & interactive **Self-Service RMA / Size Exchange Simulator** |
| 22 | **Privacy Policy** | `/privacy-policy` | `/privacy` | ✅ Complete | Sticky legal table-of-contents + interactive **Cookie & Privacy Preferences** manager |
| 23 | **Terms & Conditions** | `/terms-conditions` | `/terms` | ✅ Complete | Sticky legal clause index covering storefront terms, DDP pricing, official IP/trademarks & Design Studio creator preview + printable view |

---

## Global Shared Interactive Components

- **Slide-Over Shopping Bag Drawer** (accessible from any page via header `Bag (N)` or floating bottom-right badge)
- **Instant Search Drawer** (live product filtering + trending tags + jump to `/search`)
- **Size Guide & Fit Finder Modal** (accessible directly from Product Details & Shop filters)
- **Design Studio Early Access Drawer** (newsletter/creator interest signup)
- **All 24 Pages Storefront Directory Drawer** (`All Pages` header pill, floating `YC®` dock menu & footer link for 1-click verification of all routes)
