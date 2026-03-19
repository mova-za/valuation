# Mova Deep Dive - Full Research Report

_Research date: 2026-03-10_

---

## 1. Company Overview

- **Entity:** Mova Made To Move (Pty) Ltd
- **Registration:** 2025/449997/07 (South Africa)
- **Location:** Cape Town, South Africa
- **Website:** https://mova.madetomove.co.za
- **Linktree:** https://linktr.ee/madetomove.za
- **Instagram:** @mova.za (2,497 followers, 146 posts, 52.1K views/30 days)
- **TikTok:** @mova.za
- **Facebook:** linked from Linktree
- **Information Officer:** CTO (unnamed in public docs)

**Concept:** South African ClassPass. One flexible membership gives access to a network of gyms, studios, and fitness spaces across Cape Town. Credit-based booking system.

---

## 2. Pricing & Plans

| Plan | Price/Month (ZAR) | Credits | Estimated Classes/Month |
|------|-------------------|---------|------------------------|
| Starter | R380 | 40 | 2-3 |
| Happiness | R690 | 65 | 3-5 |
| Joy! | R1,290 | 125 | 6-9 |
| Bliss | R1,790 | 180 | 10-14 |
| Ecstasy | R2,490 | 255 | 15+ |

**Notes:**
- Starter includes promotional upgrade to Happiness in month two
- Monthly auto-renewal
- All plans allow rollover (unused credits carry to next month, capped at plan limit)
- Rollover cap adjusts if plan changes
- Credits expire immediately upon cancellation (non-refundable, non-transferable)

---

## 3. Business Rules (from Terms of Service)

### Booking
- Book up to **14 days** in advance
- Individual studios set their own latest booking times (immediately before class to 24 hours prior)

### Cancellation
- Cancel anytime, no reactivation or cancellation fees
- Must cancel at least **72 hours** before renewal date to avoid charge
- Late cancellation (within studio's window): **R10 per credit** charge, but credits returned

### No-Show
- Credits forfeited + **R15 per credit** penalty
- Platform may waive first-time no-show fee
- Credits typically remain forfeited due to studio payment obligations

### Payment
- Processed in **ZAR through Paystack** (credit/debit card)
- Card data NOT retained by Mova (handled by Paystack)
- Buy-now-pay-later options planned for future

---

## 4. Platform Features

### User-Facing
- Unified class scheduling across 60+ studios
- Browse by location, time, style
- Flexible booking, cancellation, rescheduling
- Credit-based system with rollover
- QR code check-in at studios
- Calendar reminders
- Referral program
- Push notifications
- Subscription management in-app
- Promo code support
- Dark mode
- Save favorite studios
- 850+ weekly classes (website also claims 1,000+)

### Studio/B2B Side
- Partner application via Flodesk form: https://mova.myflodesk.com/partner-with-mova
- Studios listed for free
- Payment per completed booking (graduated)
- Studio receives booking data for reservation management only
- Studios cannot independently market to Mova users

---

## 5. App Store Data

### iOS (App Store)
- **Version:** 1.2.2 (Feb 17, 2026)
- **Rating:** 4.3/5 (3 ratings only)
- **Size:** 55.9 MB
- **Compatibility:** iOS 15.1+, iPad, iPod touch, macOS 12.0+ (M1), visionOS 1.0+
- **Language:** English
- **Age Rating:** 18+
- **Category:** Health & Fitness
- **Price:** Free
- **Privacy:** Collects linked contact info and phone numbers; location data collected but not linked to identity

**Recent Updates (v1.2.2):**
- Studio map grouping
- Referral features
- Push notifications
- Subscription management
- Promo codes
- Dark mode improvements

**Reviews:**
- Positive: "Transformative for fitness routine in Cape Town"
- Negative: "UI friction where scrolling inadvertently clicks classes"

### Google Play
- **Package:** za.co.madetomove.mova
- Could not extract details (JS-rendered page)

---

## 6. Known Tech Stack

### Confirmed (from privacy policy + terms)
- **Payment Processing:** Paystack (ZAR, credit/debit card)
- **Analytics:** Google Analytics, Mixpanel
- **Data Security:** Encryption, secure hosting, access controls (specifics not disclosed)
- **Marketing/Forms:** Flodesk (partner onboarding)
- **Link Management:** Linktree

### Inferred from App
- Native iOS + Android apps (separate builds based on App Store listing)
- QR code generation/scanning for check-ins
- Push notification service (APNs + FCM)
- Geolocation services (for studio discovery)
- Calendar integration

### Unknown
- Frontend framework (React Native? Flutter? Native Swift/Kotlin?)
- Backend language/framework
- Database
- Hosting provider
- API architecture

---

## 7. Competitor Comparison: Flex Pass

| Feature | Mova | Flex Pass |
|---------|------|-----------|
| **Studios** | 60+ claimed | 24 named, 28 listed |
| **Pricing** | R380-R2,490/mo (5 tiers) | R750-R2,290/mo (4 tiers) |
| **Credits** | 40-255/mo | 26-86/mo |
| **Cheapest Plan** | R380 (Starter) | R750 (Basic) |
| **App Type** | Native iOS + Android | PWA (Progressive Web App) |
| **Instagram** | 2,497 followers | 2,879 followers |
| **Posts** | 146 | 85 |
| **Rollover** | Yes (capped at plan limit) | Yes (capped at plan limit) |
| **Cancellation** | Anytime, 72hr before renewal | Anytime |
| **No-show fee** | R15/credit | R50 flat |
| **Payment** | Paystack | Unknown |
| **Check-in** | QR code | Unknown |
| **B2B model** | Free listing, pay per booking | Free listing, pay per booking |

**Mova Advantages:**
- Cheaper entry point (R380 vs R750)
- More studios (60+ vs 28)
- Native app (vs PWA)
- More credit tiers/flexibility
- Lower no-show penalty structure

**Flex Pass Advantages:**
- Slightly more Instagram followers
- Longer in market (based on content volume)
- Named/visible studio partnerships
- Credits never expire (vs Mova's expire on cancel)

---

## 8. FAQ Topics (Questions Listed, Answers Not Publicly Visible)

### Privacy & Account
- Do you track where I live?
- When does my subscription renew?

### Membership & Credits
- How long am I committed for?
- Do my credits roll over?
- When do credits expire?
- Can I transfer or refund credits?
- I ran out of credits - how do I get more?
- Can I pause or cancel?

### Bookings, Check-ins & Schedules
- Where do I see my bookings?
- How far in advance can I book?
- I forgot to check in - what happens?
- How do I know studio schedules fit my life?

### Cancellations & No-Shows
- How do cancellations work?

### Studios & Data
- Do studios get my personal data?
- Do I need to sign waivers?
- One of my favourite studios isn't on MOVA - what do I do?

---

## 9. What It Would Take to Rebuild Mova

### The Question
Can Callie rebuild the entire Mova app with Claude Code, owning the IP, as a solo founder with AI assistance?

### Short Answer
**Yes, absolutely.** People are building complete SaaS products with Claude Code in 2026. One developer shipped a Rails SaaS with 38,632 lines of code across 727 commits in ~8 weeks. A fitness booking marketplace is well within range.

### Recommended Tech Stack for Rebuild

#### Frontend (Mobile App)
- **React Native** or **Expo** (cross-platform iOS + Android from single codebase)
- Why: Massive ecosystem, easy to find help, Claude Code excels at React/JS
- Alternative: Flutter (Dart) - also viable but smaller ecosystem

#### Backend
- **Node.js** (Express or Fastify) or **Python** (Django/FastAPI)
- Why: Claude Code writes excellent Node.js and Python. Django has built-in admin panel which saves time.
- Recommendation: **Node.js + Express** for API, matches React Native JS ecosystem

#### Database
- **PostgreSQL** (primary relational DB - users, bookings, studios, credits)
- **Redis** (caching, session management, real-time availability)

#### Authentication
- **Firebase Auth** or **Supabase Auth** (handles email, social login, phone auth)
- Or roll own with JWT + bcrypt

#### Payment Processing
- **Paystack** (same as current Mova - ZAR support, SA-focused)
- Already has subscription/recurring billing APIs

#### Hosting/Infrastructure
- **Vercel** or **Railway** (backend API)
- **Supabase** (database + auth + realtime - could replace several services)
- **AWS S3** or **Cloudflare R2** (image/file storage)
- Or **DigitalOcean** (simple, cheap, SA-adjacent data centers)

#### Additional Services
- **Expo Push Notifications** (if using Expo) or **Firebase Cloud Messaging**
- **Google Maps API** (studio locations, distance)
- **QR code generation** (simple library, no external service needed)
- **Mixpanel** or **PostHog** (analytics - PostHog is free/open-source)
- **Resend** or **Postmark** (transactional email)

### Core Features to Build

1. **User App (React Native/Expo)**
   - Registration/login (email, social, phone)
   - Studio browsing (map view, list view, filters)
   - Class schedule browsing (by studio, by time, by type)
   - Credit-based booking system
   - QR code check-in
   - Subscription management (plan selection, upgrade/downgrade)
   - Push notifications (booking reminders, new classes)
   - Favorites/saved studios
   - Booking history
   - Referral system
   - Promo code redemption
   - Profile management
   - Dark mode

2. **Studio Dashboard (Web App - React or Next.js)**
   - Class schedule management (CRUD)
   - Booking management (view, confirm, cancel)
   - Check-in verification (scan QR)
   - Revenue/analytics dashboard
   - Studio profile management

3. **Admin Dashboard (Web App)**
   - User management
   - Studio onboarding/management
   - Credit system configuration
   - Pricing/plan management
   - Analytics and reporting
   - Content management
   - Support ticket handling

4. **Backend API**
   - User auth + sessions
   - Credit ledger system (allocate, deduct, rollover, expire)
   - Booking engine (availability, conflicts, waitlists)
   - Payment/subscription management (Paystack integration)
   - QR code generation + validation
   - Push notification service
   - Studio data sync
   - Admin endpoints
   - Reporting/analytics endpoints

### Estimated Timeline (Solo + Claude Code)

| Phase | Duration | What |
|-------|----------|------|
| Planning + Architecture | 1 week | DB schema, API design, wireframes |
| Auth + User Management | 1 week | Registration, login, profiles |
| Studio + Class System | 2 weeks | Studio CRUD, schedules, search/filter |
| Booking Engine + Credits | 2 weeks | Core booking logic, credit ledger |
| Payment Integration | 1 week | Paystack subscriptions, webhooks |
| QR Check-in | 3 days | Generate + scan + validate |
| Notifications | 3 days | Push, email, reminders |
| Studio Dashboard | 1.5 weeks | Web portal for studio partners |
| Admin Dashboard | 1 week | Management interface |
| Polish + Testing | 2 weeks | Bug fixes, edge cases, UI polish |
| App Store Submission | 1 week | Screenshots, descriptions, review process |

**Total: ~12-14 weeks** (3-3.5 months) working full-time with Claude Code

### Estimated Cost

| Item | Cost |
|------|------|
| Apple Developer Account | $99/year |
| Google Play Developer | $25 one-time |
| Hosting (Railway/Vercel) | $0-20/month initially |
| Database (Supabase free tier) | $0 initially |
| Paystack | Transaction fees only (no monthly) |
| Domain | Already owned |
| Google Maps API | Free tier covers initial usage |
| Push notifications | Free (Firebase/Expo) |
| **Total to launch** | **~$150-200** |

### IP Considerations

**Critical question:** What does Callie's partnership agreement say about IP ownership? Before building:
1. Review the Mova partnership/shareholder agreement
2. Determine who owns the IP (code, brand, user data)
3. If Callie owns the brand "Mova" - she can rebuild freely
4. If the company owns it - she may need to negotiate or rebrand
5. User data likely stays with the company entity
6. Studio relationships are personal/contractual - those can transfer

### The Honest Assessment

Building a Mova clone is 100% doable with Claude Code as a solo developer. The app is a **standard marketplace/booking platform** - not rocket science. The hard parts are:

1. **Studio relationships** (business development, not code)
2. **User acquisition** (marketing, not code)
3. **Reliability at scale** (can be addressed incrementally)
4. **Payment edge cases** (refunds, failed charges, disputes)

The code is the easy part. The business is the hard part. But Callie already has the business knowledge, the studio relationships, and the market understanding. Claude Code handles the rest.

---

## 10. Market Context

- Global fitness app market: projected $20B+ by 2030
- AI in fitness/wellness: $9.8B (2024) projected to $46.1B by 2034
- 1.1B+ fitness app users expected globally by 2026
- ClassPass (the global version of this model) uses: Django, PostgreSQL, JavaScript, Python, AWS, TensorFlow
- Typical ClassPass clone development cost (agency): $50K-$100K
- With Claude Code as solo dev: effectively $150-200 in infrastructure costs

---

_This research was saved properly this time. No more 11-hour thinking sessions with nothing to show for it._
