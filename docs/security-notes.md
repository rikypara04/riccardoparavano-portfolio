# Security Notes

## Known transitive advisory

The current Astro toolchain resolves `picomatch` through Astro, Vite, tinyglobby and unstorage. npm reports the ReDoS advisory `GHSA-fc5q-39xc-vjpf`.

## Current exposure

The portfolio is built as a static site. Production deployment contains the generated `dist` output and does not execute Astro, Vite or picomatch for website visitors. No visitor-controlled glob patterns are processed.

## Decision

Do not use `npm audit fix --force` because npm currently proposes a breaking Astro downgrade. Track the advisory through Dependabot and update normally when compatible patched dependencies are available.

## Review condition

Reassess immediately if the architecture changes to server-side rendering, accepts untrusted pattern input, introduces server functions, or runs build tooling against untrusted repository content.