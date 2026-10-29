# The CakeHouse Bakery: Project Status & Roadmap

**Target Business:** The CakeHouse Bakery (`https://www.thecakehousebakery.ca/`)  
**Founder & Head Baker:** Tammy  
**Lead Strategist & Project Lead:** Scott  
**Live Interactive Prototype:** [https://scottrepository.github.io/the-cakehouse-bakery/](https://scottrepository.github.io/the-cakehouse-bakery/)  
**GitHub Repository:** [ScottRepository/the-cakehouse-bakery](https://github.com/ScottRepository/the-cakehouse-bakery)  
**Last Updated:** October 29, 2026 (Weddings Showcase Microsite & Copy Integration)  

---

## 1. Project Overview & Tech Stack

### Executive Summary
The CakeHouse Bakery is an artisanal, custom-craft bakery based in Norwood, Ontario, serving Peterborough, the Kawartha Lakes, and Prince Edward County. Following our strategy and review session with Tammy and the integration of the dedicated Weddings & Events Showcase copy, the commercial structure and storefront design are aligned to maximize operational efficiency, protect Tammy's baking bandwidth, and drive guaranteed revenue.

The core platform is built around four focused commercial pillars:
1. **Bespoke Weddings & Inquiries (Primary Web Traffic Driver):** A dedicated micro-site experience providing transparent investment guides ($150 cutting cakes to $450+ tiered showpieces and $275+ croquembouche towers), quarterly $45 tasting boxes (6 miniature cake pairings, Norwood pickup or Canada shipping), a full-width masonry portfolio gallery, Wayward Gent wedding bar integration, and an enhanced date inquiry form with inspiration photo attachments.
2. **The Monthly Baker's Box (Soft Launch Cap: 50 Boxes):** Streamlined single flagship shippable box featuring giant New York-style stuffed cookies ($6/ea) and gourmet fudge brownies engineered for transit across Canada. Promoting in December with waitlist signups; first shipments dispatch January 2027.
3. **In-Person Baking Workshops ($60/Seat):** Hands-on cookie decorating classes at Norwood Town Hall with our signature hot chocolate bar, attendee intake, and an automated urgency trigger that alerts shoppers when inventory reaches 5 or fewer seats.
4. **Everyday Drops (Bi-Weekly Local Pre-Orders):** Alternating schedule between Week A (Brioche Cinnamon Buns in plain 6-packs or assorted 6-packs with gourmet toppings) and Week B (Market cookies and cupcakes). Strictly **Local Norwood Studio Pickup Only** (no shipping for fresh bakes).

*Deferred for Phase 2 (Early 2027):* The Dessert Club (finished monthly local drop club) and The Recipe Vault (digital masterclasses) have been temporarily paused to prevent operational overload.

```
                          ┌──────────────────────────────────┐
                          │   The CakeHouse Bakery Brand     │
                          │ Sage Green Accent & Editorial UI │
                          │  STRICTLY BY APPOINTMENT ONLY    │
                          └─────────────────┬────────────────┘
                                            │
         ┌───────────────────┬──────────────┴──────┬───────────────────┐
         ▼                   ▼                     ▼                   ▼
┌─────────────────┐ ┌─────────────────┐  ┌──────────────────┐ ┌─────────────────┐
│ Bespoke Weddings│ │The Baker's Box  │  │  Town Hall Class │ │ Everyday Drops  │
│(Showcase Microsite│(50 Soft-Launch  │  │($60 / Seat with  │ │  (Bi-Weekly     │
│+ Masonry + $45) │ │ Boxes • Canada) │  │ 5-Seat Trigger)  │ │ Pickup Only)    │
└────────┬────────┘ └────────┬────────┘  └────────┬─────────┘ └────────┬────────┘
         │                   │                     │                   │
         └───────────────────┴──────────┬──────────┴───────────────────┘
                                        ▼
                         ┌─────────────────────────────┐
                         │   Unified Shopify OS 2.0    │
                         │ Slide-Out Cart with Upsells │
                         │ (Wayward Gent Cocktail Jar) │
                         └─────────────────────────────┘
```

---

### Tech Stack & App Architecture

| Component | Prototype Implementation | Production Target (Shopify) |
| :--- | :--- | :--- |
| **Storefront Engine** | Single-Page Application (HTML5 / Tailwind CSS / Vanilla JS) | Shopify Online Store 2.0 (Custom child of Dawn) |
| **Styling & Palette** | Monochrome `#FFFFFF` & `#1A1A1A`, Soft Blush `#E6D8D7`, **Sage Green `#4A5E4D`** | Custom CSS & Web Fonts (Cormorant Garamond + Montserrat) |
| **Appointment Notice** | Prominent top banner warning: *By Appointment Only • No Pop-Ins* | Sitewide sticky announcement bar & checkout disclaimers |
| **Weddings Showcase** | Dedicated Microsite, Masonry Gallery, $45 Tasting Box, Investment Guide, Wayward Gent Modal, Inquiry Uploader | Standalone Page Template (`page.weddings.json`) |
| **Subscriptions Engine** | Flagship Baker's Box: 3-Mo Commitment ($42/mo, Save 15%), Monthly ($48), 1-Time ($52) | **Shopify Subscriptions** (Native, 0% added transaction fees) |
| **Upsell Integration** | Wayward Gent Cocktail Infusion Jar ($18.00) in cart & box builder | Shopify Checkout Extensibility / Theme Upsell Block |
| **Class Inventory Trigger** | Dynamic badge: triggers *"Only 5 seats left"* when inventory $\le$ 5 | Liquid inventory logic (`product.variants.first.inventory_quantity`) |
| **Local Pre-Orders** | Bi-weekly alternating Cinnamon Buns & Market Cookies (Local Pickup) | Shopify Local Pickup settings + Scheduled fulfillment windows |
| **Inquiry & Form Upload** | Form with Date, Servings, Timing, Venue, and File Attachment | Shopify Inbox / Klaviyo Custom Forms / UploadKit |
| **Lead Generation** | VIP Pop-Up & Embedded Footer with *Free Oreo Brookie Recipe* | Shopify Email / Klaviyo (4-part automated welcome sequence) |

---

## 2. Summary of Feedback & Updates Completed

### 1. Weddings & Events Showcase Integration (`weddings_showcase_copy.md`)
* **Hero Section:** "Lavish Cakes & Sweets" / "*The CakeHouse — Where Dessert Becomes Art*".
* **Full-Width High-Resolution Masonry Portfolio Gallery:** Replaced standard e-commerce sidebars with an editorial visual portfolio (Tiered Cakes, French Croquembouche, Artisanal Dessert Bars, Single-Tier Cutting Cakes, Monogram Favours, and Celebration Tiers).
* **Reserve Your Tasting Box ($45.00 CAD):**
  - Updated to **6 miniature signature cake pairings** with Swiss Meringue Buttercreams and fillings.
  - Set release timing for January 2027 in limited batches of 8–9 boxes to eliminate product waste.
  - Clearly articulated delivery options: Scheduled Studio Pickup in Norwood or Canada-wide Tracked Courier Shipping.
* **Investment & Pricing Guide:** Baseline planning investments for Cutting Cakes (from $150), 2 & 3 Tier Cakes (from $450), French Croquembouche (from $275), and Dessert Tables ($4.50+/guest).
* **Sister Company Spotlight (Wayward Gent Cocktails):** Elevated feature with interactive exploration modal detailing artisanal cocktail infusion jars ($18), custom wedding bar favours, and dehydrated garnishes.
* **Wedding Date Inquiry Form:** Multi-field availability form capturing couple names, date, servings/guest count, phone, venue name & city, dessert timing, vision notes, and an **inspiration photo attachment uploader**.

### 2. Brand Styling & Studio Policy Banners
* **Sage Green Brand Accents:** Incorporated Tammy's preferred green banners (`#4A5E4D`) alongside her signature blush accents and editorial typography.
* **Appointment-Only Warning Banner:** Added a top sticky banner making it clear that The CakeHouse operates **strictly by appointment only** from a dedicated home kitchen studio (no daily pop-in retail).

### 3. Streamlining The Baker's Box Subscription
* **Eliminated Complexity:** Removed the Patisserie Box and Junior Baker Family Box. Focused 100% on **The Monthly Baker's Box**.
* **Soft-Launch Capped at 50 Boxes:** Set a 50-subscriber soft-launch limit to test operations and generate predictable recurring revenue without overwhelming Tammy. Promotional waitlist opens in December; first boxes ship in January 2027.
* **Shippable Product Formulation:** Box features giant New York-style stuffed cookies ($6/ea) and gourmet fudge brownies chosen specifically for shipping durability across Ontario and Canada.
* **Pricing & Commitment Options:**
  - 3-Month Plan ($42.00/mo — Save 15%): Recommended option to secure a soft-launch spot.
  - Monthly Billing ($48.00/mo): Flexible monthly subscription.
  - One-Time Gift Box ($52.00): Single box purchase.
* **Dietary Policy:**
  - Nut-free and peanut-free options **completely removed** to eliminate cross-contamination liability in a facility that processes nuts.
  - Added a **Non-Celiac Gluten-Free Option (+ $6.00)** with a clear disclaimer: *"Prepared in a kitchen that handles wheat; not certified celiac-safe."*
* **Cross-Sell / Upsell:** Integrated the **Wayward Gent Cocktail Infusion Jar (+$18.00)** directly into the subscription configurator and slide-out cart drawer.

### 4. Class Setup & Seat Urgency Triggers
* Removed exact remaining seat counts (e.g. no "3 of 16 seats left").
* Replaced with an automated urgency trigger that alerts shoppers with a **"🔥 ONLY 5 SEATS LEFT"** badge once inventory drops to 5 or fewer tickets.

### 5. Everyday Drops (Bi-Weekly Local Pre-Orders)
* Renamed from Seasonal Drops to **Everyday Drops (Bi-Weekly Pre-Orders)**.
* **Local Norwood Pickup Only:** Prominently marked that fresh bakes and cinnamon buns do not ship.
* Structured on a bi-weekly alternating schedule:
  - Week A: Brioche Cinnamon Buns (Classic 6-Pack @ $24 or Assorted Mix with 6 toppings @ $28).
  - Week B: Signature Market Cookies (singles, custom counts, or 6-pack box @ $26) and cupcakes.

### 6. Contact Information & Privacy
* Removed the raw email address (`cakehousebakery@hotmail.com` or `hello@...`) from public view to protect against web scrapers.
* Set general location to **Norwood, Ontario** (exact street address sent with appointment/order confirmation).
* Replaced shop hours with **By Appointment Only**.

### 7. Lead Magnet Documentation
* Authored [`HOW_TO_MANAGE_LEAD_MAGNET.md`](file:///c:/Users/scott/OneDrive/Consulting%20Business/Cakehouse/HOW_TO_MANAGE_LEAD_MAGNET.md) giving Tammy clear, non-technical instructions on where and how to swap the *Oreo Brookie* recipe PDF in both Wix and Shopify.

---

## 3. Current State of the Codebase & Project Files

### Directory Structure
```
📁 ~/the-cakehouse-bakery (Linux Local Git Repository)
│
├── index.html                         <-- Complete, verified prototype with Weddings Showcase
├── PROJECT_STATUS.md                  <-- Master project summary & roadmap (this document)
├── HOW_TO_MANAGE_LEAD_MAGNET.md       <-- Tammy's guide for updating recipe PDFs & automations
├── email_to_tammy_review.md           <-- Updated review email incorporating meeting decisions
├── seo_and_schema_strategy.md         <-- Keyword matrix, JSON-LD schema & 301 redirect map
└── cakehouse_shopify_strategy.md      <-- Comprehensive architecture & lean app recommendations
```

### Key File Reference Links
* **Live Web URL:** [https://scottrepository.github.io/the-cakehouse-bakery/](https://scottrepository.github.io/the-cakehouse-bakery/)
* **Local Prototype HTML:** [index.html](file:///home/scottcarpentier/the-cakehouse-bakery/index.html)
* **Lead Magnet How-To Guide:** [HOW_TO_MANAGE_LEAD_MAGNET.md](file:///c:/Users/scott/OneDrive/Consulting%20Business/Cakehouse/HOW_TO_MANAGE_LEAD_MAGNET.md)
* **Client Review Email:** [email_to_tammy_review.md](file:///c:/Users/scott/OneDrive/Consulting%20Business/Cakehouse/email_to_tammy_review.md)
* **SEO & Redirect Strategy:** [seo_and_schema_strategy.md](file:///c:/Users/scott/OneDrive/Consulting%20Business/Cakehouse/seo_and_schema_strategy.md)
* **Shopify Strategy Blueprint:** [cakehouse_shopify_strategy.md](file:///c:/Users/scott/OneDrive/Consulting%20Business/Cakehouse/cakehouse_shopify_strategy.md)

---

## 4. Immediate Next Steps

### Publishing to GitHub Pages:
Run the following in the `scottcarpentier@penguin` terminal:
```bash
cd ~/the-cakehouse-bakery
git add index.html PROJECT_STATUS.md
git commit -m "feat: complete weddings showcase microsite, masonry gallery & wayward gent modal"
git push origin main
```
This deploys live in ~45 seconds to `https://scottrepository.github.io/the-cakehouse-bakery/`.
