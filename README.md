# Integrated Payroll Astro Clone

Static Astro rebuild of `https://integratedpayroll.us` for moving the public site away from WordPress.

## Commands

```sh
npm install
npm run dev
npm run build
npm run preview
```

The workspace currently expects Node `>=22.12.0`; it was scaffolded with Node `26.5.0`. Run `nvm use` from the project root to match `.nvmrc`.

## Forms

Forms are static HTML and currently post to `/__forms/cloudflare-worker-placeholder`. Replace that placeholder action in `src/components/StaticForm.astro` when the Cloudflare Worker endpoint is ready. Each form includes a hidden `form-name` field.

## Removed Images

These live WordPress images are intentionally not copied, referenced, or hotlinked:

- `https://www.integratedpayroll.us/wp-content/uploads/2026/03/downtown-TC.jpg`
- `https://www.integratedpayroll.us/wp-content/uploads/2026/04/TC-by-the-bay.jpg`

Hero regions that previously depended on those photos use CSS-based branded panels instead.

## Asset Notes

Safe client site assets belong in `public/assets/`. Before launch, search source and build output for `downtown-TC`, `TC-by-the-bay`, and `wp-content/uploads` to confirm the clone is independent of the old WordPress media library.
