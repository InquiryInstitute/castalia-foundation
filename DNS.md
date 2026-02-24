# DNS for castalia.foundation (GitHub Pages)

Point **castalia.foundation** to this GitHub Pages site by adding these records where the domain is managed (e.g. Route 53, GoDaddy, Cloudflare).

## Apex domain (castalia.foundation)

### Option A: A records (IPv4)

| Type | Name | Value | TTL |
|------|------|-------|-----|
| A | @ (or castalia.foundation) | 185.199.108.153 | 3600 |
| A | @ | 185.199.109.153 | 3600 |
| A | @ | 185.199.110.153 | 3600 |
| A | @ | 185.199.111.153 | 3600 |

### Option B: AAAA records (IPv6)

| Type | Name | Value | TTL |
|------|------|-------|-----|
| AAAA | @ | 2606:50c0:8000::153 | 3600 |
| AAAA | @ | 2606:50c0:8001::153 | 3600 |
| AAAA | @ | 2606:50c0:8002::153 | 3600 |
| AAAA | @ | 2606:50c0:8003::153 | 3600 |

### Option C: ALIAS/ANAME (Route 53, DNSimple, etc.)

If your DNS provider supports alias records for the apex:

- **Name:** @ (or castalia.foundation)  
- **Target:** `inquiryinstitute.github.io`

## Optional: www subdomain

| Type | Name | Value | TTL |
|------|------|-------|-----|
| CNAME | www | inquiryinstitute.github.io | 3600 |

## After adding DNS

1. In GitHub: **Settings → Pages** for this repo already has custom domain **castalia.foundation**.
2. Wait for DNS to propagate (up to 24–48 hours). GitHub will issue a TLS certificate automatically.
3. Optionally enable **Enforce HTTPS** under **Settings → Pages** (recommended).

## References

- [GitHub: Managing a custom domain for GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
