# Architecture — gmoplus-academy-blog-web

## Stack
- Framework: Next.js (App Router)
- Language: TypeScript
- i18n: next-intl ([locale] prefix routing)
- Styling: Tailwind CSS + tailwind-merge + clsx
- Content safety: isomorphic-dompurify
- No auth, no state management library

## Folder Structure
```
src/
  app/
    [locale]/
      page.tsx              — Blog index (skeleton)
      [slug]/page.tsx       — Post detail (skeleton)
      category/[slug]/      — Category posts (skeleton)
      author/[slug]/        — Author posts (skeleton)
      tag/[slug]/           — Tag posts (skeleton)
      search/page.tsx       — Search (skeleton)
      kategoriler/          — Category list (skeleton)
  components/
    blog/                   — PostCard, FeaturedPost, PostContent,
                              PostHeader, RelatedPosts, TagList,
                              ShareButtons, SidebarSearch,
                              NewsletterCTA, ReadingProgress
    layout/                 — BlogHeader, BlogFooter, BlogSidebar,
                              LanguageSwitcher
  lib/
    api.ts                  — CMS fetch (placeholder URLs — not functional)
    seo.ts                  — OG metadata helpers
    translations.ts         — i18n message loader
    vertical-config.ts      — Blog identity (academy-specific)
  i18n/                     — next-intl config
  middleware.ts             — Locale detection
  types/blog.ts             — Post, Category, Author types
```

## Current Status
Component structure is in place (copied from store-blog-web template) but lib/api.ts fetch URLs are not pointing to a valid CMS endpoint. The app will build but return empty or error pages at runtime.

## What Needs to Be Done
1. Fix .env.example to use https://academy.gmoplus.com domain
2. Wire lib/api.ts to the actual admin-api blog CMS endpoint with correct academy vertical filter
3. Verify vertical-config.ts branding is academy-specific (not copied from another vertical)
4. Test at least one post renders end-to-end before deploying