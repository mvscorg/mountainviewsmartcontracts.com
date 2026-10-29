# mountainviewsmartcontracts.com

The website for Mountain View Smart Contracts: one static page and one image. GitHub Pages publishes the `main` branch as it is, with no build step (`.nojekyll`). The custom domain is in `CNAME`.

## DNS

Cloudflare runs the DNS. Set every website record to **DNS only** (grey cloud), not Proxied, because GitHub can't issue a certificate through the proxy.

| Type | Name | Content | Proxy |
|---|---|---|---|
| A | `@` | four records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` | DNS only |
| AAAA | `@` | four records: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153` | DNS only |
| CNAME | `www` | `mvscorg.github.io` | DNS only |
| TXT | `_github-pages-challenge-mvscorg` | the code from the mvscorg organisation's Settings → Pages → Add a domain | |

The MX records and the SPF TXT record point at a Google Workspace. Keep them while anyone uses those addresses.
