# MSK Graffiti Gallery Project Plan

## Overview
This project is for building a modern graffiti/art gallery website for the MSK (Manhattan Subway Kings) community. The goal is to create a CMS-powered site with:

- a gallery of artwork and archive images
- artist and crew profiles
- story/history content
- social sharing
- comments and moderation
- an admin dashboard for content management
- a live deployment on a custom domain

## Recommended stack

- Frontend: Next.js
- CMS/Admin: Payload CMS or Strapi
- Database: PostgreSQL (Supabase, Railway, or Render)
- Media: Cloudinary or Cloudflare Images
- Comments: Hyvor Talk or a custom moderated comments system
- Hosting: Vercel
- Analytics: Google Analytics 4 (already included in the repo)

## Current repo state

Repository:
- https://github.com/williamortiz/MSK

Branch:
- dev/gallery-cms

Current status:
- static landing page exists
- Google Analytics tracking is installed
- project is being migrated from a plain HTML landing page toward a CMS-backed gallery app

## Project goals

1. Replace the static landing page with a modern MSK gallery experience
2. Add an admin dashboard so content can be managed without editing code
3. Support artwork uploads, profile management, stories, and crew content
4. Add social sharing features for artwork and project pages
5. Add comments system with moderation
6. Launch the site on a production domain and keep it live

## Roadmap

### Phase 1 — Planning and architecture
- choose the CMS stack
- choose the database provider
- choose deployment host
- define content models
- define page routes

### Phase 2 — Local setup
- initialize the app
- install dependencies
- configure local environment variables
- connect the database
- connect media storage

### Phase 3 — Build the app
- homepage
- gallery feed
- artwork detail page
- artist pages
- crew pages
- stories/history pages
- about page
- admin login and dashboard

### Phase 4 — Social and comments
- Facebook/X/share links
- copy-link sharing
- comment form
- moderation workflow
- Open Graph tags
- metadata configuration

### Phase 5 — Deployment and testing
- deploy preview environment
- test gallery, admin, and comments
- deploy to production
- configure domain and SSL
- verify Google Analytics

### Phase 6 — Launch and maintenance
- add initial content
- publish featured collection
- monitor analytics and comments
- maintain backups and updates

## Suggested route structure

- `/`
- `/gallery`
- `/gallery/[slug]`
- `/artists`
- `/artists/[slug]`
- `/crews`
- `/crews/[slug]`
- `/stories`
- `/stories/[slug]`
- `/about`
- `/admin`

## Suggested content models

### Artwork
- title
- slug
- artist
- crew
- year
- location
- style
- description
- image
- additional images
- tags
- featured flag
- published flag

### Artist
- name
- alias
- bio
- crew affiliation
- profile image
- social links
- location
- featured flag

### Crew / community
- name
- history
- members
- notable locations
- timeline
- profile image

### Story
- title
- excerpt
- content
- author
- published date
- tags

### Comment
- artwork reference
- author name
- comment text
- approved flag
- created date

## Recommended production setup

```text
Next.js
Payload CMS
PostgreSQL via Supabase
Cloudinary media hosting
Vercel deployment
Google Analytics 4
Custom domain via DNS + SSL
```

## Important notes

- The current repo is a static HTML landing page and is not yet a CMS-backed app.
- A full gallery/admin system will require a proper app runtime and database.
- Once the local environment is set up, the work should continue in the `dev/gallery-cms` branch.

## Files to revisit later

- `index.html`
- `CNAME`
- `styles.css`
- `app.js`

## Next step

When you are ready to continue off chat, start by setting up the local project environment and creating the Next.js + Payload app in this branch.

This file is intended to track the plan so the project can continue without pausing.
