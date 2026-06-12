# gmoplus-academy-blog-web

## What It Does
Standalone Next.js blog for the GMOPlus academy/learning vertical. Intended to serve SEO content about online education, course topics, and learning guides. Currently a skeleton — nearly all implementation is missing.

## Who Uses It
- Learners: organic search traffic on education topics
- Academy users: navigated from academy-web /blog links

## Key Features (intended)
- Multilingual blog (next-intl, [locale] routing)
- Post listing, post detail, category, author, tag, search pages
- Reading progress, social share, newsletter CTA
- HTML sanitization via isomorphic-dompurify
- SEO metadata per post

## Current State
The repo contains the component scaffolding and routing structure (identical to other blog apps) but is functionally a skeleton. lib/api.ts likely has placeholder fetch URLs. No real CMS integration verified. Do not deploy to production without completing the API integration and fixing .env.example domain.

## Business Flow (intended)
1. Admin publishes education article in CMS
2. Blog fetches and renders server-side
3. Reader arrives via organic search
4. Engages with article, follows CTA to academy.gmoplus.com

## Success Criteria
- All post pages return HTTP 200 with correct content (not currently met)
- .env.example uses correct academy domain (currently broken)