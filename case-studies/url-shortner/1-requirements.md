# Requirements

## Functional

- Shorten: Given a long URL, generate a unique, short alias (e.g., short.xyz/abc123).

- Redirect: When a short link is visited, redirect (HTTP 301/302) to the original long URL.

- Custom aliases: Allow users to choose a custom slug (e.g., short.xyz/my-blog).

- Expiration: Links can be time‑based (TTL) or permanent.

- Analytics: Track click count, referrer, geolocation, device type.

- User accounts: (Optional) Manage own links, view stats.

## Non-Functional

- Availability: 99.99% (four nines) – redirects must always work.

- Latency: Shorten API < 100ms p99; redirect < 50ms (excluding DNS).

- Scalability: Handle 1B+ short links total; 100M daily active redirects.

- Durability: Zero loss of mapping data.

- Security: Prevent malicious links, rate limiting, abuse detection.
