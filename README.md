# sutra.noldor.tech redirect

Static GitHub Pages site that redirects **sutra.noldor.tech** → <https://sutra.topazcomputing.com/>.

Path, query string, and hash are preserved (e.g. `sutra.noldor.tech/foo?x=1` →
`https://sutra.topazcomputing.com/foo?x=1`). GitHub Pages issues a free Let's Encrypt
certificate for the custom domain, so `https://sutra.noldor.tech` works without a
TLS error.

## DNS setup (at the registrar)
`sutra.noldor.tech` is a subdomain, so point it at GitHub Pages with a single CNAME record:

- **Type:** CNAME
- **Host/Name:** `sutra` (the subdomain of `noldor.tech`)
- **Value/Target:** `emmaleonhart.github.io`

The `CNAME` file in this repo sets the Pages custom domain to `sutra.noldor.tech`.

## GitHub Pages setup
Source: deploy from the `main` branch (root). The custom domain populates from the
`CNAME` file. Once DNS resolves, tick **Enforce HTTPS**.
