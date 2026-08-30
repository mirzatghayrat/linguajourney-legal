# Lingua Journey — legal

Public, static, and deliberately tiny: the one thing it hosts is the privacy
policy, because App Store Connect requires a reachable privacy-policy URL before
an app can go to external TestFlight testers or to the App Store.

- `privacy.html` — the policy, English and 简体中文 in one page.
- `index.html` — redirects to it, so the bare repo URL is not a 404.

Served by GitHub Pages. **Not hosted on the app's own relay** on purpose: that
server is in mainland China on a domain with no ICP filing, which is why the API
runs on port 8443 rather than 443. A US App Review reviewer fetching a policy
from a Chinese IP on a non-standard port is a slow, flaky request in exactly the
place where a stall is most expensive.

The source of truth is `docs/legal/privacy-policy.html` in the app repository,
where a comment records which line of code makes each claim in the policy true.
Edit it there and copy it here, not the other way round.
