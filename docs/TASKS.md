# Task Backlog — gmoplus-academy-blog-web

## P0 — Critical
- [ ] Skeleton only — lib/api.ts has placeholder/incorrect CMS URLs; all pages return empty or broken content. App must not be deployed until CMS integration is completed and at least one post renders end-to-end

## P1 — High
- [ ] Wrong domain in .env.example — fix to https://academy.gmoplus.com and correct admin-api CMS URL before any deployment
- [ ] vertical-config.ts may contain copy-pasted identity from another blog vertical — verify branding is academy-specific
- [ ] Blog conflict: academy-web already serves /blog inline — decide canonical source for academy.gmoplus.com/blog before this app goes live

## P2 — Medium
- [ ] Newsletter CTA has no backend endpoint
- [ ] No sitemap.xml
- [ ] No robots.txt
- [ ] Search page fires on every keystroke without debounce

## P3 — Low
- [ ] No JSON-LD Article schema on post pages
- [ ] No canonical URL tags across locales
- [ ] Missing pagination on category/tag archive pages
- [ ] ReadingProgress component does not clean up scroll listener on unmount