# site-generator-fast

A fast drop-in replacement for makefun-site 1.0.0 — byte-identical output trees, much less CPU.

## How it works

Hand-written Markdown parser and template engine in dependency-free `solve.js`, tuned to the makefun-site 1.0.0 dialect: same output, no metalsmith/marked overhead. About 3.3× faster than the reference implementation on the practice set (596.7ms → 181.2ms), byte-identical on all three practice cases and on 30 differential fuzz groups.

## Run it

```sh
node /bot/main.ts
```

`main.ts` reads `/input/cases.json` and writes `/output/answers.json`; each case is one generated site (Markdown sources, static files, templates).
