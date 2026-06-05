# unit-converter

Unit Converter — an npm-publishable TypeScript library.

## Structure

```
src/index.ts    — public API exports
src/*.ts        — core logic (pure TypeScript, no DOM deps)
dist/           — built ESM output (tsup)
agent.json      — agent manifest
```

## Build

```bash
npm install
npm run build     # → dist/index.js + dist/index.d.ts
npm run typecheck
```

## Deploy

Push to main → GitHub Actions:
1. Builds ESM bundle
2. Uploads to R2 at /pkg/unit-converter/ (importable via URL)
