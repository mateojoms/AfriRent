# AfriRent

Below is a UI wireframe specification designed for direct implementation in Next.js + Tailwind + ShadCN UI. It is structured so an AI coding agent can translate it into actual components without ambiguity.

🧭 UI WIREFRAME SPECIFICATION
Kenya Rental Marketplace Web App
1. GLOBAL LAYOUT (ALL PAGES)
Desktop Layout (Primary)
+--------------------------------------------------------------+
| NAVBAR                                                       |
| Logo | Search Bar | Map Toggle | Favorites | Profile         |
+--------------------------------------------------------------+
| FILTERS |                 MAIN CONTENT AREA                  |
| Panel   |  Map View + Listings Grid                         |
|         |                                                   |
|         |  [Map (pins)]   |  [Listing Cards Column]         |
|         |                 |                                  |
+--------------------------------------------------------------+
Mobile Layout
+-----------------------------+
| Logo        Profile         |
+-----------------------------+
| Search Bar                  |
+-----------------------------+
| MAP / LIST TOGGLE          |
+-----------------------------+
| Listings (stacked cards)   |
| Listing Card               |
| Listing Card               |
+-----------------------------+
2. LANDING PAGE (/)
Purpose
Fast entry into search or listing creation.

+--------------------------------------------------------------+
| NAVBAR                                                      |
+--------------------------------------------------------------+
| HERO SECTION                                               |
|--------------------------------------------------------------|
| "Find Homes in Kenya Near You"                             |
| [ Search location or area __________ ]                     |
| [ Find Homes ]   [ List Property ]                        |
+--------------------------------------------------------------+

| FEATURE SECTION                                            |
|--------------------------------------------------------------|
| [Map Icon] Find homes near you                             |
| [Shield] Verified listings                                |
| [Chat Icon] WhatsApp direct contact                       |
+--------------------------------------------------------------+

| FOOTER                                                    |
+--------------------------------------------------------------+
3. AUTH PAGES
3.1 LOGIN
+-----------------------------+
| Login                       |
+-----------------------------+
| Email                      |
| Password                   |
| [ Login Button ]           |
|-----------------------------|
| Continue with Google       |
+-----------------------------+
| No account? Sign up        |
+-----------------------------+
3.2 SIGNUP
+-----------------------------+
| Create Account             |
+-----------------------------+
| Full Name                 |
| Email                     |
| Phone Number              |
| Password                  |
|-----------------------------|
| Select Role:              |
| ( ) House Seeker         |
| ( ) House Owner          |
|-----------------------------|
| [ Create Account ]        |
+-----------------------------+
4. MAIN DASHBOARD (SEEKER)
Layout
+--------------------------------------------------------------+
| NAVBAR                                                      |
+--------------------------------------------------------------+
| FILTERS | MAP VIEW + LISTINGS                               |
|--------------------------------------------------------------|
| Filters:                                                     |
| - Location dropdown                                          |
| - Price range slider                                         |
| - Bedrooms                                                  |
| - Radius selector (5km/10km/20km)                          |
| [Apply Filters]                                             |
|--------------------------------------------------------------|
|                                                              |
| MAP AREA (pins show houses)                                 |
|                                                              |
|--------------------------------------------------------------|
| LISTING CARDS (scrollable)                                  |
| [Card] [Card] [Card]                                        |
+--------------------------------------------------------------+
LISTING CARD COMPONENT
+-----------------------------+
| [IMAGE]                    |
| Price: KES 25,000         |
| Location: Kilimani        |
| 2 Bed | 1 Bath            |
| Short description...      |
|-----------------------------|
| [View] [Save] [WhatsApp]  |
+-----------------------------+
5. LISTING DETAILS PAGE (/listings/[id])
+--------------------------------------------------------------+
| IMAGE GALLERY (carousel)                                    |
+--------------------------------------------------------------+

| TITLE: Modern 2 Bedroom Apartment                          |
| PRICE: KES 35,000                                           |
| LOCATION: Westlands                                         |
+--------------------------------------------------------------+

| MAP PREVIEW                                                |
| (small embedded map with pin)                              |
+--------------------------------------------------------------+

| DESCRIPTION                                                |
| Lorem ipsum...                                             |
+--------------------------------------------------------------+

| OWNER CONTACT                                              |
| [ WhatsApp Owner ]                                         |
| [ Send Inquiry ]                                           |
+--------------------------------------------------------------+
6. OWNER DASHBOARD (/dashboard/owner)
+--------------------------------------------------------------+
| NAVBAR                                                      |
+--------------------------------------------------------------+

| OWNER DASHBOARD                                            |
|--------------------------------------------------------------|
| [ + Create New Listing ]                                   |
+--------------------------------------------------------------+

| YOUR LISTINGS                                              |
|--------------------------------------------------------------|
| [Card] Listing 1  [Edit] [Delete]                         |
| [Card] Listing 2  [Edit] [Delete]                         |
+--------------------------------------------------------------+
7. CREATE LISTING PAGE
+--------------------------------------------------------------+
| Create Listing                                             |
+--------------------------------------------------------------+

| Title                                                     |
| Description                                               |
| Price (KES)                                               |
| Location Name                                             |
| Map Picker (click to set pin)                            |
| Bedrooms                                                  |
| Bathrooms                                                 |
| Upload Images (multi upload)                              |

| [ Save Listing ]                                          |
+--------------------------------------------------------------+
8. FAVORITES PAGE
+--------------------------------------------------------------+
| Saved Listings                                             |
+--------------------------------------------------------------+

| [Card] Favorite 1                                         |
| [Card] Favorite 2                                         |
| [Card] Favorite 3                                         |
+--------------------------------------------------------------+
9. MAP VIEW COMPONENT (CORE FEATURE)
Behavior:
Pins represent listings

Clicking pin shows preview card

Cluster pins when zoomed out

+--------------------------------------------------------------+
|                     MAP AREA                                |
|   •   •   •   •   •   •   •                               |
|        (interactive Mapbox/Google Maps)                   |
|                                                              |
+--------------------------------------------------------------+
10. NAVIGATION STRUCTURE
Navbar:
- Logo (Nyumba / Makazi / etc.)
- Search bar
- Map toggle (Map / List)
- Favorites
- Profile dropdown

Profile dropdown:
- Dashboard
- My Listings (owner only)
- Logout
11. COMPONENT ARCHITECTURE (FOR CODING AGENT)
/components
  Navbar.tsx
  Hero.tsx
  SearchBar.tsx
  FiltersPanel.tsx
  MapView.tsx
  ListingCard.tsx
  ListingGrid.tsx
  ListingCarousel.tsx
  AuthForm.tsx
  RoleSelector.tsx
  WhatsAppButton.tsx
  ImageUploader.tsx
12. UI STYLE GUIDELINES
Design system:
Clean white background

Primary color: deep green or blue (Kenya trust tone)

Rounded cards (lg radius)

Soft shadows

Large images (real estate feel)

Typography:
Headings: bold, modern sans-serif

Body: clean, readable (Inter recommended)

13. INTERACTION RULES
Every listing MUST have a WhatsApp contact button

Map must update when filters change

Listings update instantly on search

Mobile layout defaults to list view (map optional toggle)

14. MVP PRIORITY ORDER (UI BUILD)
Navbar + layout shell

Listing cards

Landing page

Auth pages

Seeker dashboard

Listing details page

Owner dashboard

Create listing page

Map integration

If you want next step, I can generate:

Full Next.js + Tailwind starter code (ready to run in Codespaces)

Or a Supabase schema + RLS security rules (production-grade)

Or a Mapbox integration module already wired to listings


provide prompt for stitch ai to design the ui for this project

Here’s a high-quality Stitch AI prompt tailored specifically for your Kenya rental marketplace. It is structured to produce a production-ready UI design system + screens that can be directly implemented in Next.js + Tailwind + ShadCN.

🎯 STITCH AI PROMPT (COPY & PASTE)
Project: Kenya Rental Marketplace Web App UI
Design a modern, mobile-first web application UI for a Kenya-based rental marketplace that connects house owners and house seekers.

The app allows users to:

Search for rental houses using location-based search and maps

View listings with images, price, and details

Contact owners directly via WhatsApp

Owners to post and manage rental listings

Use geolocation to find nearby houses

🧭 DESIGN REQUIREMENTS
1. Visual Style
Modern real estate marketplace aesthetic

Clean, minimal, high trust design

Mobile-first responsive design

Kenyan context (warm, approachable, trustworthy feel)

Use soft shadows, rounded cards, spacious layout

Prioritize readability and speed

Color direction:
Primary: Deep green or deep blue (trust + stability)

Accent: Warm yellow or orange (calls-to-action)

Neutral: White, light gray backgrounds

Typography:
Clean sans-serif (Inter or similar)

Bold headings, highly readable body text

📱 CORE SCREENS TO DESIGN
1. Landing Page
Include:

Hero section with headline: “Find Homes in Kenya Near You”

Search bar (location input)

Buttons:

“Find a Home”

“List a Property”

Feature highlights:

Verified listings

Location-based search

WhatsApp contact system

2. Authentication Screens
Login Page
Email + password form

Google login option

Simple, centered card layout

Signup Page
Full name, email, phone, password

Role selection:

House Seeker

House Owner

3. Main Marketplace Dashboard (Seeker View)
Design a split layout (desktop):

Left panel:
Filters:

Location

Price range slider

Bedrooms

Radius selector (5km / 10km / 20km)

Center:
Interactive map with pins for listings

Right panel:
Scrollable listing cards

Each listing card includes:

Image

Price (KES)

Location

Bedrooms & bathrooms

“View details”

“Save”

“WhatsApp owner” button

4. Listing Details Page
Include:

Large image gallery carousel

Price and location header

Map preview showing exact location

Description section

Owner contact section:

WhatsApp button (primary CTA)

Inquiry form (secondary)

5. Owner Dashboard
Include:

“Create New Listing” button (prominent)

Grid of user’s listings
Each listing card includes:

Edit button

Delete button

View stats (optional placeholder)

6. Create Listing Page
Form layout with:

Title

Description

Price (KES)

Location name

Map picker (drag pin to set location)

Bedrooms

Bathrooms

Image upload (multi-image)

Submit button

7. Favorites Page
Simple grid of saved listings

Each card allows:

Remove from favorites

View listing

8. Map Component
Design a full-screen interactive map:

Pins represent listings

Cluster pins when zoomed out

Clicking a pin shows preview card

Syncs with filters in real time

⚙️ UX BEHAVIOR REQUIREMENTS
Mobile-first navigation with bottom or top navbar

Listings update dynamically when filters change

Map and list views toggle smoothly

WhatsApp is the primary contact method

Fast browsing experience (low-latency feel)

Smooth animations (subtle, not heavy)

🧱 COMPONENT STYLE SYSTEM
Design reusable components:

Navbar (search + profile + favorites)

ListingCard

FilterPanel

MapView

ImageCarousel

AuthForm

Button system (primary, secondary, danger)

📐 RESPONSIVENESS
Mobile: stacked layout (map optional toggle)

Tablet: split layout

Desktop: 3-column marketplace layout

🧩 PRODUCT GOAL
This UI should feel like:

Airbnb simplicity

Jiji Kenya practicality

WhatsApp-first communication behavior

Mobile-first African internet optimization

🚀 OUTPUT EXPECTATION
Generate:

Complete UI design system

All key screens listed above

Component library consistency

Mobile + desktop responsive variants

Modern SaaS-grade UI suitable for production implementation in Next.js + Tailwind + ShadCN

If you want, I can next generate:

A Figma-style layout breakdown per screen (pixel-level guidance)

Or a ready Next.js frontend code scaffold that matches this UI exactly

Or a branding pack (name, logo direction, colors, typography system)


i have the design and the the documentation guide on how i can clearly instruct kimi to use the two to bring a seemless application

Good. At this stage you need a single orchestration prompt that forces Kimi to treat your design + documentation as source-of-truth specs, and then implement incrementally without drifting.

Below is a ready-to-paste “master implementation prompt” for Codespaces Kimi Copilot.

🧠 MASTER BUILD PROMPT (PASTE INTO KIMI CODE)
Role
You are a senior full-stack engineer building a production-grade web application from provided design files and technical documentation.

Objective
Build a Kenya Rental Marketplace Web Application that connects house owners and house seekers using:

Next.js (App Router)

TypeScript

Tailwind CSS

ShadCN UI

Supabase (Auth + Database + Storage)

Map integration (Mapbox or Google Maps)

Vercel deployment readiness

Critical Instruction (VERY IMPORTANT)
You MUST strictly follow:

UI Design Reference (PRIMARY SOURCE OF TRUTH)

Use the provided UI design exactly as the visual blueprint

Do NOT redesign layouts unless necessary for responsiveness

Match spacing, hierarchy, and component structure

Technical Documentation (SECOND SOURCE OF TRUTH)

Use it for architecture, database schema, features, and logic

Do NOT simplify or remove required features unless explicitly impossible

If conflict exists:

UI design overrides visual structure

Documentation overrides logic and functionality

Build Strategy (MANDATORY ORDER)
You must implement the system in phases:

PHASE 1 — Project Foundation
Initialize Next.js App Router project

Configure TypeScript + Tailwind + ShadCN

Setup folder structure exactly as scalable production app

Configure Supabase client

Setup environment variables

PHASE 2 — Authentication System
Implement Supabase Auth:

Email/password login

Signup with role selection:

owner

seeker

Add:

Protected routes

Role-based access control (RBAC)

Session persistence

PHASE 3 — Core Database Layer
Implement Supabase schema:

users

listings

inquiries

favorites

Ensure:

Proper foreign keys

Row Level Security (RLS) policies

Owners can only edit their listings

Seekers cannot create listings

PHASE 4 — Core UI Implementation (FROM DESIGN FILE)
Build UI exactly according to design:

Pages:
Landing page

Auth pages

Seeker dashboard (map + listings layout)

Listing details page

Owner dashboard

Create listing page

Favorites page

Components:
Navbar

ListingCard

FiltersPanel

MapView

ImageGallery

AuthForm

RoleSelector

WhatsAppButton

PHASE 5 — Marketplace Functionality
Implement:

Listing CRUD (create, read, update, delete)

Image uploads (Supabase Storage)

Geolocation detection (browser API)

Radius-based filtering (5km / 10km / 20km)

Search by location name

Favorites system

PHASE 6 — Map Integration
Implement:

Interactive map with pins

Listing coordinates binding

Pin click → preview card

Sync map with filters and listings

PHASE 7 — Communication System
Implement:

WhatsApp deep link:
https://wa.me/PHONE?text=PRE_FILLED_MESSAGE

Inquiry form saved in database

WhatsApp is PRIMARY communication method.

PHASE 8 — Performance & Security Hardening
Must include:

Input validation (Zod or equivalent)

Image upload validation (size + type)

Rate limiting for listing creation

Environment variable protection

Secure API routes

Loading states + skeleton UI

PHASE 9 — UI/UX POLISH
Implement:

Mobile-first responsiveness

Smooth transitions

Skeleton loaders

Empty states

Error states

Optimized image loading

Architecture Rules
You MUST:

Use reusable components

Avoid duplication

Keep logic separated from UI

Use hooks for data fetching

Use clean folder structure

Folder Structure (STRICT)
/app
/components
/lib
/hooks
/services
/types
/styles
Non-Negotiable Requirements
App must be fully responsive

Must work on mobile-first Kenyan usage conditions

Must prioritize speed and simplicity

WhatsApp integration must be fully functional

Map + listings must be synchronized

Role-based access must be enforced everywhere

Final Output Expectation
The final system must be:

Production-ready

Deployable to Vercel without modification

Cleanly structured and scalable

Fully aligned with UI design provided

Execution Rule
Start building immediately. Do not ask for confirmation. Proceed step-by-step in correct build phases and ensure each phase is functional before moving to the next.

If you want next upgrade
I can also give you:

A “debug-proof Kimi prompt” (prevents hallucinated code / missing Supabase setup)

A Vercel deployment checklist

Or a full production-grade Supabase RLS security script (very important for marketplaces)


Provide a new prompt to be put in readme file such that the coding assistant will be directed to look for  the design pages from the files in the project. The rest of the contenr to remain

Below is a README-ready instruction prompt you can paste directly into your project. It is designed to force any coding assistant (Kimi, Copilot, etc.) to first locate and use your design files inside the repo before generating or modifying UI code.

📄 README — AI CODING INSTRUCTION PROMPT
⚠️ CRITICAL DEVELOPMENT DIRECTIVE
This project contains design reference files inside the repository. These design files are the PRIMARY SOURCE OF TRUTH for all UI/UX implementation.

The coding assistant MUST follow the rules below strictly.

🎯 DESIGN FILE USAGE RULE
Before writing or modifying any UI code, the assistant MUST:

Search the repository for design assets, including but not limited to:

/design

/ui

/assets

/mockups

/figma

Image files (.png, .jpg, .svg)

Any wireframe or UI reference files

Identify all available design screens and UI references

Use those files as the authoritative blueprint for implementation

🧠 UI IMPLEMENTATION RULE
When building or modifying UI:

ALWAYS match the layout, spacing, structure, and hierarchy from the design files

DO NOT invent alternative layouts unless required for responsiveness

DO NOT simplify or reinterpret the design

Pixel structure should be respected as closely as possible in web form

🔁 PRIORITY ORDER (MANDATORY)
If conflicts arise:

Design files inside repository (HIGHEST PRIORITY)

Technical documentation (README / specs)

Existing codebase patterns

Developer intuition (LOWEST PRIORITY — DO NOT RELY ON THIS)

🧩 FUNCTIONAL REQUIREMENTS (UNCHANGED)
All functionality requirements from the project documentation remain fully valid, including:

Authentication (owner / seeker roles)

Listings CRUD system

Geolocation-based search

Map integration

WhatsApp-based communication

Favorites system

Supabase backend integration

These must NOT be reduced or removed when applying design files.

🏗️ DEVELOPMENT BEHAVIOR RULES
The assistant MUST:

First inspect project structure before writing code

Reuse existing components where possible

Create reusable UI components when needed

Maintain clean separation between UI and logic

Ensure mobile-first responsiveness based on design

🚫 STRICT PROHIBITIONS
The assistant MUST NOT:

Ignore design files in the repository

Replace design structure with generic templates

Skip searching for UI references before implementation

Modify layout style without referencing design assets

Assume UI structure without checking project files

📌 FINAL GOAL
The final application must:

Match the provided design files visually and structurally

Be fully functional according to documentation

Be production-ready and deployable to Vercel without UI rework
